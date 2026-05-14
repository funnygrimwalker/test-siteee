<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Work Without a Net</title>

  <!-- Google Fonts -->
  <link
    href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,600;1,400&family=Libre+Franklin:wght@300;400;500;600&display=swap"
    rel="stylesheet"
  />

  <style>
    /* ================================
       VARIABLES
    ================================ */
    :root {
      --bg: #0e0e0c;
      --surface: #161614;
      --surface2: #1e1e1b;
      --border: rgba(255, 255, 255, 0.07);
      --text: #f0ede6;
      --muted: #8a8780;
      --faint: #4a4844;
      --gold: #c8a96e;
      --green: #4e8c6a;
      --red: #b85a4a;
      --blue: #4a7fa8;
      --serif: "Playfair Display", serif;
      --sans: "Libre Franklin", sans-serif;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: var(--sans);
      font-size: 15px;
      line-height: 1.75;
    }

    /* ================================
       NAVIGATION
    ================================ */
    nav {
      position: fixed;
      top: 0;
      width: 100%;
      height: 56px;
      background: rgba(14, 14, 12, 0.95);
      border-bottom: 0.5px solid var(--border);
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0 2.5rem;
      z-index: 100;
    }

    .nav-logo {
      font-family: var(--serif);
      color: var(--gold);
      cursor: pointer;
    }

    .nav-links {
      list-style: none;
      display: flex;
    }

    .nav-links a {
      padding: 0 1rem;
      line-height: 56px;
      font-size: 12px;
      text-transform: uppercase;
      color: var(--muted);
      text-decoration: none;
      border-bottom: 2px solid transparent;
    }

    .nav-links a:hover,
    .nav-links a.active {
      color: var(--text);
      border-bottom-color: var(--gold);
    }

    /* ================================
       PAGES
    ================================ */
    .page {
      display: none;
      padding-top: 56px;
      min-height: 100vh;
    }

    .page.active {
      display: block;
    }

    /* ================================
       HERO
    ================================ */
    .hero {
      max-width: 900px;
      margin: 0 auto;
      padding: 6rem 2.5rem 4rem;
      border-bottom: 0.5px solid var(--border);
    }

    .eyebrow {
      font-size: 11px;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 1.5rem;
    }

    .hero h1 {
      font-family: var(--serif);
      font-size: clamp(2.4rem, 6vw, 4rem);
      line-height: 1.15;
      margin-bottom: 1.5rem;
    }

    .hero-desc {
      color: var(--muted);
      max-width: 600px;
      font-size: 17px;
      margin-bottom: 2.5rem;
    }

    /* ================================
       CONTENT
    ================================ */
    .page-content {
      max-width: 900px;
      margin: 0 auto;
      padding: 3.5rem 2.5rem;
    }

    .page-header {
      border-bottom: 0.5px solid var(--border);
      padding-bottom: 2rem;
      margin-bottom: 3rem;
    }

    .page-header h2 {
      font-family: var(--serif);
      font-size: 2.5rem;
      margin-bottom: 1rem;
    }

    .section-label {
      font-size: 10px;
      letter-spacing: 0.14em;
      text-transform: uppercase;
      color: var(--faint);
      margin-bottom: 1rem;
    }

    .content-section {
      margin-bottom: 3.5rem;
    }

    /* ================================
       LISTS
    ================================ */
    .styled-list {
      list-style: none;
      margin-top: 1rem;
    }

    .styled-list li {
      position: relative;
      padding-left: 1.2rem;
      margin-bottom: 0.6rem;
      color: #c8c5be;
    }

    .styled-list li::before {
      content: "→";
      position: absolute;
      left: 0;
      color: var(--green);
    }

    /* ================================
       FOOTER
    ================================ */
    footer {
      border-top: 0.5px solid var(--border);
      padding: 1.5rem 2.5rem;
      display: flex;
      justify-content: space-between;
      font-size: 12px;
      color: var(--faint);
    }
  </style>
</head>

<body>
  <!-- NAV -->
  <nav>
    <div class="nav-logo" onclick="showPage('home')">Work Without a Net</div>
    <ul class="nav-links">
      <li><a id="nav-home" class="active" href="#" onclick="showPage('home');return false;">Overview</a></li>
      <li><a id="nav-page1" href="#" onclick="showPage('page1');return false;">The Gig Economy</a></li>
      <li><a id="nav-page2" href="#" onclick="showPage('page2');return false;">Physical Health</a></li>
    </ul>
  </nav>

  <!-- HOME -->
  <div class="page active" id="home">
    <div class="hero">
      <div class="eyebrow">Medical Sociology — Capstone</div>
      <h1>Work without a net:<br />the <em>gig economy</em></h1>
      <p class="hero-desc">
        When workers are denied institutional protections, health consequences
        become structurally inevitable.
      </p>
    </div>

    <footer>
      <span>Medical Sociology Capstone</span>
      <span>Due May 13, 2026</span>
    </footer>
  </div>

  <!-- PAGE 1 -->
  <div class="page" id="page1">
    <div class="page-content">
      <div class="page-header">
        <div class="eyebrow">Panel 01</div>
        <h2>What is the gig economy?</h2>
      </div>

      <div class="content-section">
        <div class="section-label">Classification</div>
        <ul class="styled-list">
          <li>No employer-provided health insurance</li>
          <li>No workers’ compensation</li>
          <li>No paid sick leave</li>
          <li>No unemployment insurance</li>
        </ul>
      </div>
    </div>

    <footer>
      <span onclick="showPage('home')" style="cursor:pointer;">← Overview</span>
      <span onclick="showPage('page2')" style="cursor:pointer;">Physical Health →</span>
    </footer>
  </div>

  <!-- PAGE 2 -->
  <div class="page" id="page2">
    <div class="page-content">
      <div class="page-header">
        <div class="eyebrow">Panel 02</div>
        <h2>Physical Health</h2>
      </div>

      <div class="content-section">
        <div class="section-label">Healthcare Access</div>
        <ul class="styled-list">
          <li>Workers delay care due to cost</li>
          <li>Emergency departments replace primary care</li>
          <li>Chronic illness goes untreated</li>
        </ul>
      </div>
    </div>

    <footer>
      <span onclick="showPage('page1')" style="cursor:pointer;">← Gig Economy</span>
      <span onclick="showPage('home')" style="cursor:pointer;">Overview →</span>
    </footer>
  </div>

  <!-- JAVASCRIPT -->
  <script>
    function showPage(pageId) {
      document.querySelectorAll(".page").forEach(p => p.classList.remove("active"));
      document.querySelectorAll(".nav-links a").forEach(a => a.classList.remove("active"));

      document.getElementById(pageId).classList.add("active");
      const nav = document.getElementById("nav-" + pageId);
      if (nav) nav.classList.add("active");

      window.scrollTo({ top: 0, behavior: "smooth" });
    }
  </script>
</body>
</html>
