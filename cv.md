---
layout: page
permalink: /assets/
---
<style>
  .post-title,
  .page-heading {
    display: none;
  }
</style>

<!-- ===== CV Page Styles (matches Home theme + dark mode) ===== -->
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

  .wrap{
    display:flex;
    flex-direction:column;
    gap:1rem;
  }

  .card{
    background:var(--card);
    border:1px solid var(--border);
    border-radius:16px;
    padding:1rem 1.1rem;
    box-shadow: var(--shadow);
  }

  .title{
    margin:.1rem 0 .35rem 0;
  }
  .muted{ color:var(--muted); }

  .btnrow{
    display:flex;
    flex-wrap:wrap;
    gap:.6rem;
    margin-top:.7rem;
  }
  .btn{
    display:inline-flex;
    align-items:center;
    gap:.5rem;
    padding:.55rem .85rem;
    border-radius:999px;
    border:1px solid var(--border);
    background:var(--bg);
    color:var(--text);
    box-shadow: var(--shadow);
    font-weight:600;
  }
  .btn:hover{ text-decoration:none; }

  .btn.primary{
    background: var(--accent);
    border-color: var(--accent);
    color: #ffffff;
  }

  .grid{
    display:grid;
    grid-template-columns: 1.2fr .8fr;
    gap:1rem;
  }
  @media (max-width: 860px){
    .grid{ grid-template-columns: 1fr; }
  }

  .kv{
    margin:.6rem 0 0 0;
    padding:0;
    list-style:none;
  }
  .kv li{
    display:flex;
    gap:.65rem;
    padding:.35rem 0;
    border-top:1px solid var(--border);
  }
  .kv li:first-child{ border-top:none; }
  .k{
    min-width: 84px;
    font-weight:700;
    color:var(--text);
  }
  .v{
    color:var(--muted);
    word-break: break-word;
  }

  .note{
    border:1px dashed var(--border);
    background: linear-gradient(180deg, rgba(37,99,235,.07), transparent);
    padding:.85rem 1rem;
    border-radius:16px;
  }
  html[data-theme="dark"] .note{
    background: linear-gradient(180deg, rgba(96,165,250,.12), transparent);
  }
</style>

<div class="wrap">

  <div class="card">
    <h2 class="title">Curriculum Vitae</h2>
    <div class="muted">
      Download the latest PDF version, or quickly open it in a new tab.
    </div>

    <div class="btnrow">
      <a class="btn primary" href="/assets/2025_Tri_An_Le_CV_GS.pdf" target="_blank" rel="noopener">
        ⬇️ Download PDF
      </a>
      <a class="btn" href="/assets/2025_Tri_An_Le_CV_GS.pdf" target="_blank" rel="noopener">
        👀 View in browser
      </a>
    </div>

    <div class="note" style="margin-top:1rem;">
      <div style="font-weight:700; margin-bottom:.25rem;">Tip</div>
      <div class="muted">
        If the PDF doesn’t open correctly on mobile, use “Download PDF” and open it from your device’s file viewer.
      </div>
    </div>
  </div>

  <div class="grid">

    <div class="card">
      <h3 class="title">Quick Links</h3>
      <div class="muted">
        Useful links related to my work and applications.
      </div>

      <div class="btnrow">
        <a class="btn" href="/publications">📚 Publications</a>
        <a class="btn" href="/">🏠 Home</a>
        <a class="btn" href="https://github.com/TriAnLe171" target="_blank" rel="noopener">💻 GitHub</a>
        <a class="btn" href="https://www.linkedin.com/in/trianle" target="_blank" rel="noopener">💼 LinkedIn</a>
      </div>
    </div>

    <div class="card">
      <h3 class="title">Contact</h3>
      <ul class="kv">
        <li>
          <div class="k">Email</div>
          <div class="v"><a href="mailto:triandole@gmail.com">triandole@gmail.com</a></div>
        </li>
        <li>
          <div class="k">GitHub</div>
          <div class="v"><a href="https://github.com/TriAnLe171" target="_blank" rel="noopener">github.com/TriAnLe171</a></div>
        </li>
        <li>
          <div class="k">LinkedIn</div>
          <div class="v"><a href="https://www.linkedin.com/in/trianle" target="_blank" rel="noopener">linkedin.com/in/trianle</a></div>
        </li>
      </ul>
    </div>

  </div>

</div>