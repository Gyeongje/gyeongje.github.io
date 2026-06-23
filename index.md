---
layout: default
title: Gyeongje Oh
---

<div class="cv-wrapper">

<div class="cv-header">
  <h1 class="cv-name"><a href="{{ '/' | prepend: site.baseurl }}" class="cv-name__link">Gyeongje Oh</a></h1>
  <p class="cv-title">Offensive Security Researcher</p>
  <div class="cv-contact">
    <a href="mailto:ogj0824@gmail.com"><i class="fa fa-envelope"></i> ogj0824@gmail.com</a>
    <a href="https://github.com/Gyeongje" target="_blank"><i class="fa fa-github"></i> github.com/Gyeongje</a>
    <a href="https://www.linkedin.com/in/gyeongjeoh/" target="_blank"><i class="fa fa-linkedin-square"></i> linkedin.com/in/gyeongjeoh</a>
  </div>
  <div class="cv-actions">
    <a href="#" class="cv-download" onclick="generatePDF(); return false;">Download CV</a>
    <a href="#" class="cv-download" onclick="generateFullPDF(); return false;">Full Download</a>
  </div>
</div>

<div id="cv-content">

<!-- ==================== WORK EXPERIENCE ==================== -->
<section class="cv-section">
  <h2 class="cv-section__title" data-en="Work Experience" data-ko="경력">Work Experience</h2>

  <div class="cv-role">
    <div class="cv-role__head">
      <strong class="cv-role__company">HAYYIM SECURITY</strong>
      <span class="cv-role__title">Security Researcher</span>
      <span class="cv-role__date">2022.03 – 2023.12</span>
    </div>
    <ul class="cv-role__bullets">
      <li>Vulnerability research and exploit development across Browser, Office, VM, and RDP attack surfaces on Windows.</li>
      <li>Built WinAFL-based fuzzing harnesses for commercial document parsers; surfaced heap-overflow and OOB-write primitives.</li>
      <li>Disclosed two RCEs to KISA Bug Bounty — <strong>KVE-2023-0095</strong>, <strong>KVE-2023-5125</strong> ($3,100).</li>
      <li><em>(추가 디테일 자리 — 본인이 owned했던 컴포넌트 / 산출물 / 협업)</em></li>
    </ul>
  </div>
</section>

<!-- ==================== RESEARCH ==================== -->
<section class="cv-section">
  <h2 class="cv-section__title" data-en="Research" data-ko="연구">Research</h2>

  <div class="cv-role">
    <div class="cv-role__head">
      <strong class="cv-role__company">PWNLAB — Kyung Hee University</strong>
      <span class="cv-role__title">M.S. Candidate · Lab Leader</span>
      <span class="cv-role__date">2025.03 – Current</span>
    </div>
    <p class="cv-role__sub">Advisor: <a href="https://pwnlab.kr/downloads/cv.pdf" target="_blank">Prof. Daehee Jang</a></p>
    <ul class="cv-research-list">
      <li>
        <span class="cv-research-text">macOS kernel Bluetooth chipset firmware analysis and mitigation bypass research.</span>
        <span class="cv-research-meta">2026.02 – 11 · <a href="{{ '/portfolio/#macos-bt' | prepend: site.baseurl }}">Details →</a></span>
      </li>
      <li>
        <span class="cv-research-text">Satellite OBC security audit tooling for GomSpace / EnduroSat in collaboration with GMO IERAE.</span>
        <span class="cv-research-meta">2025.07 – 2026.03 · <a href="{{ '/portfolio/#satellite-obc' | prepend: site.baseurl }}">Details →</a></span>
      </li>
      <li>
        <span class="cv-research-text">Open-source ground station vulnerability research with live SDR signal validation.</span>
        <span class="cv-research-meta">2025.03 – 2025.12 · <a href="{{ '/portfolio/#ground-station' | prepend: site.baseurl }}">Details →</a></span>
      </li>
      <li>
        <span class="cv-research-text">Android kernel MTE (Memory Tagging Extension) bypass research.</span>
        <span class="cv-research-meta">2025.12 – 2026.02 · <a href="{{ '/portfolio/#android-mte' | prepend: site.baseurl }}">Details →</a></span>
      </li>
      <li>
        <span class="cv-research-text">Windows kernel local privilege escalation research and exploit development.</span>
        <span class="cv-research-meta">2025.04 – 2025.12 · <a href="{{ '/portfolio/#windows-lpe' | prepend: site.baseurl }}">Details →</a></span>
      </li>
    </ul>
  </div>

  <div class="cv-role">
    <div class="cv-role__head">
      <strong class="cv-role__company">GMO Cybersecurity by Ierae</strong>
      <span class="cv-role__title">Research Internship</span>
      <span class="cv-role__date">2025.07 – 2025.08</span>
    </div>
    <ul class="cv-role__bullets">
      <li>Co-developed CCSDS protocol firewall prototype for the satellite ground-station / OBC uplink.</li>
      <li>Live-demoed at <strong>DEFCON 33 Aerospace Village (Las Vegas)</strong> and <strong>Bahrain Aerospace Village</strong>.</li>
      <li>Co-authored <em>"CCSDS based Firewall for Modern Satellite System"</em> — Computers &amp; Security (SCI, under review).</li>
      <li><em>(추가 디테일 자리 — 본인이 owned한 컴포넌트 / 공격 시나리오 / 산출물)</em></li>
    </ul>
  </div>
</section>

<!-- ==================== PUBLICATIONS ==================== -->
<section class="cv-section">
  <h2 class="cv-section__title" data-en="Publications" data-ko="논문">Publications</h2>
  <ul class="cv-list">
    <li>
      <strong>"CCSDS based Firewall for Modern Satellite System"</strong> · Computers &amp; Security (SCI) · <em data-en="Under review" data-ko="투고예정">Under review</em>
      <div class="cv-list__sub">Woohyeop Im, Gyeongje Oh, Shinichi Kan, Kosuke Ito, Hikohiro Lin, Sayeon Kim, Jinwoo Jeong, Sangbom Yun, Daehee Jang</div>
    </li>
    <li>
      <strong data-en="Vulnerability Research on Open-Source Ground Station Systems via Satellite RF Signal Generation" data-ko="인공위성 RF 신호 생성을 통한 오픈소스 지상국 시스템 취약점 연구">"인공위성 RF 신호 생성을 통한 오픈소스 지상국 시스템 취약점 연구"</strong> · CISC (KCI) · 2026.05
      <div class="cv-list__sub" data-en="Gyeongje Oh, Daehee Jang" data-ko="오경제, 장대희">오경제, 장대희</div>
    </li>
  </ul>
</section>

<!-- ==================== TALKS ==================== -->
<section class="cv-section">
  <h2 class="cv-section__title" data-en="Talks" data-ko="발표">Talks</h2>
  <ul class="cv-list">
    <li><strong data-en="CodeEngn 2026" data-ko="코드엔진 2026">CodeEngn 2026</strong> · 2026.07 — <em data-en="Vulnerability Research on Open-Source Ground Station Systems via Satellite RF Signal Generation" data-ko="인공위성 RF 신호 생성을 통한 오픈소스 지상국 시스템 취약점 연구">"인공위성 RF 신호 생성을 통한 오픈소스 지상국 시스템 취약점 연구"</em></li>
    <li><strong data-en="CISC 2026" data-ko="정보보호학회 2026">CISC 2026</strong> · 2026.05 — <em data-en="Vulnerability Research on Open-Source Ground Station Systems via Satellite RF Signal Generation" data-ko="인공위성 RF 신호 생성을 통한 오픈소스 지상국 시스템 취약점 연구">"인공위성 RF 신호 생성을 통한 오픈소스 지상국 시스템 취약점 연구"</em></li>
    <li><strong>DEFCON 33 Aerospace Village — Bahrain</strong> · 2025.11 — <em>"CCSDS based Firewall for Modern Satellite System"</em></li>
    <li><strong>DEFCON 33 Aerospace Village — Las Vegas</strong> · 2025.08 — <em>"CCSDS based Firewall for Modern Satellite System"</em></li>
  </ul>
</section>

<!-- ==================== AWARDS ==================== -->
<section class="cv-section">
  <h2 class="cv-section__title" data-en="Selected CTF Awards" data-ko="해킹 대회 수상">Selected CTF Awards</h2>

  <h3 class="cv-subsection">International</h3>

  <div class="cv-awards-year">
    <div class="cv-awards-year__label">2026</div>
    <div class="cv-awards-year__list">
      <div class="cv-award">
        <span class="cv-award__place" data-en="Finalist" data-ko="본선 진출">Finalist</span>
        <span class="cv-award__name">DEFCON CTF 2026</span>
        <span class="cv-award__team"><a href="{{ '/assets/defcon2026_quals.png' | prepend: site.baseurl }}">Cold Fusion</a></span>
      </div>
    </div>
  </div>

  <div class="cv-awards-year">
    <div class="cv-awards-year__label">2025</div>
    <div class="cv-awards-year__list">
      <div class="cv-award">
        <span class="cv-award__place">5th</span>
        <span class="cv-award__name">Cykor CTF</span>
        <span class="cv-award__team"><a href="{{ '/assets/Cykor2025.png' | prepend: site.baseurl }}">경희대미남해커들</a></span>
      </div>
      <div class="cv-award">
        <span class="cv-award__place">8th</span>
        <span class="cv-award__name">DEFCON 33 CTF Final</span>
        <span class="cv-award__team"><a href="{{ '/assets/defcon33_quals.png' | prepend: site.baseurl }}">Cold Fusion</a></span>
      </div>
      <div class="cv-award">
        <span class="cv-award__place">9th</span>
        <span class="cv-award__name">CODEGATE CTF Final</span>
        <span class="cv-award__team"><a href="{{ '/assets/codegate2025quals.jpg' | prepend: site.baseurl }}">경희로운세종대왕</a></span>
      </div>
    </div>
  </div>

  <div class="cv-awards-year">
    <div class="cv-awards-year__label">2024</div>
    <div class="cv-awards-year__list">
      <div class="cv-award">
        <span class="cv-award__place">6th</span>
        <span class="cv-award__name">HITCON CTF Final</span>
        <span class="cv-award__team"><a href="https://ctftime.org/event/2345">Cold Fusion</a></span>
      </div>
      <div class="cv-award">
        <span class="cv-award__place">9th</span>
        <span class="cv-award__name">DEFCON 32 CTF Final</span>
        <span class="cv-award__team"><a href="https://nautilus.institute/blog/2024/defcon-32-ctf-final-results">Cold Fusion</a></span>
      </div>
    </div>
  </div>

  <div class="cv-awards-year">
    <div class="cv-awards-year__label">2023</div>
    <div class="cv-awards-year__list">
      <div class="cv-award">
        <span class="cv-award__place">4th</span>
        <span class="cv-award__name">HITCON CTF Final</span>
        <span class="cv-award__team"><a href="https://ctftime.org/event/2035/">프로그램털모찌</a></span>
      </div>
      <div class="cv-award">
        <span class="cv-award__place">6th</span>
        <span class="cv-award__name">CODEGATE CTF University Final</span>
        <span class="cv-award__team"><a href="http://www.newstap.co.kr/news/photo/202306/196798_315670_357.jpg">경희대미남해커들</a></span>
      </div>
      <div class="cv-award">
        <span class="cv-award__place">10th</span>
        <span class="cv-award__name">DiceCTF</span>
        <span class="cv-award__team"><a href="https://ctftime.org/event/1838/">HotIceAmericano</a></span>
        <span class="cv-award__prize">$100</span>
      </div>
    </div>
  </div>

  <div class="cv-awards-year">
    <div class="cv-awards-year__label">2022</div>
    <div class="cv-awards-year__list">
      <div class="cv-award">
        <span class="cv-award__place">10th</span>
        <span class="cv-award__name">CODEGATE CTF University Final</span>
        <span class="cv-award__team"><a href="https://www.boannews.com/media/view.asp?idx=105159">경희대미남해커들</a></span>
      </div>
      <div class="cv-award">
        <span class="cv-award__place">5th</span>
        <span class="cv-award__name">Samsung Hacker's Playground CTF</span>
        <span class="cv-award__team"><a href="https://ctftime.org/event/1715">KoreaNumberOne</a></span>
      </div>
    </div>
  </div>

  <h3 class="cv-subsection">Domestic</h3>

  <div class="cv-awards-year">
    <div class="cv-awards-year__label">2025</div>
    <div class="cv-awards-year__list">
      <div class="cv-award">
        <span class="cv-award__place">5th</span>
        <span class="cv-award__name">CCE CTF Final</span>
        <span class="cv-award__team"><a href="{{ '/assets/2025_CCE.png' | prepend: site.baseurl }}">경희대미남해커들</a></span>
      </div>
    </div>
  </div>

  <div class="cv-awards-year">
    <div class="cv-awards-year__label">2024</div>
    <div class="cv-awards-year__list">
      <div class="cv-award">
        <span class="cv-award__place" data-en="Excellence" data-ko="우수상">Excellence</span>
        <span class="cv-award__name">LG U+ Hacking Competition</span>
        <span class="cv-award__team"><a href="{{ '/assets/LGU+우수상.jpg' | prepend: site.baseurl }}">리버서 구해요</a></span>
        <span class="cv-award__prize">$3,000</span>
      </div>
      <div class="cv-award">
        <span class="cv-award__place" data-en="Special" data-ko="특별상">Special</span>
        <span class="cv-award__name">AutoHack Hacking Competition</span>
        <span class="cv-award__team"><a href="{{ '/assets/Autohack특별상.jpg' | prepend: site.baseurl }}">오똑핵</a></span>
      </div>
      <div class="cv-award">
        <span class="cv-award__place" data-en="Special" data-ko="특별상">Special</span>
        <span class="cv-award__name">FIESTA Hacking Competition</span>
        <span class="cv-award__team"><a href="{{ '/assets/fiesta2024.png' | prepend: site.baseurl }}">학석박입니다</a></span>
        <span class="cv-award__prize">$400</span>
      </div>
      <div class="cv-award">
        <span class="cv-award__place" data-en="Excellence" data-ko="우수상">Excellence</span>
        <span class="cv-award__name">HackTheon Sejong</span>
        <span class="cv-award__team"><a href="https://m.boannews.com/html/detail.html?tab_type=1&idx=130709">QWER</a></span>
        <span class="cv-award__prize">$3,000</span>
      </div>
    </div>
  </div>

  <div class="cv-awards-year">
    <div class="cv-awards-year__label">2022</div>
    <div class="cv-awards-year__list">
      <div class="cv-award">
        <span class="cv-award__place" data-en="Excellence" data-ko="우수상">Excellence</span>
        <span class="cv-award__name">HackTheon Sejong</span>
        <span class="cv-award__team"><a href="https://www.ccnnews.co.kr/news/articleView.html?idxno=265932">라임도둑</a></span>
        <span class="cv-award__prize">$1,000</span>
      </div>
    </div>
  </div>

  <div class="cv-awards-year">
    <div class="cv-awards-year__label">2018</div>
    <div class="cv-awards-year__list">
      <div class="cv-award">
        <span class="cv-award__place" data-en="Gold" data-ko="금상">Gold</span>
        <span class="cv-award__name" data-en="Information Security Olympiad" data-ko="정보보호올림피아드">Information Security Olympiad</span>
        <span class="cv-award__team"><a href="{{ '/assets/정보보호올림피아드_금상.jpg' | prepend: site.baseurl }}">오경제</a></span>
        <span class="cv-award__prize">$1,000</span>
      </div>
    </div>
  </div>
</section>

<!-- ==================== BUG BOUNTY ==================== -->
<section class="cv-section">
  <h2 class="cv-section__title" data-en="Bug Bounty" data-ko="버그바운티">Bug Bounty</h2>
  <div class="cv-bounty">
    <strong>KISA Bug Bounty</strong>
    <span class="cv-award__prize">$3,100</span>
    <p>Remote Code Execution via Heap Overflow in Viewer</p>
    <p class="cv-list__sub">KVE-2023-0095, KVE-2023-5125</p>
  </div>
</section>

<!-- ==================== EDUCATION ==================== -->
<section class="cv-section">
  <h2 class="cv-section__title" data-en="Education" data-ko="학력">Education</h2>
  <ul class="cv-list">
    <li>
      <strong data-en="M.S., Computer Engineering" data-ko="컴퓨터공학과 석사">M.S., Computer Engineering</strong>, <span data-en="Kyung Hee University" data-ko="경희대학교">Kyung Hee University</span> · 2025.03 – Current
      <div class="cv-list__sub">PWNLAB <span data-en="(Lab Leader)" data-ko="(랩장)">(Lab Leader)</span> · Advisor: <a href="https://pwnlab.kr/downloads/cv.pdf" target="_blank">Prof. Daehee Jang</a></div>
    </li>
    <li>
      <strong data-en="B.S., Software Convergence" data-ko="소프트웨어융합학과 학사">B.S., Software Convergence</strong>, <span data-en="Kyung Hee University" data-ko="경희대학교">Kyung Hee University</span> · 2019.03 – 2025.02
      <div class="cv-list__sub" data-en="Including military service (ROK Air Force, 2020.04 – 2022.01)" data-ko="군 복무 포함 (대한민국 공군, 2020.04 – 2022.01)">Including military service (ROK Air Force, 2020.04 – 2022.01)</div>
    </li>
    <li>
      <strong>Best of the Best 7th</strong>, KITRI · <span data-en="Vulnerability Analysis Track" data-ko="취약점 분석 트랙">Vulnerability Analysis Track</span> · 2018.03 – 2019.02
      <div class="cv-list__sub"><a href="{{ '/assets/bob임명장.png' | prepend: site.baseurl }}">Certificate</a></div>
    </li>
  </ul>
</section>

<!-- ==================== OTHER ==================== -->
<section class="cv-section">
  <h2 class="cv-section__title" data-en="Other" data-ko="기타">Other</h2>

  <div class="cv-remarks-group">
    <h4 data-en="CTF Challenge Author / Organizer" data-ko="해킹 대회 출제 및 운영">CTF Challenge Author / Organizer</h4>
    <ul class="cv-remarks-list">
      <li>2023 / 2024 International Drone Hacking Competition</li>
      <li>2022 KHU Software Security Competition</li>
      <li>2017 / 2018 ROOTCTF</li>
    </ul>
  </div>

  <div class="cv-remarks-group">
    <h4 data-en="Wargame" data-ko="워게임">Wargame</h4>
    <ul class="cv-remarks-list">
      <li><a href="http://reversing.kr/rank.php">Reversing.kr</a> — All Clear</li>
      <li><a href="http://xcz.kr/START/rank.php">xcz.kr</a> — All Clear</li>
    </ul>
  </div>
</section>

</div><!-- /cv-content -->

</div><!-- /cv-wrapper -->
