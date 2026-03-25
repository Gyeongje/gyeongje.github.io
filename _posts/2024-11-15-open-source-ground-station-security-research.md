---
layout: page
title: "Security Analysis of Open-Source Satellite Ground Station Software"
subtitle: "Vulnerability discovery and RF fuzzing on TinyGS"
date: 2024-11-15 00:00:00 +0900
categories: ["satellite"]
---

## 개요

본 연구는 오픈소스 위성 지상국 소프트웨어인 **TinyGS**를 대상으로 보안 분석을 수행한 결과이다. TinyGS는 SatNOGS와 함께 대표적인 오픈소스 지상국 프로젝트로, 2024년 4월 기준 5,264명의 사용자와 1,632개의 활성 지상국을 보유하며, 총 8,860,691건의 Telemetry 데이터를 수신하였다.

연구를 통해 **MQTT Spoofing**, **위조 RF 신호 송신**, **DoS 취약점 2건**(메모리 커럽션)을 발견하였고, 이를 chaining하여 공격 시나리오를 구성하였다. 또한 위성/지상국 자동화 보안 시나리오 및 **RF Fuzzer**를 설계 및 구현하였다.

---

## 배경

### NewSpace와 지상국 보안

뉴스페이스(NewSpace) 시대에 진입하면서 민간 기업들의 위성 운용이 급증하고 있다. 하지만 위성 시스템은 역사적으로 **Security by Obscurity**에 의존해왔으며, 지상국 인프라에 대한 보안 연구는 매우 제한적이다.

지상국은 위성과 지상 네트워크를 연결하는 핵심 노드이며, 지상국을 장악하면 단일 스테이션뿐 아니라 전체 네트워크에 영향을 미칠 수 있다.

![Research Scenario]({{ "/assets/img/blog/ground-station/image3.png" | prepend: site.baseurl }})

### TinyGS 아키텍처

TinyGS는 크게 3개의 구성요소로 이루어진다:

| 구성요소 | 역할 |
|---------|------|
| **TinyGS Server** | 위성 데이터 수집 및 배포 중앙 플랫폼 |
| **MQTT Broker** | 지상국과 서버를 연결하는 메시지 버스 |
| **ESP32 Ground Station** | LoRa 칩(SX126x/SX127x)이 탑재된 ESP32 보드로 위성 신호 수신 |

**동작 흐름:**
1. 지상국이 LoRa 칩을 통해 위성 RF 신호 수신
2. HPD14A 칩이 하드웨어적으로 신호를 복조하여 raw binary 생성
3. MQTT Broker를 통해 TinyGS Server로 데이터 전송
4. Server에서 디코딩하여 텔레메트리 패킷 완성

### 지상국 Setup

![TinyGS Installer]({{ "/assets/img/blog/ground-station/image5.png" | prepend: site.baseurl }})

TinyGS 지상국을 운용하려면:
1. TinyGS Installer를 통해 ESP32 보드에 펌웨어 플래싱
2. WiFi Config Page에서 SSID, 비밀번호, 위도/경도/Timezone 설정
3. 설정 완료 시 MQTT Broker에 연결되어 위성 신호 수신 대기

![WiFi Config Page]({{ "/assets/img/blog/ground-station/image6.png" | prepend: site.baseurl }})

![TinyGS Board (LILYGO LORA32)]({{ "/assets/img/blog/ground-station/image7.png" | prepend: site.baseurl }})

---

## 취약점 1: MQTT Server Spoofing

### 발견

![MQTT Config Fields]({{ "/assets/img/blog/ground-station/image9.png" | prepend: site.baseurl }})

TinyGS Setup 과정 중 WiFi Configuration 단계에서 **Server Address, Server Port, MQTT Username, MQTT Password**를 임의로 변경할 수 있는 문제가 발견되었다.

### PoC

![Fake MQTT Server (Mosquitto)]({{ "/assets/img/blog/ground-station/image10.png" | prepend: site.baseurl }})

**Mosquitto** 프레임워크를 이용하여 MQTT 서버를 구축하였다. `0.0.0.0`으로 바인딩하여 외부 IP에서도 MQTT 데이터를 주고받을 수 있음을 확인하였다.

위조된 MQTT Server로부터 위성 데이터 요청이 정상적으로 이루어지는 것을 확인하였다.

---

## 취약점 2: 위조 RF 신호 송신

### 분석

TinyGS의 신호 수신 코드를 분석하여 Satellite Packet Data를 위조한 RF 신호를 송신할 수 있는 방법을 발견하였다. **PlatformIO IDE**를 사용하여 별도의 ESP32 보드에 LoRa 송신 코드를 작성하였다.

NORBI 위성의 beacon 신호를 송신하기 위한 주요 파라미터:

| Parameter | Value |
|-----------|-------|
| Frequency | 436.703 MHz |
| Bandwidth | 250 KHz |
| Spreading Factor | 10 |
| Coding Rate Denominator | 5 |
| Baud Rate | 250,000 |

![Norbi Satellite TX Code]({{ "/assets/img/blog/ground-station/image12.png" | prepend: site.baseurl }})

### RF 신호 송신 확인

![Serial Monitor — Packet Sending]({{ "/assets/img/blog/ground-station/image13.png" | prepend: site.baseurl }})

코드를 보드에 업로드하면 Serial Monitor를 통해 패킷 송신 메시지를 확인할 수 있다.

![Gqrx Waterfall — 436.703MHz]({{ "/assets/img/blog/ground-station/image14.png" | prepend: site.baseurl }})

**Gqrx** SDR 소프트웨어를 통해 436.703MHz에서 위조 신호가 정상적으로 발생하고 있음을 waterfall diagram으로 확인하였다.

### Full Attack Chain

일반적인 방법으로는 TinyGS 지상국이 특정 위성 신호를 수신하려면 해당 위성의 궤도가 지상국 위를 지날 때까지 기다려야 한다. 이 대기 시간을 없애기 위해 MQTT Broker에 직접 연결하여 위성 수신 대기 payload를 전송하였다.

![MQTT Client for Signal Waiting]({{ "/assets/img/blog/ground-station/image15.png" | prepend: site.baseurl }})

payload가 TinyGS 펌웨어에 전달되면 지상국이 NORBI 위성 신호를 수신 대기하는 상태로 전환된다.

![TinyGS Board — NORBI 수신 대기 상태]({{ "/assets/img/blog/ground-station/image16.png" | prepend: site.baseurl }})

![TinyGS 수신 로그 — 위조 패킷 수신 확인]({{ "/assets/img/blog/ground-station/image17.png" | prepend: site.baseurl }})

앞서 Arduino 코드를 이용하여 송신한 위조 패킷이 TinyGS 지상국에서 정상 위성 패킷으로 처리되어 TinyGS 프로젝트에 업로드된 것을 확인하였다.

![TinyGS Console — 위조 패킷이 정상 패킷으로 인식]({{ "/assets/img/blog/ground-station/image18.png" | prepend: site.baseurl }})

### Packet Decoding

수신된 raw binary 데이터를 해석하기 위해 GitHub의 `4m1g0/tinygs-decoders`를 기반으로 NORBI 패킷 디코더를 수정하여 작성하였다.

![수신 로그 — 위성 패킷 상세]({{ "/assets/img/blog/ground-station/image11.png" | prepend: site.baseurl }})

---

## 취약점 3 & 4: DoS via MQTT Topic Parsing

TinyGS 펌웨어의 MQTT Communication 중 Topic Parsing 부분에서 DoS(Exception) 취약점 2건이 발견되었다. **ESP32 Exception Decoder**를 사용하여 크래시 로그를 분석하였다.

### DoS #1: strcmp NULL 역참조

![DoS Bug #1 — 취약 코드]({{ "/assets/img/blog/ground-station/image20.png" | prepend: site.baseurl }})

MQTT Topic 포맷: `tinygs/[mqtt_id]/[GS_name]/[cmnd]/...`

Topic을 `/`로 파싱하는 코드에서, **슬래시가 3개 미만인 비정상 topic**을 전송하면 354번 라인의 `strcmp`가 NULL을 참조하여 Exception이 발생한다.

![ESP32 Exception — DoS #1]({{ "/assets/img/blog/ground-station/image21.png" | prepend: site.baseurl }})

### DoS #2: Packet Length Overflow

![DoS Bug #2 — 취약 코드]({{ "/assets/img/blog/ground-station/image22.png" | prepend: site.baseurl }})

Packet Receive 코드에서 패킷 길이가 최대 255인데, `respLen` 변수가 TinyGS Board의 **Setup Board Length** 값으로 설정된다. FSK 모듈레이션 모드에서는 MQTT를 통해 이 Length를 255보다 크게 설정할 수 있다.

이후 255바이트를 초과하는 패킷을 수신하면 오버플로우가 발생하여 Exception이 트리거된다.

![ESP32 Exception — DoS #2]({{ "/assets/img/blog/ground-station/image23.png" | prepend: site.baseurl }})

---

## Vulnerability Chaining

개별 취약점을 **chaining**하여 더 큰 영향의 공격 시나리오를 구성할 수 있다:

```
1. DoS Attack → TinyGS Exception으로 Setup 상태로 강제 전환
2. WiFi Hijack → 재부팅 시 WiFi hotspot 모드 진입 → 초기 Setup 페이지 접근
3. MQTT Spoofing → 위조 MQTT Server 연결 → 수신 패킷 및 주파수 정보 확인
4. RF Spoofing → 위조 위성 신호 송신 → 지상국에 가짜 데이터 주입
```

---

## Satellite & Ground Station Fuzzer

### 설계

![Fuzzing Scenario]({{ "/assets/img/blog/ground-station/image24.png" | prepend: site.baseurl }})

TM/TC 프로토콜의 패킷을 뮤테이션하고, RF 또는 네트워크 경로를 통해 대상 시스템에 전달하여 자동으로 취약점을 검증할 수 있는 시스템을 설계하였다.

### Mutation Engine

![Radamsa]({{ "/assets/img/blog/ground-station/image25.png" | prepend: site.baseurl }})

Mutation 엔진은 **Radamsa**를 사용하였다.

### Corpus Collection

![TinyGS Packet Web Crawler]({{ "/assets/img/blog/ground-station/image26.png" | prepend: site.baseurl }})

TinyGS 프로젝트에 실시간으로 수신되는 Raw Packet Data를 수집하는 **TinyGS Packet Crawling Platform**을 Python으로 개발하여 Fuzzer Corpus로 활용하였다.

### RF Fuzzer Architecture

![RF Fuzzer Architecture]({{ "/assets/img/blog/ground-station/image27.png" | prepend: site.baseurl }})

```
┌──────────────────┐     ┌───────────────┐     ┌───────────────┐
│  Fuzzer Server    │────▶│ Attack Board  │─RF─▶│ TinyGS Board  │
│  - Crawled Corpus │     │ (ESP32+LoRa)  │     │ (Fuzz Target) │
│  - Radamsa Mutate │     │ - Socket Recv │     │               │
│  - Crash Logging  │     │ - Modulation  │     │               │
│  - Coverage Track │     │ - RF Transmit │     │               │
└──────────────────┘     └───────────────┘     └───────────────┘
```

- **Fuzzer Server**: 중앙 처리 장치 — Corpus 관리, Mutation 패킷 생성, Crash 발생 시 Coverage 저장 및 Log 처리
- **Attack Board**: Fuzzer Server로부터 Mutation Packet을 수신하여 modulation 후 TinyGS Board로 RF 송신
- **Target Board**: 지상국 펌웨어가 로딩된 상태로 RF 신호 수신 및 처리

Blackbox fuzzing 방식으로, **소스코드 계측(instrumentation) 없이** 동작하므로 폐쇄 소스 지상국 소프트웨어에도 적용 가능하다.

### 동작 확인

![RF Fuzzer Running]({{ "/assets/img/blog/ground-station/image28.png" | prepend: site.baseurl }})

왼쪽은 Fuzzer Server이며, Mutation된 TM/TC 패킷을 생성하여 Attack Board로 전송한다. 오른쪽 상단의 Attack Board Terminal은 Fuzzer Server로부터 Packet data를 수신하고, Modulation하여 오른쪽 하단의 TinyGS 지상국으로 RF 신호를 전송하는 모습이다. TinyGS 지상국이 Attack Board가 송신한 신호를 정상적으로 수신하고 있음을 확인할 수 있다.

---

## 결론

본 연구를 통해 오픈소스 지상국 소프트웨어의 보안 취약점을 발견하고, 이를 chaining하여 실제 공격 시나리오를 구성할 수 있음을 증명하였다. 발견된 취약점은 단일 지상국에 국한되지 않으며, 전체 네트워크로 확대될 수 있는 잠재적 위협이다.

뉴스페이스 시대의 확산과 함께 위성 지상국의 보안은 더욱 중요해지고 있으며, 본 연구에서 개발한 RF Fuzzing 프레임워크는 위성 통신 시스템의 체계적인 보안 검증을 위한 기반을 제공한다.

---

## References

- [1] 윤재호, 박소영. 뉴스페이스 시대의 우주산업 현황과 향후 전망. 한국항공우주학회 추계학술대회. 2022
- [2] TinyGS: [tinygs.com](https://tinygs.com)
- [3] LoRa Frequency: [mokosmart.com/lora-frequency](https://www.mokosmart.com/lora-frequency)
- [4] tinygs-decoders: [github.com/4m1g0/tinygs-decoders](https://github.com/4m1g0/tinygs-decoders)
- [5] TinyGS Ground Station Config: [github.com/G4lile0/tinyGS/wiki](https://github.com/G4lile0/tinyGS/wiki/Ground-Station-configuration)
- [6] Gqrx SDR: [gqrx.dk](https://www.gqrx.dk)
