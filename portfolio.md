---
layout: page
title: Portfolio
subtitle: Research & Experience
permalink: /portfolio/
---

<div style="text-align: center; margin-bottom: 20px;">
  <a href="#" class="cv-download" onclick="generatePortfolioPDF(); return false;">
    <i class="fa fa-download"></i> Download Portfolio
  </a>
</div>

<div id="portfolio-content">

<!-- ==================== PROJECTS ==================== -->
<div class="pf-projects">
  <h2 class="pf-projects__title"><i class="fa fa-flask"></i> Projects</h2>

  <!-- ===== macOS BT ===== -->
  <div class="pf-project" id="macos-bt">
    <div class="pf-project__header">
      <h3 class="pf-project__name" data-en="🍎 macOS Kernel Bluetooth Chipset Security Research" data-ko="🍎 macOS 커널 블루투스 칩셋 보안 연구">🍎 macOS 커널 블루투스 칩셋 보안 연구</h3>
      <span class="pf-project__period">2026.02 ~ 2026.12</span>
    </div>
    <p class="pf-project__desc"
       data-en="Bluetooth chipsets on virtually every IoT device expose a Host Controller Interface (HCI) for debugging, including a WriteRAM primitive that lets the host write arbitrary memory in the chipset. Attackers in the wild patched chipset firmware via WriteRAM to turn the chip into an SDR-like arbitrary BT RF transmitter, after which Broadcom hardened the firmware with a mitigation blocking WriteRAM. This research targets the Broadcom chipset shipped in every MacBook, aiming to analyze and bypass that mitigation. With no public PoC available, prior related research informed the firmware extraction, the chipset-to-kernel interaction surface was mapped end-to-end, and the mitigation logic was reverse-engineered. A bypass was implemented against the mitigation code path, successfully re-enabling the restricted WriteRAM HCI primitive."
       data-ko="다양한 IoT 기기에 탑재되는 블루투스 칩셋은 OS Host와의 디버깅을 위해 Bluetooth Host Controller Interface(HCI)를 제공하며, 그 주요 기능 중 RAM 영역에 메모리를 Write할 수 있는 WriteRAM 기능이 존재합니다. 이 기능을 통해 펌웨어를 변조하면 마치 SDR·모뎀처럼 원하는 블루투스 RF 신호를 송신할 수 있게 Weaponizing할 수 있어, ITW(In the Wild)에서 악용 사례가 적발되었고 Broadcom은 칩셋 펌웨어 내 WriteRAM 기능을 차단하는 Mitigation을 적용했습니다. 본 연구는 모든 MacBook에 탑재되는 Broadcom 칩셋을 대상으로, 이 Mitigation이 어떻게 적용되었는지 분석하고 최종적으로 우회하는 것을 목표로 진행했습니다. 공개된 PoC나 상세 자료가 없는 상태였기에 이전 유사 연구 사례를 조사해 펌웨어를 추출했고, 칩셋 펌웨어와 macOS 커널이 어떻게 상호작용하는지 시스템 전체 동작 과정을 분석했습니다. 그 과정에서 Mitigation 적용 지점을 리버스 엔지니어링으로 파악했고, 분석한 내용을 토대로 실제 Mitigation 코드를 Bypass할 수 있는 아이디어를 적용하여 기능이 제한되어 있던 HCI 주요 기능인 WriteRAM 활성화에 성공했습니다.">
    다양한 IoT 기기에 탑재되는 블루투스 칩셋은 OS Host와의 디버깅을 위해 Bluetooth Host Controller Interface(HCI)를 제공하며, 그 주요 기능 중 RAM 영역에 메모리를 Write할 수 있는 WriteRAM 기능이 존재합니다. 이 기능을 통해 펌웨어를 변조하면 마치 SDR·모뎀처럼 원하는 블루투스 RF 신호를 송신할 수 있게 Weaponizing할 수 있어, ITW(In the Wild)에서 악용 사례가 적발되었고 Broadcom은 칩셋 펌웨어 내 WriteRAM 기능을 차단하는 Mitigation을 적용했습니다. 본 연구는 모든 MacBook에 탑재되는 Broadcom 칩셋을 대상으로, 이 Mitigation이 어떻게 적용되었는지 분석하고 최종적으로 우회하는 것을 목표로 진행했습니다. 공개된 PoC나 상세 자료가 없는 상태였기에 이전 유사 연구 사례를 조사해 펌웨어를 추출했고, 칩셋 펌웨어와 macOS 커널이 어떻게 상호작용하는지 시스템 전체 동작 과정을 분석했습니다. 그 과정에서 Mitigation 적용 지점을 리버스 엔지니어링으로 파악했고, 분석한 내용을 토대로 실제 Mitigation 코드를 Bypass할 수 있는 아이디어를 적용하여 기능이 제한되어 있던 HCI 주요 기능인 WriteRAM 활성화에 성공했습니다.
    </p>
    <div class="pf-project__tags">
      <span class="pf-tag">macOS Kernel</span><span class="pf-tag">Bluetooth</span><span class="pf-tag">Broadcom</span><span class="pf-tag">HCI</span><span class="pf-tag">Firmware</span><span class="pf-tag">Mitigation Bypass</span>
    </div>
  </div>

  <!-- ===== MS Exchange Server ===== -->
  <div class="pf-project" id="ms-exchange">
    <div class="pf-project__header">
      <h3 class="pf-project__name" data-en="📧 MS Exchange Server Vulnerability Research" data-ko="📧 MS Exchange Server 취약점 연구">📧 MS Exchange Server 취약점 연구</h3>
      <span class="pf-project__period">2026 ~ 2026.12</span>
    </div>
    <p class="pf-project__desc"
       data-en="A recently started offensive research effort targeting Microsoft Exchange Server, a foundational on-premise enterprise service. After mapping the broader system architecture, an unpublished 1-day was reproduced as a Cross-Site Scripting (XSS) trigger inside the Exchange Mailbox surface, validating an attack scenario that affects mailbox data and session context under authenticated user privileges. The work expands prior research scope from client / embedded / kernel into enterprise server and SaaS-adjacent attack surfaces."
       data-ko="최근 시작한 Offensive Security 연구로, 온프레미스 엔터프라이즈 환경에서 널리 운영되는 Microsoft Exchange Server를 대상으로 진행 중입니다. 전체 시스템 구조 분석부터 시작해, 공개되지 않은 최신 1-day를 재현하는 데 성공했습니다. 해당 1-day는 Exchange Mailbox 내에서 XSS(Cross-Site Scripting)을 트리거할 수 있는 경로를 갖고 있어, 인증된 사용자 권한 안에서 메일박스 데이터·세션 컨텍스트에 영향을 줄 수 있는 공격 시나리오를 검증했습니다. 기존에 수행해 온 클라이언트·임베디드·커널 연구에서 한 단계 확장해, 엔터프라이즈 서버 및 SaaS 인접 영역으로 분석 범위를 넓혀가는 단계의 연구입니다.">
    최근 시작한 Offensive Security 연구로, 온프레미스 엔터프라이즈 환경에서 널리 운영되는 Microsoft Exchange Server를 대상으로 진행 중입니다. 전체 시스템 구조 분석부터 시작해, 공개되지 않은 최신 1-day를 재현하는 데 성공했습니다. 해당 1-day는 Exchange Mailbox 내에서 XSS(Cross-Site Scripting)을 트리거할 수 있는 경로를 갖고 있어, 인증된 사용자 권한 안에서 메일박스 데이터·세션 컨텍스트에 영향을 줄 수 있는 공격 시나리오를 검증했습니다. 기존에 수행해 온 클라이언트·임베디드·커널 연구에서 한 단계 확장해, 엔터프라이즈 서버 및 SaaS 인접 영역으로 분석 범위를 넓혀가는 단계의 연구입니다.
    </p>
    <div class="pf-project__tags">
      <span class="pf-tag">MS Exchange</span><span class="pf-tag">On-Premise</span><span class="pf-tag">Enterprise</span><span class="pf-tag">XSS</span><span class="pf-tag">1-day</span>
    </div>
  </div>

  <!-- ===== Windows Kernel LPE + LLM/MCP ===== -->
  <div class="pf-project" id="windows-lpe">
    <div class="pf-project__header">
      <h3 class="pf-project__name" data-en="🪟 Windows Kernel LPE & LLM/MCP Automation" data-ko="🪟 Windows Kernel LPE 및 LLM/MCP 자동화 연구">🪟 Windows Kernel LPE 및 LLM/MCP 자동화 연구</h3>
      <span class="pf-project__period">2025.04 ~ 2026.12</span>
    </div>
    <p class="pf-project__desc"
       data-en="Targeting older Windows builds, this work reproduces undisclosed 1-day PoCs and weaponizes them to full local privilege escalation. Patch diff extraction ranks changed functions by CWE / domain / pattern weight, and PoC drafting confirms the patched vulnerable function. A Race Condition PoC proved hard to reproduce, so a UAF primitive was used instead to construct an arbitrary write, then writing the system token into the current process token to escalate. A parallel research effort wraps this manual workflow in an LLM agent + MCP pipeline (IDA Headless, WinDbg, Hyper-V), staged as L0 reachability → L1 trigger extraction → L1.5 field-consumption tracking → L2 runtime breakpoint verification → L3 PoC BSOD reproduction. The agent automates trigger generation and Hyper-V snapshot rollback for repeated PoC runs; Claude-based and GPT Codex Security configurations are cross-validated. The pipeline has reproduced CVE-2024-38106 (Race Condition) and the unpublished CVE-2026-40407 (CLFS Heap Overflow) to user-mode BSOD, and discovered a new UAF BSOD in the Windows 11 (Build 26100) Object Manager namespace-root path — submitted to MSRC with both attack and defensive patch code."
       data-ko="최신 Windows가 아닌 특정 과거 버전을 대상으로, 공개되지 않은 1-day PoC를 구현해 실제 권한 상승까지 Weaponizing하는 보안 연구를 진행했습니다. 패치 diff로 변경 함수를 추출하고 CWE·도메인·패턴 가중치로 후보를 랭킹화한 뒤, PoC를 제작해 패치가 적용된 취약 함수를 확인했습니다. PoC가 Race Condition 취약점이라 재현이 매우 어려웠기에 대신 UAF 취약점을 일으켜 Arbitrary write primitive를 구성한 뒤, 시스템 토큰을 현재 프로세스 토큰에 write하는 방식으로 권한 상승에 성공했습니다. 최근에는 이 수동 분석 과정을 LLM 에이전트·MCP 도구로 체계화하는 자동화 파이프라인 연구를 병행하고 있습니다. MSRC 패치 메타데이터와 Hyper-V 기반 patch before/after 바이너리를 수집하고, IDA Headless·WinDbg·Hyper-V를 MCP 도구로 연결해 정적 도달성(L0) → 트리거 조건 추출(L1) → 필드 소비 추적(L1.5) → 런타임 브레이크포인트 검증(L2) → PoC BSOD 재현(L3)까지 단계별 검증을 자동화했습니다. 커널 타겟 함수 도달 트리거 코드와 Hyper-V 스냅샷 복원을 통한 PoC 반복 실행 전 과정을 에이전트가 처리하며, 현재는 Claude로 구성한 파이프라인을 GPT Codex Security로 병행 검증해 LLM별 보안 분석 역량을 비교·갱신하고 있습니다. 이 파이프라인으로 공개 1-day인 CVE-2024-38106(Race Condition)과 미공개 취약점 CVE-2026-40407(CLFS Heap Overflow)을 user-mode BSOD까지 재현했고, 최신 Windows 11(Build 26100)의 Object Manager 네임스페이스 루트 처리 코드에서 UAF BSOD 결함을 발견해 공격 코드·방어 패치를 함께 제시하여 MSRC에 제보했습니다.">
    최신 Windows가 아닌 특정 과거 버전을 대상으로, 공개되지 않은 1-day PoC를 구현해 실제 권한 상승까지 Weaponizing하는 보안 연구를 진행했습니다. 패치 diff로 변경 함수를 추출하고 CWE·도메인·패턴 가중치로 후보를 랭킹화한 뒤, PoC를 제작해 패치가 적용된 취약 함수를 확인했습니다. PoC가 Race Condition 취약점이라 재현이 매우 어려웠기에 대신 UAF 취약점을 일으켜 Arbitrary write primitive를 구성한 뒤, 시스템 토큰을 현재 프로세스 토큰에 write하는 방식으로 권한 상승에 성공했습니다. 최근에는 이 수동 분석 과정을 LLM 에이전트·MCP 도구로 체계화하는 자동화 파이프라인 연구를 병행하고 있습니다. MSRC 패치 메타데이터와 Hyper-V 기반 patch before/after 바이너리를 수집하고, IDA Headless·WinDbg·Hyper-V를 MCP 도구로 연결해 정적 도달성(L0) → 트리거 조건 추출(L1) → 필드 소비 추적(L1.5) → 런타임 브레이크포인트 검증(L2) → PoC BSOD 재현(L3)까지 단계별 검증을 자동화했습니다. 커널 타겟 함수 도달 트리거 코드와 Hyper-V 스냅샷 복원을 통한 PoC 반복 실행 전 과정을 에이전트가 처리하며, 현재는 Claude로 구성한 파이프라인을 GPT Codex Security로 병행 검증해 LLM별 보안 분석 역량을 비교·갱신하고 있습니다. 이 파이프라인으로 공개 1-day인 CVE-2024-38106(Race Condition)과 미공개 취약점 CVE-2026-40407(CLFS Heap Overflow)을 user-mode BSOD까지 재현했고, 최신 Windows 11(Build 26100)의 Object Manager 네임스페이스 루트 처리 코드에서 UAF BSOD 결함을 발견해 공격 코드·방어 패치를 함께 제시하여 MSRC에 제보했습니다.
    </p>
    <div class="pf-project__tags">
      <span class="pf-tag">Windows Kernel</span><span class="pf-tag">LPE</span><span class="pf-tag">UAF</span><span class="pf-tag">Race Condition</span><span class="pf-tag">LLM Agent</span><span class="pf-tag">MCP</span><span class="pf-tag">IDA Headless</span><span class="pf-tag">WinDbg</span><span class="pf-tag">Hyper-V</span><span class="pf-tag">MSRC</span><span class="pf-tag">CVE-2024-38106</span><span class="pf-tag">CVE-2026-40407</span>
    </div>
  </div>

  <!-- ===== Android Kernel MTE ===== -->
  <div class="pf-project" id="android-mte">
    <div class="pf-project__header">
      <h3 class="pf-project__name" data-en="🤖 Android Kernel MTE Bypass Research" data-ko="🤖 Android Kernel MTE Bypass 연구">🤖 Android Kernel MTE Bypass 연구</h3>
      <span class="pf-project__period">2025.09 ~ 2026.02</span>
    </div>
    <p class="pf-project__desc"
       data-en="Modern Android kernels ship with MTE (Memory Tagging Extension), a hardware-assisted memory protection. This study evaluates how prior memory-corruption 1-days fare under MTE and explores bypass avenues. Most direct memory-corruption 1-days are blocked, but an indirect path through the modprobe_path primitive reliably bypasses MTE. The bypass was reproduced on a Pixel device with MTE enabled, ending in full root escalation. ROGuard — a defense designed to block the same class of bypass with minimal performance overhead — is proposed alongside the attack research, treating offense and defense as one effort."
       data-ko="최신 안드로이드 커널에는 MTE(Memory Tagging Extension)라는 메모리 보호 기법이 존재합니다. 본 연구는 MTE가 적용된 환경에서 과거 1-day 사례를 적용했을 때 공격 성공률이 얼마나 떨어지는지, 그리고 우회 가능성이 존재하는지를 다각도로 분석하기 위해 진행되었습니다. 대부분의 메모리 커럽션 1-day는 MTE에 의해 정상적으로 탐지·차단되었지만, modprobe_path라는 Primitive를 사용했을 때는 MTE를 우회할 수 있다는 방법론을 도출했습니다. 실제 Pixel 기기에 MTE를 적용한 상태에서 modprobe_path Primitive Exploit을 실행해 ROOT 권한 탈취를 재현했고, 동일한 우회 경로를 차단할 수 있는 방어 기법 ROGuard를 함께 제시했습니다. ROGuard는 제품 본연의 성능 저하를 최소화하면서 동일 클래스의 우회를 차단하도록 설계하였으며, 공격·방어를 한 연구 안에서 함께 다룬 점에 의미를 두고 있습니다.">
    최신 안드로이드 커널에는 MTE(Memory Tagging Extension)라는 메모리 보호 기법이 존재합니다. 본 연구는 MTE가 적용된 환경에서 과거 1-day 사례를 적용했을 때 공격 성공률이 얼마나 떨어지는지, 그리고 우회 가능성이 존재하는지를 다각도로 분석하기 위해 진행되었습니다. 대부분의 메모리 커럽션 1-day는 MTE에 의해 정상적으로 탐지·차단되었지만, modprobe_path라는 Primitive를 사용했을 때는 MTE를 우회할 수 있다는 방법론을 도출했습니다. 실제 Pixel 기기에 MTE를 적용한 상태에서 modprobe_path Primitive Exploit을 실행해 ROOT 권한 탈취를 재현했고, 동일한 우회 경로를 차단할 수 있는 방어 기법 ROGuard를 함께 제시했습니다. ROGuard는 제품 본연의 성능 저하를 최소화하면서 동일 클래스의 우회를 차단하도록 설계하였으며, 공격·방어를 한 연구 안에서 함께 다룬 점에 의미를 두고 있습니다.
    </p>
    <div class="pf-project__tags">
      <span class="pf-tag">Android Kernel</span><span class="pf-tag">MTE</span><span class="pf-tag">Bypass</span><span class="pf-tag">modprobe_path</span><span class="pf-tag">Pixel</span><span class="pf-tag">Root</span><span class="pf-tag">ROGuard</span>
    </div>
  </div>

  <!-- ===== Satellite OBC GMO ===== -->
  <div class="pf-project" id="gmo-ccsds">
    <span id="gmo-paper"></span>
    <div class="pf-project__header">
      <h3 class="pf-project__name" data-en="🛰️ Satellite OBC Security Tooling (GMO IERAE)" data-ko="🛰️ 위성 OBC 보안 도구 개발 (GMO IERAE)">🛰️ 위성 OBC 보안 도구 개발 (GMO IERAE)</h3>
      <span class="pf-project__period">2025.07 ~ 2026.03</span>
    </div>
    <p class="pf-project__desc"
       data-en="An MOU-based collaboration with GMO Internet (Japan) brought a one-month embedded engagement at the GMO Shibuya office, focused on satellite security research for international conference booths and SCI journal output. Real GomSpace and EnduroSat OBC (On-Board Computer) boards were purchased; an in-SDK security proxy tool was developed and flashed to firmware. Internally, plausible attack scenarios against satellite ground stations and matching defenses were designed end-to-end. The defense layer is a CCSDS (Consultative Committee for Space Data Systems)-protocol-based firewall that filters malicious / tampered packets on uplink and downlink paths. The work was authored as &quot;CCSDS based Firewall for Modern Satellite System&quot; and submitted to Computers &amp; Security (SCI), then live-demoed at DEFCON 33 Las Vegas and Bahrain Aerospace Village in 2025."
       data-ko="석사 과정 중 일본 기업 GMO Internet과 MOU 협약을 맺고, 도쿄 시부야 GMO Internet 사옥에서 약 1개월간 단기 근무하며 위성 보안 연구를 수행했습니다. 본 연구의 핵심 목표는 DEFCON 33, CodeBlue 등 국제 컨퍼런스 부스에서 발표할 인공위성 보안 데모와 SCI 논문을 준비하는 것이었습니다. GomSpace와 EnduroSat OBC(위성 온보드 컴퓨터) 보드를 직접 구매해, SDK 내에서 보안을 점검할 수 있는 Proxy 도구를 개발하고 펌웨어에 플래싱하는 작업을 수행했습니다. 내부 개발 코드로는 실제로 발생 가능한 지상국 보안 공격 시나리오와, 이에 대응할 수 있는 방어 시스템을 함께 구축했습니다. 방어 측면에서는 CCSDS(우주데이터시스템자문위원회) 프로토콜 기반 Firewall을 설계해, 위성 uplink·downlink 경로 상에서 악성·변조 패킷을 차단할 수 있도록 했습니다. 본 연구 결과를 토대로 &quot;CCSDS based Firewall for Modern Satellite System&quot; 주제의 SCI 논문(Computers &amp; Security)을 작성하였고, 2025년 DEFCON 33 Las Vegas와 Bahrain Aerospace Village 두 곳에서 위성 보안 시스템 시연 및 발표를 성공적으로 진행했습니다.">
    석사 과정 중 일본 기업 GMO Internet과 MOU 협약을 맺고, 도쿄 시부야 GMO Internet 사옥에서 약 1개월간 단기 근무하며 위성 보안 연구를 수행했습니다. 본 연구의 핵심 목표는 DEFCON 33, CodeBlue 등 국제 컨퍼런스 부스에서 발표할 인공위성 보안 데모와 SCI 논문을 준비하는 것이었습니다. GomSpace와 EnduroSat OBC(위성 온보드 컴퓨터) 보드를 직접 구매해, SDK 내에서 보안을 점검할 수 있는 Proxy 도구를 개발하고 펌웨어에 플래싱하는 작업을 수행했습니다. 내부 개발 코드로는 실제로 발생 가능한 지상국 보안 공격 시나리오와, 이에 대응할 수 있는 방어 시스템을 함께 구축했습니다. 방어 측면에서는 CCSDS(우주데이터시스템자문위원회) 프로토콜 기반 Firewall을 설계해, 위성 uplink·downlink 경로 상에서 악성·변조 패킷을 차단할 수 있도록 했습니다. 본 연구 결과를 토대로 "CCSDS based Firewall for Modern Satellite System" 주제의 SCI 논문(Computers &amp; Security)을 작성하였고, 2025년 DEFCON 33 Las Vegas와 Bahrain Aerospace Village 두 곳에서 위성 보안 시스템 시연 및 발표를 성공적으로 진행했습니다.
    </p>
    <div class="pf-project__tags">
      <span class="pf-tag">GMO IERAE</span><span class="pf-tag">GomSpace</span><span class="pf-tag">EnduroSat</span><span class="pf-tag">OBC</span><span class="pf-tag">CCSDS</span><span class="pf-tag">Firewall</span><span class="pf-tag">DEFCON 33</span><span class="pf-tag">SCI</span><span class="pf-tag">Computers &amp; Security</span>
    </div>
  </div>

  <!-- ===== Satellite Signal & Commercial GS ===== -->
  <div class="pf-project" id="satellite-rx">
    <div class="pf-project__header">
      <h3 class="pf-project__name" data-en="📡 Satellite Signal Reception & Commercial Ground Station Security" data-ko="📡 인공위성 신호 수신 및 상용 지상국 보안 연구">📡 인공위성 신호 수신 및 상용 지상국 보안 연구</h3>
      <span class="pf-project__period">2025.03 ~ 2025.12</span>
    </div>
    <p class="pf-project__desc"
       data-en="As the space industry scales, satellite and ground-station security have become front-line research domains. Under an MOU with a commercial ground-station operator, this work approaches security from two angles. First, real-world RF reception: a USRP-based SDR, GNU Radio toolchain, and dedicated antennas were built from scratch to receive and demodulate live X- and S-band satellite signals, successfully decoding select Earth-observation imagery. Second, a deep structural analysis of the operator's production ground-station systems surfaced exploitable weaknesses; the resulting chain achieved a foothold on a production server and full filesystem access. Together the two tracks demonstrate the attack surface across the full RF-to-infrastructure chain of a commercial satellite link."
       data-ko="우주 산업이 가속화됨에 따라 인공위성 및 지상국 보안 연구의 가치가 점점 더 중요해지고 있습니다. 본 연구는 실제 상용 지상국 서비스를 운영하는 기업과 MOU 협업을 통해 진행되었고, 두 가지 관점에서 보안성을 점검했습니다. 첫째, 실제 인공위성으로부터 송신되는 RF 신호를 수신·복호화하는 연구를 수행했습니다. SDR(USRP), GNU Radio, 전용 안테나를 직접 구축해 X-band와 S-band 위성 신호를 실제로 수신·복조했고, 그중 일부 지구 관측 이미지를 성공적으로 디코딩해 원본 영상을 복원할 수 있었습니다. 둘째, 실제 운영 중인 상용 지상국 시스템의 구조를 분석하고 취약 구조를 식별하는 연구를 진행했습니다. 분석 결과 도출된 취약점을 통해 운영 중인 서버에 침투하는 데 성공했고, 시스템 전체 파일 시스템에 접근할 수 있는 단계까지 도달했습니다. 두 트랙을 결합해 RF 단부터 운영 인프라까지 위성-지상국 통신 사슬 전반의 attack surface를 입증한 사례입니다.">
    우주 산업이 가속화됨에 따라 인공위성 및 지상국 보안 연구의 가치가 점점 더 중요해지고 있습니다. 본 연구는 실제 상용 지상국 서비스를 운영하는 기업과 MOU 협업을 통해 진행되었고, 두 가지 관점에서 보안성을 점검했습니다. 첫째, 실제 인공위성으로부터 송신되는 RF 신호를 수신·복호화하는 연구를 수행했습니다. SDR(USRP), GNU Radio, 전용 안테나를 직접 구축해 X-band와 S-band 위성 신호를 실제로 수신·복조했고, 그중 일부 지구 관측 이미지를 성공적으로 디코딩해 원본 영상을 복원할 수 있었습니다. 둘째, 실제 운영 중인 상용 지상국 시스템의 구조를 분석하고 취약 구조를 식별하는 연구를 진행했습니다. 분석 결과 도출된 취약점을 통해 운영 중인 서버에 침투하는 데 성공했고, 시스템 전체 파일 시스템에 접근할 수 있는 단계까지 도달했습니다. 두 트랙을 결합해 RF 단부터 운영 인프라까지 위성-지상국 통신 사슬 전반의 attack surface를 입증한 사례입니다.
    </p>
    <div class="pf-project__tags">
      <span class="pf-tag">Satellite</span><span class="pf-tag">Ground Station</span><span class="pf-tag">SDR</span><span class="pf-tag">USRP</span><span class="pf-tag">GNU Radio</span><span class="pf-tag">X-band</span><span class="pf-tag">S-band</span><span class="pf-tag">Earth Observation</span><span class="pf-tag">Commercial</span><span class="pf-tag">MOU</span>
    </div>
  </div>

  <!-- ===== Drone (DJI/PX4) ===== -->
  <div class="pf-project" id="drone-security">
    <div class="pf-project__header">
      <h3 class="pf-project__name" data-en="🛩️ Drone (DJI / PX4) Vulnerability Analysis" data-ko="🛩️ 상용 드론 (DJI / PX4) 보안 연구">🛩️ 상용 드론 (DJI / PX4) 보안 연구</h3>
      <span class="pf-project__period">2024.03 ~ 2024.12</span>
    </div>
    <p class="pf-project__desc"
       data-en="A research effort targeting popular Chinese consumer drones, focused on hijacking RC joystick control. Real drone RF traffic was captured, a constrained replay tool was built, and unauthenticated Takeoff / Landing commands were executed without the original controller. Newer drones with added security were then analyzed deeper at the RF protocol level; a low-entropy weakness allowed brute-force recovery of the encryption key. Decrypting the link revealed the custom DUML packet format, after which arbitrary joystick commands could be replayed past authentication / sequence guards, completing a full drone-disable scenario. The work spans RF capture, firmware reversing, crypto-key inference, protocol parsing, and end-to-end weaponization on an embedded wireless target."
       data-ko="중국 유명 상용 드론을 대상으로, RC 조이스틱 제어권을 탈취할 수 있는지에 초점을 맞춘 보안 연구를 진행했습니다. 실제 드론 RF 신호를 수집한 뒤, 일부 상황에서 패킷을 replay할 수 있는 도구를 직접 제작했고, 조종기 없이 Takeoff·Landing 명령을 실행하는 데 성공했습니다. 이후 보안 기능이 추가된 상위 버전 드론을 대상으로 RF 프로토콜을 더 자세히 분석했고, 그 과정에서 entropy를 낮춰 암호화 키를 유추할 수 있는 Bruteforce 취약점을 발견했습니다. 해당 취약점을 통해 커스텀 DUML 프로토콜의 패킷 형식을 알아낼 수 있었고, 인증·시퀀스 등의 제한 상황을 우회해 조이스틱 명령을 임의로 실행함으로써 드론을 무력화하는 시나리오까지 재현했습니다. RF 수집·분석부터 펌웨어 리버스, 암호 키 추정, 프로토콜 해독, 최종 무력화까지 전 과정을 직접 다룬 임베디드 무선 보안 연구 사례입니다.">
    중국 유명 상용 드론을 대상으로, RC 조이스틱 제어권을 탈취할 수 있는지에 초점을 맞춘 보안 연구를 진행했습니다. 실제 드론 RF 신호를 수집한 뒤, 일부 상황에서 패킷을 replay할 수 있는 도구를 직접 제작했고, 조종기 없이 Takeoff·Landing 명령을 실행하는 데 성공했습니다. 이후 보안 기능이 추가된 상위 버전 드론을 대상으로 RF 프로토콜을 더 자세히 분석했고, 그 과정에서 entropy를 낮춰 암호화 키를 유추할 수 있는 Bruteforce 취약점을 발견했습니다. 해당 취약점을 통해 커스텀 DUML 프로토콜의 패킷 형식을 알아낼 수 있었고, 인증·시퀀스 등의 제한 상황을 우회해 조이스틱 명령을 임의로 실행함으로써 드론을 무력화하는 시나리오까지 재현했습니다. RF 수집·분석부터 펌웨어 리버스, 암호 키 추정, 프로토콜 해독, 최종 무력화까지 전 과정을 직접 다룬 임베디드 무선 보안 연구 사례입니다.
    </p>
    <div class="pf-project__tags">
      <span class="pf-tag">DJI</span><span class="pf-tag">PX4</span><span class="pf-tag">Drone</span><span class="pf-tag">RF</span><span class="pf-tag">Replay</span><span class="pf-tag">Bruteforce</span><span class="pf-tag">DUML</span><span class="pf-tag">Embedded</span><span class="pf-tag">Firmware</span>
    </div>
  </div>

  <!-- ===== Commercial Radio RF ===== -->
  <div class="pf-project" id="radio-rf">
    <div class="pf-project__header">
      <h3 class="pf-project__name" data-en="📻 Commercial Radio RF Security Research" data-ko="📻 상용 무전기 RF 보안 연구">📻 상용 무전기 RF 보안 연구</h3>
      <span class="pf-project__period">2025.03 ~ 2025.12</span>
    </div>
    <p class="pf-project__desc"
       data-en="A research effort targeting commercial walkie-talkie radios — capturing RF, extracting firmware, and statically + dynamically analyzing the on-device voice decryption pipeline. A low-entropy weakness enabled brute-force recovery of the encryption key. An Oracle-style helper tool was built to boost voice-recovery probability under noisy / lossy RF conditions, meaningfully improving recovery rates. The work extends the same analysis pattern proven on drones and satellite ground stations into the radio domain."
       data-ko="유명 상용 무전기를 대상으로 RF 신호를 수집해, 실제 음성으로 복호화하는 보안 연구를 진행했습니다. 무전기 펌웨어를 추출해 RF 신호 복호화 과정을 정적·동적으로 분석했고, 그 과정에서 entropy를 낮춰 암호화 키를 유추할 수 있는 Bruteforce 취약점을 발견했습니다. 또한 RF 신호 음성 복호화 성공률을 끌어올리기 위한 Oracle 도구를 제작해, 잡음·손실이 있는 신호 환경에서도 음성 신호 복구 확률을 의미 있게 높이는 데 성공했습니다. 무전기·드론·위성 등 다양한 RF 기반 임베디드 시스템에서 공통적으로 적용 가능한 분석 패턴을 확장한 사례입니다.">
    유명 상용 무전기를 대상으로 RF 신호를 수집해, 실제 음성으로 복호화하는 보안 연구를 진행했습니다. 무전기 펌웨어를 추출해 RF 신호 복호화 과정을 정적·동적으로 분석했고, 그 과정에서 entropy를 낮춰 암호화 키를 유추할 수 있는 Bruteforce 취약점을 발견했습니다. 또한 RF 신호 음성 복호화 성공률을 끌어올리기 위한 Oracle 도구를 제작해, 잡음·손실이 있는 신호 환경에서도 음성 신호 복구 확률을 의미 있게 높이는 데 성공했습니다. 무전기·드론·위성 등 다양한 RF 기반 임베디드 시스템에서 공통적으로 적용 가능한 분석 패턴을 확장한 사례입니다.
    </p>
    <div class="pf-project__tags">
      <span class="pf-tag">Radio</span><span class="pf-tag">RF</span><span class="pf-tag">SDR</span><span class="pf-tag">Firmware</span><span class="pf-tag">Bruteforce</span><span class="pf-tag">Entropy</span><span class="pf-tag">Voice Decryption</span><span class="pf-tag">Oracle</span>
    </div>
  </div>

  <!-- ===== Open-Source Ground Station (TinyGS) ===== -->
  <div class="pf-project" id="ground-station">
    <div class="pf-project__header">
      <h3 class="pf-project__name" data-en="📡 Open-Source Ground Station (TinyGS) Security Research" data-ko="📡 오픈소스 지상국 (TinyGS) 보안 연구">📡 오픈소스 지상국 (TinyGS) 보안 연구</h3>
      <span class="pf-project__period">2024.03 ~ 2024.12</span>
    </div>
    <p class="pf-project__desc"
       data-en="Before scaling up to a commercial ground-station engagement, this research targeted TinyGS — an ESP32-based open-source satellite ground station with roughly 8,500 active users — across three attack surfaces. First, RF eavesdropping: three ESP32 ground stations were built, brought online via Telegram / MQTT AP-mode setup, and used to receive LoRa satellite packets; a Mosquitto-based spoofing MQTT server injected during setup mirrored every received satellite packet, completing the eavesdrop flow. Second, malicious-RF injection: a GNU Radio + LoRa TX stack was developed and packaged onto a ~1kg portable rig (Raspberry Pi 4 + USRP B205mini + amplifier + antenna), and tampered packets were accepted by the ground station as legitimate. Third, over-the-air RF fuzzing: a Python fuzzer with a Radamsa mutator, seeded from TM/TC packets crawled from TinyGS's Last Packets page, looped via MQTT against the unmodifiable black-box ground station — yielding 3 vulnerabilities (1 Heap Overflow + 2 DoS). The work was published at CISC as &quot;Vulnerability Research on Open-Source Ground Station Systems via Satellite RF Signal Generation.&quot;"
       data-ko="실제 상용 지상국 연구를 본격적으로 진행하기 전에, 사용자 약 8,500명 규모의 오픈소스 인공위성 지상국 TinyGS(ESP32 기반)를 먼저 타깃으로 보안 연구를 수행했습니다. 공격 표면은 RF 도청, 변조 악성 데이터 RF 송신, 펌웨어 자동화 공격(RF Fuzzing)의 세 갈래로 분석했습니다. 첫째, RF 도청 시나리오는 ESP32 지상국 3대를 직접 구축하고 Telegram·MQTT 설정을 통해 Access Point 모드로 셋업한 뒤 LoRa 위성 패킷을 수신하는 구조로 검증했습니다. Mosquitto 기반 MQTT 스푸핑 서버를 제작해 지상국 설정 단계의 MQTT 정보에 삽입함으로써, 위성이 송신한 패킷이 스푸핑 서버에서 그대로 확인되는 도청 흐름을 구현했습니다. 둘째, 변조 악성 데이터 RF 공격은 GNU Radio 송신 코드(SDR)와 LoRa 기반 TX를 개발하고, 라즈베리파이4·USRP B205mini·앰프·안테나를 결합해 약 1kg 규모의 휴대형 송신 장비를 직접 구성했습니다. 송수신 검증을 거쳐 조작된 패킷을 지상국이 정상 패킷으로 인식하도록 만들었습니다. 셋째, 펌웨어 자동화 공격은 Python 기반 Fuzzer 서버에 Radamsa 뮤테이터를 연동하고, TinyGS 웹사이트의 Last Packets를 크롤링해 실제 TM/TC 패킷을 시드로 수집·변이했습니다. 코드 수정이 불가한 블랙박스 지상국을 MQTT로 연결한 Over-the-Air RF Fuzzing 자동화를 구축했고, 그 결과 Heap Overflow 1건과 DoS 2건을 포함해 총 3건의 취약점을 발견했습니다. 본 연구는 정보보호학회에 &quot;인공위성 RF 신호 생성을 통한 오픈소스 지상국 시스템 취약점 연구&quot;로 게재·발표했습니다.">
    실제 상용 지상국 연구를 본격적으로 진행하기 전에, 사용자 약 8,500명 규모의 오픈소스 인공위성 지상국 TinyGS(ESP32 기반)를 먼저 타깃으로 보안 연구를 수행했습니다. 공격 표면은 RF 도청, 변조 악성 데이터 RF 송신, 펌웨어 자동화 공격(RF Fuzzing)의 세 갈래로 분석했습니다. 첫째, RF 도청 시나리오는 ESP32 지상국 3대를 직접 구축하고 Telegram·MQTT 설정을 통해 Access Point 모드로 셋업한 뒤 LoRa 위성 패킷을 수신하는 구조로 검증했습니다. Mosquitto 기반 MQTT 스푸핑 서버를 제작해 지상국 설정 단계의 MQTT 정보에 삽입함으로써, 위성이 송신한 패킷이 스푸핑 서버에서 그대로 확인되는 도청 흐름을 구현했습니다. 둘째, 변조 악성 데이터 RF 공격은 GNU Radio 송신 코드(SDR)와 LoRa 기반 TX를 개발하고, 라즈베리파이4·USRP B205mini·앰프·안테나를 결합해 약 1kg 규모의 휴대형 송신 장비를 직접 구성했습니다. 송수신 검증을 거쳐 조작된 패킷을 지상국이 정상 패킷으로 인식하도록 만들었습니다. 셋째, 펌웨어 자동화 공격은 Python 기반 Fuzzer 서버에 Radamsa 뮤테이터를 연동하고, TinyGS 웹사이트의 Last Packets를 크롤링해 실제 TM/TC 패킷을 시드로 수집·변이했습니다. 코드 수정이 불가한 블랙박스 지상국을 MQTT로 연결한 Over-the-Air RF Fuzzing 자동화를 구축했고, 그 결과 Heap Overflow 1건과 DoS 2건을 포함해 총 3건의 취약점을 발견했습니다. 본 연구는 정보보호학회에 "인공위성 RF 신호 생성을 통한 오픈소스 지상국 시스템 취약점 연구"로 게재·발표했습니다.
    </p>
    <div class="pf-project__tags">
      <span class="pf-tag">TinyGS</span><span class="pf-tag">ESP32</span><span class="pf-tag">LoRa</span><span class="pf-tag">SDR</span><span class="pf-tag">GNU Radio</span><span class="pf-tag">USRP</span><span class="pf-tag">MQTT</span><span class="pf-tag">Radamsa</span><span class="pf-tag">OTA Fuzzing</span><span class="pf-tag">Heap Overflow</span><span class="pf-tag">CISC</span>
    </div>
  </div>

  <!-- ===== HAYYIM SECURITY ===== -->
  <div class="pf-project" id="hayyim">
    <div class="pf-project__header">
      <h3 class="pf-project__name" data-en="🐛 HAYYIM SECURITY — Software Vulnerability Research" data-ko="🐛 HAYYIM SECURITY — 상용 소프트웨어 취약점 연구">🐛 HAYYIM SECURITY — 상용 소프트웨어 취약점 연구</h3>
      <span class="pf-project__period">2022.03 ~ 2023.12</span>
    </div>
    <span id="hayyim-office"></span><span id="hayyim-antivirus"></span><span id="hayyim-browser"></span><span id="hayyim-rdp"></span>
    <p class="pf-project__desc"
       data-en="At HAYYIM SECURITY, vulnerability research and exploit development were performed across commercial software targets: MS Office, Web Browser, Antivirus, and RDP. Common workflow starts by mapping each program's internals and identifying user-input attack surfaces, then studying prior 1-day patch diffs to learn the bug-class taxonomy. Dynamic analysis via debugger plus static analysis on decompiled code surfaces size overflows, UAF, race conditions; for large codebases, open-source fuzzers are attached via custom harnesses for automated fuzzing combined with concurrent code auditing.<br><br><strong>Office (MS Office)</strong> — research focused on the dynamic-linked code path that parses Excel data, one of Office's primary input vectors. Given Office's massive codebase, a WinAFL-based fuzzer was attached via a custom harness, combining automated fuzzing with code auditing. A DoS-class size-manipulation bug was discovered: crafted OLE file extract data tricks the parser into following bad length values, causing invalid memory access. The condition triggers as a single-click user-interaction scenario — opening a malicious Excel file is sufficient.<br><br><strong>Antivirus</strong> — AV products auto-scan files that the user never explicitly executes, so the scan logic itself runs in a SYSTEM-privileged context. While scanning extracted OLE files, the decompression staged its output into a globally-writable TEMP path. Since that path is writable by low-privilege users, a Hard Link (or other symlink-class) primitive at that path lets system-privileged AV operations modify arbitrary target files. The chain becomes a clean Local Privilege Escalation primitive — an authenticated low-priv user can reach SYSTEM code execution merely by triggering the AV's autoscan flow.<br><br><strong>Web Browser</strong> — browsers expose one of the broadest input surfaces in commodity software (renderer, IPC, JS engine, image parsers). This work focused primarily on libangle — the renderer's graphics layer — tracing external-input code paths through static and dynamic analysis with an emphasis on heap-overflow conditions. 1-day patch diffs were studied in parallel to learn bug-class patterns and surface new candidate targets.<br><br><strong>RDP</strong> — research targeted an open-source RDP implementation, focused on whether a malicious server could trigger client-side RCE by manipulating its responses during the client → server handshake init. RDP's network-reachable attack surface gives it high RCE potential; this work specifically traced the handshake-handling code path that a legitimate client follows when connecting to a hostile server. Combined static analysis on decompiled code and dynamic debugger work surfaced patterns where untrusted server-supplied data influenced client-side memory state during the handshake."
       data-ko="하임시큐리티에서 MS Office, Web Browser, 백신(Antivirus), RDP 등 상용 소프트웨어를 대상으로 취약점 연구·익스플로잇 개발을 수행했습니다. 공통 분석 워크플로우는 우선 모든 소프트웨어의 상세 동작 과정을 파악하고, 사용자 입력을 받을 수 있는 attack surface를 조사하는 것에서 시작합니다. 이전 버전에서 발생한 1-day를 분석해 어떤 종류의 bug case가 발생하는지 함께 정리한 뒤, 디버거를 통해 사용자 입력을 주입하는 동적 분석과 디컴파일된 코드를 추적하는 정적 분석을 병행해 size Overflow, UAF, Race Condition 등 취약점을 도출합니다. 코드 규모가 큰 타깃에는 공개 Fuzzer를 활용해 취약 함수에 attach하는 Harness를 직접 작성하고, fuzzing 자동화와 코드 오디팅을 함께 진행했습니다.<br><br><strong>Office (MS Office)</strong> — MS Office의 주요 입력 벡터 중 Excel 데이터를 Parsing하는 Dynamic linking code 단을 연구 타깃으로 지정해 분석을 진행했습니다. Office는 코드 규모가 매우 방대해 정적·동적 분석만으로는 한계가 있어, WinAFL 기반 Fuzzer에 attach하는 Harness를 직접 작성해 fuzzing 자동화와 코드 오디팅을 병행했습니다. 분석 결과 Excel OLE File Extract data를 변경해 size를 조작하면, parser가 잘못된 길이 정보를 따라가며 비정상 메모리 접근을 일으키는 DoS 단 취약점 케이스를 발견했습니다. 해당 취약점은 사용자가 악성 Excel 파일을 열기만 해도 트리거되는 user-interaction 1-click 시나리오로 검증되었습니다.<br><br><strong>Antivirus (백신)</strong> — 백신은 사용자가 직접 실행하지 않은 파일도 자동으로 검사하기 때문에, 검사 로직 자체가 SYSTEM 권한 컨텍스트에서 동작한다는 특성이 있습니다. 본 연구에서는 백신이 추출된 OLE File을 검사할 때, 압축 해제 과정에서 Full Access가 가능한 일반 TEMP 경로로 압축을 해제하는 취약점을 발견했습니다. 해당 경로는 권한이 낮은 일반 사용자도 쓰기·조작이 가능한데, 공격자가 해당 경로에 Hard Link 등 심볼릭 링크 관련 기능을 사용하면 SYSTEM 권한이 경로 상의 임의 파일을 직접 수정할 수 있게 됩니다. 이 패턴은 곧바로 Local Privilege Escalation(권한 상승)으로 이어질 수 있으며, 인증된 일반 사용자가 백신의 자동 검사 동작만 트리거해도 SYSTEM 권한 코드 실행이 가능한 시나리오를 검증했습니다.<br><br><strong>Web Browser</strong> — 브라우저는 렌더러·IPC·JS 엔진·이미지 파서 등 사용자 입력이 도달하는 surface가 가장 넓은 타깃 중 하나입니다. 본 연구에서는 주로 렌더러 단의 그래픽 처리를 담당하는 libangle 모듈을 타깃으로, 외부 입력이 도달하는 코드 경로를 정적·동적 분석으로 추적하며 heap overflow 취약점을 집중적으로 조사했습니다. 패치 전·후 코드 비교(1-day diff)를 통해 bug case가 어떤 패턴으로 발생하는지 학습하며 신규 취약점 후보를 발굴했습니다.<br><br><strong>RDP</strong> — 오픈소스 RDP 구현체를 대상으로, client → server handshake init 단계에서 서버 응답 데이터를 조작해 client 측 RCE를 유도할 수 있는지를 중심으로 연구를 진행했습니다. RDP는 원격 데스크톱 프로토콜 특성상 네트워크 단에서 직접 도달 가능한 attack surface가 광범위해 RCE 잠재력이 큰 타깃이며, 본 연구에서는 특히 악성 서버에 접속한 정상 client의 handshake 처리 코드 경로를 추적했습니다. 디컴파일된 코드 정적 분석과 디버거 동적 분석을 병행해, 핸드셰이크 단에서 신뢰되지 않은 서버 데이터가 client 메모리 구조에 영향을 주는 취약 패턴을 식별했습니다.">
    하임시큐리티에서 MS Office, Web Browser, 백신(Antivirus), RDP 등 상용 소프트웨어를 대상으로 취약점 연구·익스플로잇 개발을 수행했습니다. 공통 분석 워크플로우는 우선 모든 소프트웨어의 상세 동작 과정을 파악하고, 사용자 입력을 받을 수 있는 attack surface를 조사하는 것에서 시작합니다. 이전 버전에서 발생한 1-day를 분석해 어떤 종류의 bug case가 발생하는지 함께 정리한 뒤, 디버거를 통해 사용자 입력을 주입하는 동적 분석과 디컴파일된 코드를 추적하는 정적 분석을 병행해 size Overflow, UAF, Race Condition 등 취약점을 도출합니다. 코드 규모가 큰 타깃에는 공개 Fuzzer를 활용해 취약 함수에 attach하는 Harness를 직접 작성하고, fuzzing 자동화와 코드 오디팅을 함께 진행했습니다.<br><br><strong>Office (MS Office)</strong> — MS Office의 주요 입력 벡터 중 Excel 데이터를 Parsing하는 Dynamic linking code 단을 연구 타깃으로 지정해 분석을 진행했습니다. Office는 코드 규모가 매우 방대해 정적·동적 분석만으로는 한계가 있어, WinAFL 기반 Fuzzer에 attach하는 Harness를 직접 작성해 fuzzing 자동화와 코드 오디팅을 병행했습니다. 분석 결과 Excel OLE File Extract data를 변경해 size를 조작하면, parser가 잘못된 길이 정보를 따라가며 비정상 메모리 접근을 일으키는 DoS 단 취약점 케이스를 발견했습니다. 해당 취약점은 사용자가 악성 Excel 파일을 열기만 해도 트리거되는 user-interaction 1-click 시나리오로 검증되었습니다.<br><br><strong>Antivirus (백신)</strong> — 백신은 사용자가 직접 실행하지 않은 파일도 자동으로 검사하기 때문에, 검사 로직 자체가 SYSTEM 권한 컨텍스트에서 동작한다는 특성이 있습니다. 본 연구에서는 백신이 추출된 OLE File을 검사할 때, 압축 해제 과정에서 Full Access가 가능한 일반 TEMP 경로로 압축을 해제하는 취약점을 발견했습니다. 해당 경로는 권한이 낮은 일반 사용자도 쓰기·조작이 가능한데, 공격자가 해당 경로에 Hard Link 등 심볼릭 링크 관련 기능을 사용하면 SYSTEM 권한이 경로 상의 임의 파일을 직접 수정할 수 있게 됩니다. 이 패턴은 곧바로 Local Privilege Escalation(권한 상승)으로 이어질 수 있으며, 인증된 일반 사용자가 백신의 자동 검사 동작만 트리거해도 SYSTEM 권한 코드 실행이 가능한 시나리오를 검증했습니다.<br><br><strong>Web Browser</strong> — 브라우저는 렌더러·IPC·JS 엔진·이미지 파서 등 사용자 입력이 도달하는 surface가 가장 넓은 타깃 중 하나입니다. 본 연구에서는 주로 렌더러 단의 그래픽 처리를 담당하는 libangle 모듈을 타깃으로, 외부 입력이 도달하는 코드 경로를 정적·동적 분석으로 추적하며 heap overflow 취약점을 집중적으로 조사했습니다. 패치 전·후 코드 비교(1-day diff)를 통해 bug case가 어떤 패턴으로 발생하는지 학습하며 신규 취약점 후보를 발굴했습니다.<br><br><strong>RDP</strong> — 오픈소스 RDP 구현체를 대상으로, client → server handshake init 단계에서 서버 응답 데이터를 조작해 client 측 RCE를 유도할 수 있는지를 중심으로 연구를 진행했습니다. RDP는 원격 데스크톱 프로토콜 특성상 네트워크 단에서 직접 도달 가능한 attack surface가 광범위해 RCE 잠재력이 큰 타깃이며, 본 연구에서는 특히 악성 서버에 접속한 정상 client의 handshake 처리 코드 경로를 추적했습니다. 디컴파일된 코드 정적 분석과 디버거 동적 분석을 병행해, 핸드셰이크 단에서 신뢰되지 않은 서버 데이터가 client 메모리 구조에 영향을 주는 취약 패턴을 식별했습니다.
    </p>
    <div class="pf-project__tags">
      <span class="pf-tag">MS Office</span><span class="pf-tag">Browser</span><span class="pf-tag">Antivirus</span><span class="pf-tag">RDP</span><span class="pf-tag">WinAFL</span><span class="pf-tag">Harness</span><span class="pf-tag">OLE</span><span class="pf-tag">Hard Link</span><span class="pf-tag">LPE</span><span class="pf-tag">KISA</span><span class="pf-tag">KVE</span>
    </div>
  </div>

</div>

</div><!-- end #portfolio-content -->

<div class="about">
<div class="about__divider">*****</div>
<div class="about__text"><strong>Contact: ogj0824@gmail.com</strong></div>
</div>
