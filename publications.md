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
    margin-bottom:2rem;
  }

  .pub-header h1,
  .pub-header h2{
    margin:0 0 .35rem 0;
  }

  .pub-header p{
    margin:0;
    color:var(--muted);
  }

  .pub-section{
    margin-top:2rem;
  }

  .pub-section h2{
    font-size:1.15rem;
    margin:0 0 1rem 0;
    padding-bottom:.55rem;
    border-bottom:1px solid var(--line);
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
    <p>Selected publications and manuscripts.</p>
  </div>

  <section class="pub-section">
    <h2>Conference Publications</h2>

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
</div>