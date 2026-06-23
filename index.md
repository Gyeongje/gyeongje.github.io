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
      <div class="cv-timeline__date">2025.03 -&nbsp;Current</div>
      <div class="cv-timeline__content">
        <strong data-en="KYUNGHEE UNIVERSITY" data-ko="경희대학교">KYUNGHEE UNIVERSITY</strong>
        <p data-en="M.S. in Department of Computer Engineering" data-ko="컴퓨터공학과 석사과정">M.S. in Department of Computer Engineering</p>
        <p class="cv-timeline__sub"><a href="https://pwnlab.kr" target="_blank">PWNLAB</a> <span data-en="(Lab Leader)" data-ko="(랩장)">(Lab Leader)</span> · Advisor: <a href="https://pwnlab.kr/downloads/cv.pdf" target="_blank">Prof. Daehee Jang</a></p>
      </div>
    </div>
    <div class="cv-timeline__item">
      <div class="cv-timeline__date">2019.03 -&nbsp;2025.02</div>
      <div class="cv-timeline__content">
        <strong data-en="KYUNGHEE UNIVERSITY" data-ko="경희대학교">KYUNGHEE UNIVERSITY</strong>
        <p data-en="B.S. in Department of Software Convergence" data-ko="소프트웨어융합학과 학사">B.S. in Department of Software Convergence</p>
      </div>
    </div>
  </div>
</div>

<!-- ==================== EXPERIENCE ==================== -->
<div class="cv-section">
  <h2 class="cv-section__title"><i class="fa fa-briefcase"></i> <span data-en="Experience" data-ko="Experience">Experience</span></h2>

  <div class="cv-timeline">
    <div class="cv-timeline__item">
      <div class="cv-timeline__date">2024.01 -&nbsp;Current</div>
      <div class="cv-timeline__content">
        <strong>PWNLAB</strong> <span class="cv-badge" data-en="Lab Leader" data-ko="랩장">Lab Leader</span>
        <p><span data-en="Kyung Hee University Dept. of Computer Engineering" data-ko="경희대학교 컴퓨터공학과">Kyung Hee University Dept. of Computer Engineering</span></p>
        <ul class="cv-research-list">
          <li><span class="cv-research-text">macOS kernel Bluetooth chipset firmware analysis and mitigation bypass research</span> <span class="cv-research-meta"><a href="{{ '/portfolio/#macos-bt' | prepend: site.baseurl }}">Details →</a></span></li>
          <li><span class="cv-research-text">Microsoft Exchange Server vulnerability research</span> <span class="cv-research-meta"><a href="{{ '/portfolio/#ms-exchange' | prepend: site.baseurl }}">Details →</a></span></li>
          <li><span class="cv-research-text">Windows kernel local privilege escalation research and exploit development<br>Concurrent LLM / MCP prompt-engineering for offensive tooling</span> <span class="cv-research-meta"><a href="{{ '/portfolio/#windows-lpe' | prepend: site.baseurl }}">Details →</a></span></li>
          <li><span class="cv-research-text">Android kernel MTE (Memory Tagging Extension) bypass research</span> <span class="cv-research-meta"><a href="{{ '/portfolio/#android-mte' | prepend: site.baseurl }}">Details →</a></span></li>
          <li><span class="cv-research-text">Satellite signal reception (X/S/UHF/VHF SDR) and commercial ground station vulnerability research</span> <span class="cv-research-meta"><a href="{{ '/portfolio/#satellite-rx' | prepend: site.baseurl }}">Details →</a></span></li>
          <li><span class="cv-research-text">Drone (DJI / PX4) firmware vulnerability analysis and security tooling</span> <span class="cv-research-meta"><a href="{{ '/portfolio/#drone-security' | prepend: site.baseurl }}">Details →</a></span></li>
          <li><span class="cv-research-text">Open-source ground station vulnerability research with live SDR validation</span> <span class="cv-research-meta"><a href="{{ '/portfolio/#ground-station' | prepend: site.baseurl }}">Details →</a></span></li>
        </ul>
      </div>
    </div>
    <div class="cv-timeline__item">
      <div class="cv-timeline__date">2025.07 -&nbsp;2025.08</div>
      <div class="cv-timeline__content">
        <strong>GMO CyberSecurity by Ierae</strong> <span class="cv-badge">Internship</span>
        <ul class="cv-research-list">
          <li><span class="cv-research-text">Co-developed CCSDS protocol firewall prototype for the satellite ground station and OBC uplink.<br>Live-demoed at DEFCON 33 Aerospace Village (Las Vegas, Bahrain).</span> <span class="cv-research-meta"><a href="{{ '/portfolio/#gmo-ccsds' | prepend: site.baseurl }}">Details →</a></span></li>
          <li><span class="cv-research-text">Submitted <em>"CCSDS based Firewall for Modern Satellite System"</em> to Computers &amp; Security (SCI), currently under review.</span> <span class="cv-research-meta"><a href="{{ '/portfolio/#gmo-paper' | prepend: site.baseurl }}">Details →</a></span></li>
        </ul>
      </div>
    </div>
    <div class="cv-timeline__item">
      <div class="cv-timeline__date">2022.03 -&nbsp;2023.12</div>
      <div class="cv-timeline__content">
        <strong data-en="HAYYIM SECURITY" data-ko="하임시큐리티">HAYYIM SECURITY</strong> <span class="cv-badge">Security Researcher</span>
        <ul class="cv-research-list">
          <li><span class="cv-research-text">WinAFL-based fuzzing harness for Office document parser dll.</span> <span class="cv-research-meta"><a href="{{ '/portfolio/#hayyim-office' | prepend: site.baseurl }}">Details →</a></span></li>
          <li><span class="cv-research-text">Browser vulnerability research targeting renderer / IPC attack surfaces.</span> <span class="cv-research-meta"><a href="{{ '/portfolio/#hayyim-browser' | prepend: site.baseurl }}">Details →</a></span></li>
          <li><span class="cv-research-text">Antivirus exploit and bypass research.</span> <span class="cv-research-meta"><a href="{{ '/portfolio/#hayyim-antivirus' | prepend: site.baseurl }}">Details →</a></span></li>
          <li><span class="cv-research-text">RDP protocol vulnerability research and exploitation.</span> <span class="cv-research-meta"><a href="{{ '/portfolio/#hayyim-rdp' | prepend: site.baseurl }}">Details →</a></span></li>
          <li><span class="cv-research-text">Disclosed two RCEs to KISA Bug Bounty — KVE-2023-0095, KVE-2023-5125.</span> <span class="cv-research-meta"><a href="https://gye0ngje.com/vulnerability-research/2023/01/14/heap-overflow-in-image-viewer-psd-parsing.html">Details →</a></span></li>
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
      <div class="cv-timeline__date" data-en="Under Review" data-ko="리뷰중">리뷰중</div>
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
        <p><span data-en="CISC (KCI)" data-ko="정보보호학회 (KCI)">정보보호학회 (KCI)</span> · <a href="{{ '/assets/cisc2026_ground_station.pdf' | prepend: site.baseurl }}" target="_blank">PDF</a></p>
        <p class="cv-timeline__sub" data-en="Gyeongje Oh, Daehee Jang" data-ko="오경제, 장대희">오경제, 장대희</p>
      </div>
    </div>
  </div>
</div>

<!-- ==================== CTF AWARDS ==================== -->
<div class="cv-section">
  <h2 class="cv-section__title"><i class="fa fa-trophy"></i> CTF Awards</h2>

  <div class="cv-awards-grid">
    <h3 class="cv-subsection cv-awards-grid__head">International</h3>
    <h3 class="cv-subsection cv-awards-grid__head">Domestic</h3>

    <div class="cv-awards-grid__cell cv-awards-grid__cell--intl">
      <a class="cv-award" href="{{ '/assets/defcon2026_quals.png' | prepend: site.baseurl }}">
        <span class="cv-award__place" data-en="Finalist" data-ko="본선 진출">Finalist</span>
        <span class="cv-award__name">DEFCON 34 CTF (2026)</span>
        <span class="cv-award__team">Cold Fusion</span>
      </a>
      <a class="cv-award" href="{{ '/assets/defcon33_quals.png' | prepend: site.baseurl }}">
        <span class="cv-award__place" data-en="Finalist" data-ko="본선 진출">Finalist</span>
        <span class="cv-award__name">DEFCON 33 CTF (2025)</span>
        <span class="cv-award__team">Cold Fusion</span>
      </a>
      <a class="cv-award" href="{{ '/assets/codegate2025quals.jpg' | prepend: site.baseurl }}">
        <span class="cv-award__place" data-en="Finalist" data-ko="본선 진출">Finalist</span>
        <span class="cv-award__name">CODEGATE CTF (2025)</span>
        <span class="cv-award__team">경희로운세종대왕</span>
      </a>
      <a class="cv-award" href="https://ctftime.org/event/2345">
        <span class="cv-award__place" data-en="Finalist" data-ko="본선 진출">Finalist</span>
        <span class="cv-award__name">HITCON CTF (2024)</span>
        <span class="cv-award__team">Cold Fusion</span>
      </a>
      <a class="cv-award" href="https://nautilus.institute/blog/2024/defcon-32-ctf-final-results">
        <span class="cv-award__place" data-en="Finalist" data-ko="본선 진출">Finalist</span>
        <span class="cv-award__name">DEFCON 32 CTF (2024)</span>
        <span class="cv-award__team">Cold Fusion</span>
      </a>
      <a class="cv-award" href="https://ctftime.org/event/2035/">
        <span class="cv-award__place" data-en="Finalist" data-ko="본선 진출">Finalist</span>
        <span class="cv-award__name">HITCON CTF (2023)</span>
        <span class="cv-award__team">프로그램털모찌</span>
      </a>
      <a class="cv-award" href="http://www.newstap.co.kr/news/photo/202306/196798_315670_357.jpg">
        <span class="cv-award__place" data-en="Finalist" data-ko="본선 진출">Finalist</span>
        <span class="cv-award__name">CODEGATE CTF Univ (2023)</span>
        <span class="cv-award__team">경희대미남해커들</span>
      </a>
      <a class="cv-award" href="https://www.boannews.com/media/view.asp?idx=105159">
        <span class="cv-award__place" data-en="Finalist" data-ko="본선 진출">Finalist</span>
        <span class="cv-award__name">CODEGATE CTF Univ (2022)</span>
        <span class="cv-award__team">경희대미남해커들</span>
      </a>
      <a class="cv-award" href="{{ '/assets/코드게이트본선9위.png' | prepend: site.baseurl }}">
        <span class="cv-award__place" data-en="Finalist" data-ko="본선 진출">Finalist</span>
        <span class="cv-award__name">CODEGATE CTF Junior (2018)</span>
        <span class="cv-award__team">오경제</span>
      </a>
    </div>

    <div class="cv-awards-grid__cell cv-awards-grid__cell--dom">
      <a class="cv-award" href="{{ '/assets/2025_CCE.png' | prepend: site.baseurl }}">
        <span class="cv-award__place" data-en="Finalist" data-ko="본선 진출">Finalist</span>
        <span class="cv-award__name">CCE CTF (2025)</span>
        <span class="cv-award__team">경희대미남해커들</span>
      </a>
      <a class="cv-award" href="{{ '/assets/LGU+우수상.jpg' | prepend: site.baseurl }}">
        <span class="cv-award__place" data-en="Excellence" data-ko="우수상">Excellence</span>
        <span class="cv-award__name">LG U+ CTF (2024)</span>
        <span class="cv-award__team">리버서 구해요</span>
      </a>
      <a class="cv-award" href="{{ '/assets/Autohack특별상.jpg' | prepend: site.baseurl }}">
        <span class="cv-award__place" data-en="Special" data-ko="특별상">Special</span>
        <span class="cv-award__name">AutoHack CTF (2024)</span>
        <span class="cv-award__team">오똑핵</span>
      </a>
      <a class="cv-award" href="{{ '/assets/fiesta2024.png' | prepend: site.baseurl }}">
        <span class="cv-award__place" data-en="Special" data-ko="특별상">Special</span>
        <span class="cv-award__name">FIESTA CTF (2024)</span>
        <span class="cv-award__team">학석박입니다</span>
      </a>
      <a class="cv-award" href="https://m.boannews.com/html/detail.html?tab_type=1&idx=130709">
        <span class="cv-award__place" data-en="Excellence" data-ko="우수상">Excellence</span>
        <span class="cv-award__name">HackTheon Sejong (2024)</span>
        <span class="cv-award__team">QWER</span>
      </a>
      <a class="cv-award" href="https://www.ccnnews.co.kr/news/articleView.html?idxno=265932">
        <span class="cv-award__place" data-en="Excellence" data-ko="우수상">Excellence</span>
        <span class="cv-award__name">HackTheon Sejong (2022)</span>
        <span class="cv-award__team">라임도둑</span>
      </a>
      <a class="cv-award" href="{{ '/assets/정보보호올림피아드_금상.jpg' | prepend: site.baseurl }}">
        <span class="cv-award__place" data-en="Gold" data-ko="금상">Gold</span>
        <span class="cv-award__name" data-en="Information Security Olympiad (2018)" data-ko="정보보호올림피아드 (2018)">Information Security Olympiad (2018)</span>
        <span class="cv-award__team">오경제</span>
      </a>
    </div>
  </div>

</div>

<!-- ==================== BUG BOUNTY ==================== -->
<div class="cv-section">
  <h2 class="cv-section__title"><i class="fa fa-bug"></i> Bug Bounty</h2>

  <div class="cv-bounty">
    <strong>KVE-2023-0095, KVE-2023-5125</strong>
    <p class="cv-timeline__sub">Remote Code Execution via Heap Overflow in Viewer ($3,100)</p>
  </div>
</div>

<!-- ==================== TALKS ==================== -->
<div class="cv-section">
  <h2 class="cv-section__title"><i class="fa fa-microphone"></i> <span data-en="Talks" data-ko="Talks">Talks</span></h2>

  <div class="cv-timeline">
    <div class="cv-timeline__item">
      <div class="cv-timeline__date">2026.05 /&nbsp;2026.07</div>
      <div class="cv-timeline__content">
        <strong data-en="CISC 2026 · CodeEngn 2026" data-ko="정보보호학회 2026 · 코드엔진 2026">정보보호학회 2026 · 코드엔진 2026</strong>
        <p data-en="&quot;Vulnerability Research on Open-Source Ground Station Systems via Satellite RF Signal Generation&quot;" data-ko="&quot;인공위성 RF 신호 생성을 통한 오픈소스 지상국 시스템 취약점 연구&quot;">"인공위성 RF 신호 생성을 통한 오픈소스 지상국 시스템 취약점 연구"</p>
      </div>
    </div>
    <div class="cv-timeline__item">
      <div class="cv-timeline__date">2025.08 /&nbsp;2025.11</div>
      <div class="cv-timeline__content">
        <strong>DEFCON 33 Aerospace Village (Las Vegas, Bahrain)</strong>
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
      <div class="cv-timeline__date">2020.04 -&nbsp;2022.01</div>
      <div class="cv-timeline__content">
        <strong data-en="Republic of Korea Air Force" data-ko="대한민국 공군">Republic of Korea Air Force</strong>
        <p data-en="MOS: Information Security" data-ko="병과: 정보보호">MOS: Information Security</p>
      </div>
    </div>
    <div class="cv-timeline__item">
      <div class="cv-timeline__date">2018.03 -&nbsp;2019.02</div>
      <div class="cv-timeline__content">
        <strong>Best of the Best 7th</strong>
        <p>KITRI · <span data-en="Vulnerability Analysis Track" data-ko="취약점 분석 트랙">Vulnerability Analysis Track</span> · <a href="{{ '/assets/bob임명장.png' | prepend: site.baseurl }}">Certificate</a></p>
      </div>
    </div>
  </div>

  <p class="cv-remarks-line"><strong>CTF Challenge Author / Organizer:</strong> International Drone CTF (2023 / 2024)</p>

  <p class="cv-remarks-line"><strong>Wargame:</strong> <a href="http://reversing.kr/rank.php">Reversing.kr</a> (All Clear) · <a href="http://xcz.kr/START/rank.php">xcz.kr</a> (All Clear)</p>
</div>

</div><!-- /cv-content -->

<div class="about">
<div class="about__divider">*****</div>
<div class="about__text"><strong>Contact: ogj0824@gmail.com</strong></div>
</div>

</div><!-- /cv-wrapper -->
