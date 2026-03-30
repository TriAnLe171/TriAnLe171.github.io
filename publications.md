---
layout: page
title: "Publications"
permalink: /publications/
---

<style>
  :root{
    --bg:#ffffff;
    --text:#111827;
    --muted:#6b7280;
    --line:#e5e7eb;
    --accent:#2563eb;
  }

  html[data-theme="dark"]{
    --bg:#0b1220;
    --text:#e5e7eb;
    --muted:#94a3b8;
    --line:#1f2937;
    --accent:#60a5fa;
  }

  body{
    background:var(--bg);
    color:var(--text);
  }

  a{
    color:var(--accent);
    text-decoration:none;
  }

  a:hover{
    text-decoration:underline;
  }

  .pub-page{
    max-width:780px;
    margin:0 auto;
  }

  .pub-header{
    margin-bottom:1.5rem;
  }

  .pub-header h1{
    margin:0;
  }

  .pub-section{
    margin-top:1.75rem;
  }

  .section-label{
    margin:0 0 .85rem 0;
    font-size:.95rem;
    font-weight:600;
    color:var(--muted);
    text-transform:uppercase;
    letter-spacing:.04em;
  }

  .pub-item{
    padding:0 0 1.25rem 0;
    margin-bottom:1.25rem;
    border-bottom:1px solid var(--line);
  }

  .pub-item:last-child{
    margin-bottom:0;
  }

  .paper-title{
    margin:0 0 .4rem 0;
    font-size:1.05rem;
    font-weight:700;
    line-height:1.45;
  }

  .authors,
  .venue,
  .links{
    margin:0;
    color:var(--muted);
    line-height:1.6;
  }

  .links{
    margin-top:.4rem;
  }
</style>

<div class="pub-page">
  <div class="pub-header">
    <h1>Publications</h1>
  </div>

  <section class="pub-section">
    <p class="section-label">Conference Publications</p>

    <article class="pub-item">
      <p class="paper-title">
        MemeMatch: A Large-Scale Dual-Context Multimodal Dataset and Retrieval System for Internet Memes
      </p>

      <p class="authors">
        <strong>Do Tri An Le</strong>, Donát Ákos Köller, Qixin Deng, Roland Molontay
      </p>

      <p class="venue">
        International AAAI Conference on Web and Social Media (ICWSM 2026), accepted
      </p>

      <p class="links">
        <a href="https://github.com/TriAnLe171/Meme_Recommendation_Project/blob/main/TriAn_MemeMatch_TechReport.pdf" target="_blank" rel="noopener">Paper</a>
      </p>
    </article>
  </section>

  <section class="pub-section">
    <p class="section-label">Manuscripts Under Review</p>

    <article class="pub-item">
      <p class="paper-title">Coming soon</p>

      <p class="venue">
        Additional manuscripts under review will be listed here.
      </p>
    </article>
  </section>
</div>