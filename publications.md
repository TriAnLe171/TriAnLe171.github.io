---
layout: page
title: "Publications"
permalink: /publications/
---

<!-- ===== Publications Page Styles (matches Home/CV theme + dark mode) ===== -->
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

  body{ background:var(--bg); color:var(--text); }
  a{ color:var(--accent); text-decoration:none; }
  a:hover{ text-decoration:underline; }

  .wrap{ display:flex; flex-direction:column; gap:1rem; }
  .card{
    background:var(--card);
    border:1px solid var(--border);
    border-radius:16px;
    padding:1rem 1.1rem;
    box-shadow: var(--shadow);
  }
  .title{ margin:.1rem 0 .35rem 0; }
  .muted{ color:var(--muted); }

  .sectionhead{
    display:flex;
    align-items:baseline;
    justify-content:space-between;
    gap:1rem;
    flex-wrap:wrap;
  }
  .pillrow{ display:flex; gap:.45rem; flex-wrap:wrap; }
  .pill{
    display:inline-flex;
    align-items:center;
    gap:.35rem;
    padding:.18rem .55rem;
    border-radius:999px;
    border:1px solid var(--border);
    background:var(--bg);
    color:var(--muted);
    font-size:.88rem;
    line-height:1.4;
  }
  .pill.status{
    border-color: rgba(37,99,235,.35);
    background: rgba(37,99,235,.08);
    color: var(--text);
  }
  html[data-theme="dark"] .pill.status{
    border-color: rgba(96,165,250,.35);
    background: rgba(96,165,250,.12);
  }

  .pub{
    display:flex;
    flex-direction:column;
    gap:.35rem;
  }
  .pub .paper-title{
    font-weight:800;
    font-size:1.05rem;
    margin:0;
  }
  .pub .authors{
    margin:0;
    color:var(--muted);
  }
  .pub .venue{
    margin:0;
    color:var(--muted);
  }

  .btnrow{
    display:flex;
    flex-wrap:wrap;
    gap:.6rem;
    margin-top:.55rem;
  }
  .btn{
    display:inline-flex;
    align-items:center;
    gap:.5rem;
    padding:.5rem .85rem;
    border-radius:999px;
    border:1px solid var(--border);
    background:var(--bg);
    color:var(--text);
    box-shadow: var(--shadow);
    font-weight:650;
  }
  .btn:hover{ text-decoration:none; }
  .btn.primary{
    background: var(--accent);
    border-color: var(--accent);
    color:#ffffff;
  }

  .divider{
    height:1px;
    background:var(--border);
    margin:.2rem 0 0 0;
  }
</style>

<div class="wrap">

  <div class="card">
    <div class="sectionhead">
      <div>
        <h2 class="title">Publications</h2>
        <div class="muted">
          Selected papers and manuscripts.
        </div>
      </div>
      <div class="pillrow">
        <span class="pill">📌 Multimodal NLP</span>
        <span class="pill">🔎 Retrieval</span>
        <span class="pill">🧠 Social media</span>
      </div>
    </div>
  </div>

  <div class="card">
    <div class="sectionhead">
      <h3 class="title" style="margin-bottom:.2rem;">Preprints / Under Review</h3>
      <span class="pill status">ICWSM 2026 submission (under review)</span>
    </div>
    <div class="divider"></div>

    <div class="pub" style="margin-top:.9rem;">
      <p class="paper-title">
        MemeMatch: A Large-Scale Dual-Context Multimodal Dataset and Retrieval System for Internet Memes
      </p>

      <p class="authors">
        <b>Do Tri An Le</b>, Donát Ákos Köller, Qixin Deng, Roland Molontay
      </p>

      <p class="venue">
        ICWSM 2026 submission (under review)
      </p>

      <div class="btnrow">
        <a class="btn primary" href="https://github.com/TriAnLe171/Meme_Recommendation_Project/blob/main/TriAn_MemeMatch_TechReport.pdf" target="_blank" rel="noopener">
          📄 Paper (PDF)
        </a>
      </div>
    </div>
  </div>

</div>