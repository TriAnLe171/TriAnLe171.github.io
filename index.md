---
layout: page
title: "Home"
permalink: /
---

<!-- ===== Styles: layout, cards, timeline, dark mode ===== -->
<style>
  :root{
    --bg:#ffffff;
    --text:#111827;
    --muted:#4b5563;
    --card:#f8fafc;
    --border:#e5e7eb;
    --accent:#2563eb;
    --shadow: 0 8px 30px rgba(0,0,0,.06);
  }
  html[data-theme="dark"]{
    --bg:#0b1220;
    --text:#e5e7eb;
    --muted:#94a3b8;
    --card:#0f172a;
    --border:#1f2937;
    --accent:#60a5fa;
    --shadow: 0 10px 35px rgba(0,0,0,.35);
  }

  /* Page base */
  body{ background:var(--bg); color:var(--text); }
  a{ color:var(--accent); text-decoration:none; }
  a:hover{ text-decoration:underline; }

  /* Small utilities */
  .muted{ color:var(--muted); }
  .divider{ height:1px; background:var(--border); margin: 1.5rem 0; }

  /* Screen-reader only text */
  .sr-only{
    position:absolute;
    width:1px;
    height:1px;
    padding:0;
    margin:-1px;
    overflow:hidden;
    clip:rect(0,0,0,0);
    white-space:nowrap;
    border:0;
  }

  /* Top bar */
  .topbar{
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap:1rem;
    margin: 0 0 1.2rem 0;
  }
  .toggle{
    display:inline-flex;
    align-items:center;
    justify-content:center;
    gap:.5rem;
    border:1px solid var(--border);
    background:var(--card);
    color:var(--text);
    padding:.42rem .62rem;   /* tighter for icon */
    border-radius:999px;
    cursor:pointer;
    box-shadow: var(--shadow);
    font-size:1.05rem;
    line-height:1;
  }
  .toggle .icon{
    display:inline-block;
    width:1.25rem;
    text-align:center;
  }

  /* Make the site header/nav links readable in dark mode (common Jekyll themes) */
  html[data-theme="dark"] .site-header,
  html[data-theme="dark"] header,
  html[data-theme="dark"] .site-nav{
    background: var(--bg) !important;
    border-color: var(--border) !important;
  }

  html[data-theme="dark"] .site-header a,
  html[data-theme="dark"] .site-header a:visited,
  html[data-theme="dark"] .site-nav a,
  html[data-theme="dark"] .site-nav a:visited,
  html[data-theme="dark"] a.page-link{
    color: var(--text) !important;
  }

  html[data-theme="dark"] .site-header a:hover,
  html[data-theme="dark"] .site-nav a:hover,
  html[data-theme="dark"] a.page-link:hover{
    color: var(--accent) !important;
  }

  /* Hero */
  .hero{
    display:flex;
    align-items:center;
    gap:1.25rem;
    flex-wrap:wrap;
  }
  .hero img{
    width:170px;
    border-radius:14px;
    border:1px solid var(--border);
    box-shadow: var(--shadow);
  }
  .hero .meta{
    flex:1;
    min-width: 280px;
  }
  .hero h2{
    margin:0 0 .35rem 0;
  }
  .links{
    display:flex;
    flex-wrap:wrap;
    gap:.9rem;
    margin-top:.6rem;
  }
  .chips{
    display:flex;
    flex-wrap:wrap;
    gap:.45rem;
    margin-top:.8rem;
  }
  .chip{
    border:1px solid var(--border);
    background:var(--card);
    color:var(--muted);
    padding:.22rem .6rem;
    border-radius:999px;
    font-size:.9rem;
    line-height:1.4;
  }

  /* Cards */
  .card{
    background:var(--card);
    border:1px solid var(--border);
    border-radius:16px;
    padding:1rem 1.1rem;
    box-shadow: var(--shadow);
  }
  .card h3{ margin-top:.1rem; }

  /* Timeline */
  .timeline{
    list-style:none;
    padding:0;
    margin:0;
    border-left: 2px solid var(--border);
  }
  .timeline li{
    position:relative;
    padding: 0 0 1rem 1.25rem;
  }
  .timeline li::before{
    content:"";
    position:absolute;
    left:-7px;
    top:.35rem;
    width:12px;
    height:12px;
    border-radius:999px;
    background: var(--accent);
    box-shadow: 0 0 0 4px rgba(37,99,235,.12);
  }
  html[data-theme="dark"] .timeline li::before{
    box-shadow: 0 0 0 4px rgba(96,165,250,.14);
  }
  .timeline time{
    display:inline-block;
    min-width: 4.5rem;
    font-weight:700;
    color: var(--text);
  }
  .timeline .event{
    margin-top:.15rem;
    color: var(--muted);
  }

  /* Open-to callout */
  .callout{
    border:1px solid var(--border);
    background: linear-gradient(180deg, rgba(37,99,235,.07), transparent);
    padding: .9rem 1rem;
    border-radius: 16px;
  }
  html[data-theme="dark"] .callout{
    background: linear-gradient(180deg, rgba(96,165,250,.12), transparent);
  }
</style>

<!-- ===== Dark mode logic (persists in localStorage) ===== -->
<script>
  (function () {
    const KEY = "theme";
    const saved = localStorage.getItem(KEY);
    const prefersDark = window.matchMedia &&
      window.matchMedia("(prefers-color-scheme: dark)").matches;

    const initial = (saved === "dark" || saved === "light")
      ? saved
      : (prefersDark ? "dark" : "light");

    document.documentElement.setAttribute("data-theme", initial);

    function setIcon() {
      const t = document.documentElement.getAttribute("data-theme");
      const icon = document.getElementById("theme-icon");
      const btn = document.getElementById("theme-toggle");
      if (!icon || !btn) return;

      // Show the target theme icon:
      // light -> moon (switch to dark), dark -> sun (switch to light)
      const nextIsDark = (t !== "dark");
      icon.textContent = nextIsDark ? "🌙" : "☀️";
      btn.setAttribute("aria-label", nextIsDark ? "Switch to dark mode" : "Switch to light mode");
    }

    window.__toggleTheme = function () {
      const cur = document.documentElement.getAttribute("data-theme");
      const next = (cur === "dark") ? "light" : "dark";
      document.documentElement.setAttribute("data-theme", next);
      localStorage.setItem(KEY, next);
      setIcon();
    };

    document.addEventListener("DOMContentLoaded", setIcon);
  })();
</script>

<div class="topbar">
  <div class="muted">Multimodal and multilingual NLP for social media</div>
  <button id="theme-toggle" class="toggle" type="button" onclick="__toggleTheme()" aria-label="Toggle theme">
    <span id="theme-icon" class="icon" aria-hidden="true">🌙</span>
    <span class="sr-only">Toggle theme</span>
  </button>
</div>

<div class="hero">
  <img src="/assets/img/profile.png" alt="Tri An Le">
  <div class="meta">
    <h2>Hi, I’m Tri An.</h2>
    <p class="muted" style="margin:.25rem 0 0 0;">
      I’m a senior at Wabash College, double majoring in Computer Science and Mathematics.
      My research focuses on multimodal and multilingual NLP for real-world online communication,
      especially social media content such as memes, GIFs, and short-form video.
      I’m interested in community-aware methods that capture implicit image-text cues and code-switching,
      and in using these models to study how meaning, framing, and engagement shift across communities,
      including in high-stakes settings like misinformation, online harms, and mental health.
    </p>

    <div class="links">
      <a href="mailto:triandole@gmail.com">Email</a>
      <a href="https://github.com/TriAnLe171">GitHub</a>
      <a href="https://www.linkedin.com/in/trianle/">LinkedIn</a>
      <a href="/assets/2025_Tri_An_Le_CV_GS.pdf">CV (PDF)</a>
    </div>

    <div class="chips" aria-label="Interests">
      <span class="chip">Multimodal NLP</span>
      <span class="chip">Multilingual, code-switched NLP</span>
      <span class="chip">Social media language</span>
      <span class="chip">Information retrieval</span>
      <span class="chip">Online harms</span>
      <span class="chip">Misinformation</span>
      <span class="chip">Mental health</span>
    </div>
  </div>
</div>

<div class="divider"></div>

<div class="card" markdown="1">
  <h2 style="margin-top:.2rem;">Research Highlight</h2>

  <h3>MemeMatch, Dual-Context Multimodal Meme Dataset and Retrieval</h3>
  <p class="muted">
    MemeMatch is a large-scale multimodal meme dataset and retrieval system for studying how meaning, intent,
    and emotion connect to online engagement and virality. It includes rich annotations such as emotion vectors,
    topics, and usage-intent labels, built through a dual-context pipeline:
  </p>

  <ul class="muted">
    <li><b>Local context:</b> OCR overlay text plus post title</li>
    <li><b>Global context:</b> template semantics and visual meaning</li>
  </ul>

  <p class="muted">
    On top of this representation, MemeMatch supports intent-aware search (for example, “sarcastic memes about college”)
    and image-based retrieval, enabling analyses of how memes are reframed across communities and templates, and how those
    shifts relate to engagement.
  </p>

  <p style="margin-bottom:.2rem;">
    ➡️ See: <a href="/publications">Publications</a> · <a href="/assets">CV</a>
  </p>
</div>

<div class="divider"></div>

<div class="card" markdown="1">
  <h2 style="margin-top:.2rem;">News</h2>

  <ul class="timeline">
    <li>
      <time>2026</time>
      <div class="event">MemeMatch is under review at ICWSM 2026.</div>
    </li>
    <li>
      <time>2025</time>
      <div class="event">
        Research abroad at AIT Budapest and HSDSLab (Jan 2025 to May 2025),
        internships at Citywide Classroom and Re-Volt Innovations (May 2025 to Aug 2025).
      </div>
    </li>
    <li>
      <time>2024</time>
      <div class="event">Summer Undergraduate Math and Statistics Accelerator (SUMSA), IMSI, The University of Chicago.</div>
    </li>
    <li>
      <time>2023</time>
      <div class="event">Machine Learning Research Assistant, Department of Mathematics and Computer Science, Wabash College.</div>
    </li>
  </ul>
</div>

<div class="divider"></div>

<div class="callout">
  <h2 style="margin:.1rem 0 .35rem 0;">Open to</h2>
  <div class="muted">
    PhD opportunities (Fall 2026), research collaborations in multimodal NLP, social media analysis.
  </div>
</div>