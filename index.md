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
    <a href="https://github.com/Gyeongje" target="_blank"><i class="fa fa-github"></i> GitHub</a>
    <a href="https://www.linkedin.com/in/gyeongjeoh/" target="_blank"><i class="fa fa-linkedin-square"></i> LinkedIn</a>
  </div>
  <div class="cv-actions">
    <a href="#" class="cv-download" onclick="generatePDF(); return false;">
      <i class="fa fa-download"></i> Download CV
    </a>
    <a href="#" class="cv-download" onclick="generateFullPDF(); return false;">
      <i class="fa fa-download"></i> Full Download
    </a>
  </div>
</div>

<div id="cv-content">

<!-- ==================== EDUCATION ==================== -->
<div class="cv-section">
  <h2 class="cv-section__title"><i class="fa fa-graduation-cap"></i> <span data-en="Education" data-ko="Education">Education</span></h2>

  <div class="cv-timeline">
    <div class="cv-timeline__item">
      <div class="cv-timeline__date">2025.03 - Current</div>
      <div class="cv-timeline__content">
        <strong data-en="KYUNGHEE UNIVERSITY" data-ko="경희대학교">KYUNGHEE UNIVERSITY</strong>
        <p data-en="M.S. in Department of Computer Engineering" data-ko="컴퓨터공학과 석사과정">M.S. in Department of Computer Engineering</p>
        <p class="cv-timeline__sub"><a href="https://pwnlab.kr" target="_blank">PWNLAB</a> <span data-en="(Lab Leader)" data-ko="(랩장)">(Lab Leader)</span> · Advisor: <a href="https://pwnlab.kr/downloads/cv.pdf" target="_blank">Prof. Daehee Jang</a></p>
      </div>
    </div>
    <div class="cv-timeline__item">
      <div class="cv-timeline__date">2019.03 - 2025.02</div>
      <div class="cv-timeline__content">
        <strong data-en="KYUNGHEE UNIVERSITY" data-ko="경희대학교">KYUNGHEE UNIVERSITY</strong>
        <p data-en="B.S. in Department of Software Convergence" data-ko="소프트웨어융합학과 학사">B.S. in Department of Software Convergence</p>
        <p class="cv-timeline__sub" data-en="Including military service" data-ko="군 복무 포함">Including military service</p>
      </div>
    </div>
  </div>
</div>

<!-- ==================== EXPERIENCE ==================== -->
<div class="cv-section">
  <h2 class="cv-section__title"><i class="fa fa-briefcase"></i> <span data-en="Experience" data-ko="Experience">Experience</span></h2>

  <div class="cv-timeline">
    <div class="cv-timeline__item">
      <div class="cv-timeline__date">2024.01 - Current</div>
      <div class="cv-timeline__content">
        <strong>PWNLAB</strong> <span class="cv-badge" data-en="Lab Leader" data-ko="랩장">Lab Leader</span>
        <p><span data-en="Kyunghee Univ. Dept. of Computer Engineering" data-ko="경희대학교 컴퓨터공학과">Kyunghee Univ. Dept. of Computer Engineering</span> (Advisor: <a href="https://pwnlab.kr/downloads/cv.pdf" target="_blank">Prof. Daehee Jang</a>)</p>
        <ul class="cv-research-list">
          <li>macOS kernel Bluetooth chipset firmware analysis and mitigation bypass research <span class="cv-research-meta">· <a href="{{ '/portfolio/#macos-bt' | prepend: site.baseurl }}">Details →</a></span></li>
          <li>Satellite OBC security audit tooling for GomSpace / EnduroSat with GMO IERAE <span class="cv-research-meta">· <a href="{{ '/portfolio/#satellite-obc' | prepend: site.baseurl }}">Details →</a></span></li>
          <li>Open-source ground station vulnerability research with live SDR validation <span class="cv-research-meta">· <a href="{{ '/portfolio/#ground-station' | prepend: site.baseurl }}">Details →</a></span></li>
          <li>Android kernel MTE (Memory Tagging Extension) bypass research <span class="cv-research-meta">· <a href="{{ '/portfolio/#android-mte' | prepend: site.baseurl }}">Details →</a></span></li>
          <li>Windows kernel local privilege escalation research and exploit development <span class="cv-research-meta">· <a href="{{ '/portfolio/#windows-lpe' | prepend: site.baseurl }}">Details →</a></span></li>
        </ul>
      </div>
    </div>
    <div class="cv-timeline__item">
      <div class="cv-timeline__date">2025.07 - 2025.08</div>
      <div class="cv-timeline__content">
        <strong>GMO CyberSecurity by Ierae</strong> <span class="cv-badge">Internship</span>
        <ul class="cv-research-list">
          <li>Co-developed CCSDS protocol firewall prototype for the satellite ground-station / OBC uplink.</li>
          <li>Live-demoed at <strong>DEFCON 33 Aerospace Village (Las Vegas)</strong> and <strong>Bahrain Aerospace Village</strong>.</li>
          <li>Co-authored <em>"CCSDS based Firewall for Modern Satellite System"</em> — Computers &amp; Security (SCI, under review).</li>
          <li><em>(추가 디테일 자리 — owned 컴포넌트 / 공격 시나리오 / 산출물)</em></li>
        </ul>
      </div>
    </div>
    <div class="cv-timeline__item">
      <div class="cv-timeline__date">2022.03 - 2023.12</div>
      <div class="cv-timeline__content">
        <strong data-en="HAYYIM SECURITY" data-ko="하임시큐리티">HAYYIM SECURITY</strong> <span class="cv-badge">Security Researcher</span>
        <ul class="cv-research-list">
          <li>Vulnerability research and exploit development across Browser, Office, VM, and RDP attack surfaces on Windows.</li>
          <li>Built WinAFL-based fuzzing harnesses for commercial document parsers; surfaced heap-overflow and OOB-write primitives.</li>
          <li>Disclosed two RCEs to KISA Bug Bounty — <strong>KVE-2023-0095</strong>, <strong>KVE-2023-5125</strong> ($3,100).</li>
          <li><em>(추가 디테일 자리 — 본인이 owned했던 컴포넌트 / 산출물 / 협업)</em></li>
        </ul>
      </div>
    </div>
  </div>
</div>

<!-- ==================== PUBLICATIONS ==================== -->
<div class="cv-section">
  <h2 class="cv-section__title"><i class="fa fa-file-text"></i> Publications</h2>

  <div class="cv-timeline">
    <div class="cv-timeline__item">
      <div class="cv-timeline__date" data-en="Pending" data-ko="투고예정">Pending</div>
      <div class="cv-timeline__content">
        <strong>"CCSDS based Firewall for Modern Satellite System"</strong>
        <p>Computers & Security (SCI)</p>
        <p class="cv-timeline__sub">Woohyeop Im, Gyeongje Oh, Shinichi Kan, Kosuke Ito, Hikohiro Lin, Sayeon Kim, Jinwoo Jeong, Sangbom Yun, Daehee Jang</p>
      </div>
    </div>
    <div class="cv-timeline__item">
      <div class="cv-timeline__date">2026.05</div>
      <div class="cv-timeline__content">
        <strong data-en="Vulnerability Research on Open-Source Ground Station Systems via Satellite RF Signal Generation" data-ko="인공위성 RF 신호 생성을 통한 오픈소스 지상국 시스템 취약점 연구">"인공위성 RF 신호 생성을 통한 오픈소스 지상국 시스템 취약점 연구"</strong>
        <p data-en="CISC (KCI)" data-ko="정보보호학회 (KCI)">정보보호학회 (KCI)</p>
        <p class="cv-timeline__sub" data-en="Gyeongje Oh, Daehee Jang" data-ko="오경제, 장대희">오경제, 장대희</p>
      </div>
    </div>
  </div>
</div>

<!-- ==================== CTF AWARDS ==================== -->
<div class="cv-section">
  <h2 class="cv-section__title"><i class="fa fa-trophy"></i> Hacking Competition (CTF) Awards</h2>

  <div class="cv-awards-grid">
    <div class="cv-awards-col">
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

  <div class="cv-awards-year">
    <div class="cv-awards-year__label">2018</div>
    <div class="cv-awards-year__list">
      <div class="cv-award">
        <span class="cv-award__place">9th</span>
        <span class="cv-award__name">CODEGATE CTF Junior Final</span>
        <span class="cv-award__team"><a href="{{ '/assets/코드게이트본선9위.png' | prepend: site.baseurl }}">오경제</a></span>
      </div>
    </div>
  </div>

    </div><!-- /.cv-awards-col International -->
    <div class="cv-awards-col">
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
    </div><!-- /.cv-awards-col Domestic -->
  </div><!-- /.cv-awards-grid -->

</div>

<!-- ==================== BUG BOUNTY ==================== -->
<div class="cv-section">
  <h2 class="cv-section__title"><i class="fa fa-bug"></i> Bug Bounty</h2>

  <div class="cv-bounty">
    <strong>KISA Bug Bounty</strong>
    <span class="cv-award__prize">$3,100</span>
    <p>Remote Code Execution via Heap Overflow in Viewer</p>
    <p class="cv-timeline__sub">KVE-2023-0095, KVE-2023-5125</p>
  </div>
</div>

<!-- ==================== PRESENTATIONS ==================== -->
<div class="cv-section">
  <h2 class="cv-section__title"><i class="fa fa-microphone"></i> <span data-en="Presentations" data-ko="Presentations">Presentations</span></h2>

  <div class="cv-timeline">
    <div class="cv-timeline__item">
      <div class="cv-timeline__date">2026.07</div>
      <div class="cv-timeline__content">
        <strong data-en="CodeEngn 2026" data-ko="코드엔진 2026">코드엔진 2026</strong>
        <p data-en="&quot;Vulnerability Research on Open-Source Ground Station Systems via Satellite RF Signal Generation&quot;" data-ko="&quot;인공위성 RF 신호 생성을 통한 오픈소스 지상국 시스템 취약점 연구&quot;">"인공위성 RF 신호 생성을 통한 오픈소스 지상국 시스템 취약점 연구"</p>
      </div>
    </div>
    <div class="cv-timeline__item">
      <div class="cv-timeline__date">2026.05</div>
      <div class="cv-timeline__content">
        <strong data-en="CISC 2026" data-ko="정보보호학회 2026">정보보호학회 2026</strong>
        <p data-en="&quot;Vulnerability Research on Open-Source Ground Station Systems via Satellite RF Signal Generation&quot;" data-ko="&quot;인공위성 RF 신호 생성을 통한 오픈소스 지상국 시스템 취약점 연구&quot;">"인공위성 RF 신호 생성을 통한 오픈소스 지상국 시스템 취약점 연구"</p>
      </div>
    </div>
    <div class="cv-timeline__item">
      <div class="cv-timeline__date">2025.11</div>
      <div class="cv-timeline__content">
        <strong>DEFCON Aerospace Village — Bahrain</strong>
        <p>"CCSDS based Firewall for Modern Satellite System"</p>
      </div>
    </div>
    <div class="cv-timeline__item">
      <div class="cv-timeline__date">2025.08</div>
      <div class="cv-timeline__content">
        <strong>DEFCON Aerospace Village — Las Vegas</strong>
        <p>"CCSDS based Firewall for Modern Satellite System"</p>
      </div>
    </div>
  </div>
</div>

<!-- ==================== REMARKS ==================== -->
<div class="cv-section">
  <h2 class="cv-section__title"><i class="fa fa-star"></i> <span data-en="Remarks" data-ko="Remarks">Remarks</span></h2>

  <div class="cv-timeline">
    <div class="cv-timeline__item">
      <div class="cv-timeline__date">2020.04 - 2022.01</div>
      <div class="cv-timeline__content">
        <strong data-en="Republic of Korea Air Force" data-ko="대한민국 공군">Republic of Korea Air Force</strong>
        <p data-en="MOS: Information Security" data-ko="병과: 정보보호">MOS: Information Security</p>
      </div>
    </div>
  </div>

  <div class="cv-remarks-group">
    <h4 data-en="External Program" data-ko="외부 프로그램">External Program</h4>
    <ul class="cv-remarks-list">
      <li>Best of the Best 7th, KITRI — Vulnerability Analysis Track (2018.03 – 2019.02) · <a href="{{ '/assets/bob임명장.png' | prepend: site.baseurl }}">Certificate</a></li>
    </ul>
  </div>

  <div class="cv-remarks-group">
    <h4>CTF Challenge Author / Organizer</h4>
    <ul class="cv-remarks-list">
      <li>2023/2024 International Drone Hacking Competition</li>
      <li>2022 KHU Software Security Competition</li>
      <li>2017/2018 ROOTCTF</li>
    </ul>
  </div>

  <div class="cv-remarks-group">
    <h4>Wargame</h4>
    <ul class="cv-remarks-list">
      <li><a href="http://reversing.kr/rank.php">Reversing.kr</a> <span class="cv-badge cv-badge--accent">All Clear</span></li>
      <li><a href="http://xcz.kr/START/rank.php">xcz.kr</a> <span class="cv-badge cv-badge--accent">All Clear</span></li>
    </ul>
  </div>
</div>

</div><!-- /cv-content -->

<div class="about">
<div class="about__divider">*****</div>
<div class="about__text"><strong>Contact: ogj0824@gmail.com</strong></div>
</div>

</div><!-- /cv-wrapper -->
