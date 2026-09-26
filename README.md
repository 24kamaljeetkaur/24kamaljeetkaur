<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Kamaljeet Kaur — Python & Django Developer</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@500;700&family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet">
<style>
  :root{
    --bg:#0B0F1A; --bg2:#10162A; --panel:#131A2E; --border:#232C46;
    --text:#E7ECF7; --muted:#8E98B8;
    --py-blue:#4B8BBE; --py-yellow:#FFD43B; --accent:#7FE0C9;
    box-sizing:border-box; padding-top:env(safe-area-inset-top,0px); padding-bottom:env(safe-area-inset-bottom,0px);
  }
  @media (prefers-color-scheme: light){
    :root:not([data-theme="dark"]){ --bg:#F5F7FC; --bg2:#EDF0F9; --panel:#FFFFFF; --border:#DCE2F2; --text:#111528; --muted:#5B637F; }
  }
  :root[data-theme="dark"]{ --bg:#0B0F1A; --bg2:#10162A; --panel:#131A2E; --border:#232C46; --text:#E7ECF7; --muted:#8E98B8; }
  * { box-sizing:border-box; }
  html{ scroll-padding-top:env(safe-area-inset-top,0px); scroll-behavior:smooth; }
  html,body{ height:100%; }
  body{
    margin:0; background:radial-gradient(1200px 600px at 15% -10%, var(--bg2), var(--bg) 60%);
    color:var(--text); font-family:'Space Grotesk',sans-serif; overflow-x:hidden;
  }
  .wrap{ max-width:1000px; margin:0 auto; padding:0 24px; }
  a{ color:var(--py-blue); }

  /* ---------- HERO / MOTION GRAPHICS ---------- */
  .hero{ position:relative; padding:64px 0 40px; overflow:hidden; }
  .orb{ position:absolute; border-radius:50%; filter:blur(60px); opacity:.35; animation:float 14s ease-in-out infinite; }
  .orb1{ width:260px; height:260px; background:var(--py-blue); top:-60px; right:-40px; animation-duration:16s; }
  .orb2{ width:200px; height:200px; background:var(--py-yellow); bottom:-40px; left:-30px; animation-duration:12s; animation-delay:-4s; }
  .orb3{ width:150px; height:150px; background:var(--accent); top:40%; right:20%; animation-duration:18s; animation-delay:-8s; }
  @keyframes float{
    0%,100%{ transform:translate(0,0) scale(1); }
    50%{ transform:translate(-20px,25px) scale(1.08); }
  }
  @media (prefers-reduced-motion: reduce){ .orb{ animation:none; } }

  .eyebrow{ font-family:'JetBrains Mono',monospace; color:var(--muted); font-size:13px; }
  h1{ font-size:clamp(30px,5vw,46px); line-height:1.05; margin:10px 0 6px; }
  h1 .hl{ color:var(--py-blue); }
  .role{ color:var(--muted); font-size:17px; max-width:60ch; margin:0 0 28px; }

  .terminal{
    position:relative; background:var(--panel); border:1px solid var(--border); border-radius:10px;
    font-family:'JetBrains Mono',monospace; font-size:14px; overflow:hidden; box-shadow:0 20px 60px rgba(0,0,0,.35);
  }
  .term-bar{ display:flex; gap:6px; padding:10px 14px; border-bottom:1px solid var(--border); }
  .dot{ width:10px; height:10px; border-radius:50%; background:var(--border); }
  .term-body{ padding:18px 20px 24px; min-height:132px; }
  .term-line{ color:var(--muted); margin:0 0 6px; }
  .term-line b{ color:var(--py-yellow); font-weight:500; }
  .type{
    display:inline-block; overflow:hidden; white-space:nowrap; border-right:2px solid var(--accent);
    width:0; animation:type 3.6s steps(44,end) forwards, blink .8s step-end infinite;
    color:var(--text);
  }
  @keyframes type{ to{ width:44ch; } }
  @keyframes blink{ 50%{ border-color:transparent; } }
  @media (prefers-reduced-motion: reduce){ .type{ animation:none; width:44ch; } }

  .links{ margin-top:22px; display:flex; flex-wrap:wrap; gap:14px; font-family:'JetBrains Mono',monospace; font-size:13px; }
  .links a{ text-decoration:none; border:1px solid var(--border); padding:7px 12px; border-radius:6px; color:var(--text); }
  .links a:hover{ border-color:var(--py-blue); }

  /* ---------- SECTIONS ---------- */
  section{ padding:48px 0; border-top:1px solid var(--border); }
  h2{ font-size:22px; margin:0 0 28px; }
  h2 .num{ font-family:'JetBrains Mono',monospace; color:var(--muted); font-weight:400; margin-right:10px; font-size:15px; }

  /* ---------- ANIMATED ZIGZAG TIMELINE ---------- */
  :root{ --cyan:#38BDF8; }
  .tl{ position:relative; padding:10px 0; }
  .tl-line{
    position:absolute; left:50%; top:0; bottom:0; width:2px; transform:translateX(-50%);
    background:linear-gradient(var(--cyan),var(--cyan)) no-repeat; background-size:100% 0%;
    animation:drawline 2.6s ease-out forwards; animation-delay:.2s; opacity:.55;
  }
  @keyframes drawline{ to{ background-size:100% 100%; } }
  .tl-row{
    position:relative; display:grid; grid-template-columns:1fr 56px 1fr; align-items:start;
    gap:0 18px; margin-bottom:34px; opacity:0; transform:translateY(16px);
    animation:reveal .7s ease-out forwards;
  }
  @keyframes reveal{ to{ opacity:1; transform:translateY(0); } }
  .tl-row:nth-child(2){ animation-delay:.4s; } .tl-row:nth-child(3){ animation-delay:.8s; }
  .tl-row:nth-child(4){ animation-delay:1.2s; } .tl-row:nth-child(5){ animation-delay:1.6s; }
  .tl-row:nth-child(6){ animation-delay:2.0s; } .tl-row:nth-child(7){ animation-delay:2.4s; }
  @media (prefers-reduced-motion: reduce){ .tl-row,.tl-line{ animation:none; opacity:1; transform:none; background-size:100% 100%; } }
  .tl-node{
    grid-column:2; justify-self:center; width:52px; height:52px; border-radius:50%;
    background:var(--bg2); border:2px solid var(--cyan); box-shadow:0 0 18px rgba(56,189,248,.35);
    display:flex; align-items:center; justify-content:center;
    font-family:'JetBrains Mono',monospace; font-weight:700; color:var(--cyan); font-size:15px;
  }
  .tl-row.current .tl-node{ border-color:var(--py-yellow); color:var(--py-yellow); box-shadow:0 0 18px rgba(255,212,59,.4); }
  .tl-card{
    background:var(--panel); border:1px solid var(--border); border-radius:14px; padding:16px 18px;
  }
  .tl-row.left .tl-card{ grid-column:1; }
  .tl-row.right .tl-card{ grid-column:3; }
  .tl-label{ font-family:'JetBrains Mono',monospace; font-size:11px; letter-spacing:.04em; color:var(--cyan); margin:0 0 6px; }
  .tl-title{ font-weight:700; font-size:17px; margin:0 0 8px; }
  .tl-desc{ font-size:13.5px; color:var(--muted); margin:0; line-height:1.5; }
  @media (max-width:640px){
    .tl-row{ grid-template-columns:44px 1fr; gap:0 12px; }
    .tl-node{ grid-column:1; width:40px; height:40px; font-size:13px; }
    .tl-row.left .tl-card, .tl-row.right .tl-card{ grid-column:2; }
    .tl-line{ left:20px; }
  }

  /* ---------- STACK ---------- */
  .chips{ display:flex; flex-wrap:wrap; gap:8px; }
  .chip{ font-family:'JetBrains Mono',monospace; font-size:12.5px; padding:6px 10px; border:1px solid var(--border); border-radius:20px; color:var(--muted); }

  footer{ padding:36px 0 60px; text-align:center; color:var(--muted); font-family:'JetBrains Mono',monospace; font-size:12.5px; }
</style>
</head>
<body>
<div class="wrap">

  <div class="hero">
    <div class="orb orb1"></div><div class="orb orb2"></div><div class="orb orb3"></div>
    <p class="eyebrow">~/kamaljeet-kaur</p>
    <h1>Building with <span class="hl">Python</span>, Django &amp; applied AI.</h1>
    <p class="role">Full-stack engineer who ships production Django systems and prototypes agentic AI on the side — from a live financial SaaS platform to Gemini-powered image pipelines.</p>

    <div class="terminal">
      <div class="term-bar"><span class="dot"></span><span class="dot"></span><span class="dot"></span></div>
      <div class="term-body">
        <p class="term-line">$ whoami</p>
        <p class="term-line"><span class="type">Python/Django engineer, MCA, Amritsar, India</span></p>
        <p class="term-line" style="margin-top:14px;">$ cat focus.txt <b>#</b> REST APIs · LangChain/RAG · CNNs</p>
      </div>
    </div>

    <div class="links">
      <a href="https://linkedin.com/in/kamaljeet-kaur-624249181" target="_blank" rel="noopener">LinkedIn</a>
      <a href="https://github.com/24kamaljeetkaur" target="_blank" rel="noopener">GitHub</a>
      <a href="https://design-buildsolution.web.app/kamaljeet-resume" target="_blank" rel="noopener">Portfolio</a>
      <a href="mailto:kaurkamaljeet.mehra@gmail.com">Email</a>
    </div>
  </div>

  <section>
    <h2><span class="num">01</span>Journey</h2>
    <div class="tl">
      <div class="tl-line"></div>

      <div class="tl-row left">
        <div class="tl-card">
          <p class="tl-label">2017 · BEGINNINGS</p>
          <p class="tl-title">WordPress Developer</p>
          <p class="tl-desc">Design To Webber &amp; OXO Solution — delivered WordPress themes, plugins and full sites for international clients, start to finish.</p>
        </div>
        <div class="tl-node">17</div>
        <div></div>
      </div>

      <div class="tl-row right">
        <div></div>
        <div class="tl-node">19</div>
        <div class="tl-card">
          <p class="tl-label">2019 · FRONTEND SYSTEMS</p>
          <p class="tl-title">Web Designer &amp; Trainer</p>
          <p class="tl-desc">CKD Institute of Management and Technology — replaced paper-based college workflows with Angular apps, and trained staff to use them.</p>
        </div>
      </div>

      <div class="tl-row left">
        <div class="tl-card">
          <p class="tl-label">2021 · FULL-STACK WEB</p>
          <p class="tl-title">Web Developer</p>
          <p class="tl-desc">Deepdive Innovations — owned client web projects end-to-end, from requirements through deployment, using HTML5, JS and Angular.</p>
        </div>
        <div class="tl-node">21</div>
        <div></div>
      </div>

      <div class="tl-row right">
        <div></div>
        <div class="tl-node">23</div>
        <div class="tl-card">
          <p class="tl-label">2023 · BUSINESS SYSTEMS</p>
          <p class="tl-title">Web Developer</p>
          <p class="tl-desc">Amandeep Group of Hospitals — built a multi-site hospital digital ecosystem (15+ portals), a lead-capture dashboard, and Angular reporting tools.</p>
        </div>
      </div>

      <div class="tl-row left">
        <div class="tl-card">
          <p class="tl-label">2025 · SAAS OWNERSHIP</p>
          <p class="tl-title">Full Stack Engineer</p>
          <p class="tl-desc">Vriddhi Advisors Ltd. (Sofficio.com) — sole full-stack owner of a financial SaaS platform across 5 modules: API design, auth, SQL performance, production debugging.</p>
        </div>
        <div class="tl-node">25</div>
        <div></div>
      </div>

      <div class="tl-row right current">
        <div></div>
        <div class="tl-node">26</div>
        <div class="tl-card">
          <p class="tl-label">2026 · AI EXPANSION — CURRENT</p>
          <p class="tl-title">GenAI &amp; Agentic Systems</p>
          <p class="tl-desc">Building on the full-stack foundation with LangChain, RAG, LangGraph and MCP — including a self-hosted lead agent and Gemini Vision image pipelines.</p>
        </div>
      </div>

    </div>
  </section>

  <section>
    <h2><span class="num">02</span>Stack</h2>
    <div class="chips">
      <span class="chip">Python</span><span class="chip">Django</span><span class="chip">Django ORM</span>
      <span class="chip">REST APIs</span><span class="chip">PostgreSQL</span><span class="chip">MySQL</span>
      <span class="chip">NumPy / Pandas</span><span class="chip">Gemini Vision API</span>
      <span class="chip">LangChain / RAG</span><span class="chip">TensorFlow / Keras</span>
      <span class="chip">Angular</span><span class="chip">Celery + Redis</span><span class="chip">GCP</span>
    </div>
  </section>

  <footer>built from the resume of Kamaljeet Kaur · Amritsar, Punjab</footer>
</div>
</body>
</html>
