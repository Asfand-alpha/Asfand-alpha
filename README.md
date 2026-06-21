
<style>
  @import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=JetBrains+Mono:wght@400;600&display=swap');
  .pg-wrap { font-family: 'Space Grotesk', sans-serif; background: #0a0a0f; min-height: 100vh; padding: 0; }
  .banner {
    background: linear-gradient(135deg, #0a0a0f 0%, #0f0f20 40%, #0d1a2e 100%);
    border-bottom: 1px solid #1e2a4a;
    padding: 2.5rem 2rem 2rem;
    text-align: center;
    position: relative;
    overflow: hidden;
  }
  .banner::before {
    content: '';
    position: absolute;
    top: -60px; left: 50%; transform: translateX(-50%);
    width: 400px; height: 200px;
    background: radial-gradient(ellipse, rgba(99,102,241,0.18) 0%, transparent 70%);
  }
  .avatar-ring {
    display: inline-block;
    padding: 3px;
    border-radius: 50%;
    background: conic-gradient(from 0deg, #6366f1, #38bdf8, #a78bfa, #6366f1);
    margin-bottom: 1rem;
    animation: spin 4s linear infinite;
  }
  @keyframes spin { to { transform: rotate(360deg); } }
  .avatar-inner {
    width: 100px; height: 100px;
    border-radius: 50%;
    background: #0f172a;
    border: 3px solid #0a0a0f;
    display: flex; align-items: center; justify-content: center;
    font-size: 2.2rem; font-weight: 700;
    color: #a78bfa;
    font-family: 'JetBrains Mono', monospace;
  }
  .hero-name {
    font-size: 2.6rem; font-weight: 700;
    background: linear-gradient(90deg, #a78bfa, #38bdf8, #a78bfa);
    background-size: 200%;
    -webkit-background-clip: text; -webkit-text-fill-color: transparent;
    animation: shimmer 3s linear infinite;
    margin: 0 0 0.4rem;
    letter-spacing: -1px;
  }
  @keyframes shimmer { to { background-position: 200% center; } }
  .hero-role {
    font-size: 1rem; color: #94a3b8; letter-spacing: 2px;
    text-transform: uppercase; font-weight: 500; margin: 0 0 1.2rem;
    font-family: 'JetBrains Mono', monospace;
  }
  .social-row { display: flex; gap: 10px; justify-content: center; flex-wrap: wrap; margin-bottom: 0.5rem; }
  .social-btn {
    display: flex; align-items: center; gap: 7px;
    padding: 8px 18px; border-radius: 50px;
    font-size: 12px; font-weight: 600; text-transform: uppercase; letter-spacing: 1px;
    cursor: pointer; text-decoration: none;
    border: 1px solid; transition: all 0.2s;
    font-family: 'Space Grotesk', sans-serif;
  }
  .btn-github { background: #0f172a; border-color: #334155; color: #e2e8f0; }
  .btn-github:hover { border-color: #6366f1; color: #a78bfa; }
  .btn-linkedin { background: #0f172a; border-color: #334155; color: #e2e8f0; }
  .btn-linkedin:hover { border-color: #38bdf8; color: #38bdf8; }
  .btn-email { background: #0f172a; border-color: #334155; color: #e2e8f0; }
  .btn-email:hover { border-color: #f472b6; color: #f472b6; }
  .section { padding: 1.5rem 2rem; border-bottom: 1px solid #1e2a4a; }
  .section-label {
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px; font-weight: 600; letter-spacing: 3px;
    text-transform: uppercase; color: #6366f1; margin-bottom: 1rem;
    display: flex; align-items: center; gap: 8px;
  }
  .section-label::after { content: ''; flex: 1; height: 1px; background: linear-gradient(90deg, #1e2a4a, transparent); }
  .about-text { color: #94a3b8; line-height: 1.8; font-size: 14px; }
  .about-text span { color: #c4b5fd; font-weight: 600; }
  .stack-group { margin-bottom: 1.2rem; }
  .stack-title { font-size: 11px; color: #64748b; text-transform: uppercase; letter-spacing: 2px; font-weight: 600; margin-bottom: 10px; font-family: 'JetBrains Mono', monospace; }
  .badges { display: flex; flex-wrap: wrap; gap: 8px; }
  .badge {
    display: flex; align-items: center; gap: 6px;
    padding: 6px 14px; border-radius: 6px;
    font-size: 12px; font-weight: 600;
    letter-spacing: 0.5px;
    border: 1px solid;
    font-family: 'Space Grotesk', sans-serif;
    transition: transform 0.15s;
  }
  .badge:hover { transform: translateY(-2px); }
  .badge-dot { width: 6px; height: 6px; border-radius: 50%; flex-shrink: 0; }
  .b-fe { background: #0c1a2e; border-color: #1e3a5f; color: #38bdf8; }
  .b-fe .badge-dot { background: #38bdf8; }
  .b-be { background: #150d2a; border-color: #2d1a5e; color: #a78bfa; }
  .b-be .badge-dot { background: #a78bfa; }
  .b-ai { background: #0d1f1a; border-color: #1a4a3a; color: #34d399; }
  .b-ai .badge-dot { background: #34d399; }
  .b-tools { background: #1a1208; border-color: #3d2c0a; color: #fbbf24; }
  .b-tools .badge-dot { background: #fbbf24; }
  .stats-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
  .stat-card {
    background: #0f172a; border: 1px solid #1e2a4a; border-radius: 10px;
    padding: 1rem 1.2rem; text-align: center;
  }
  .stat-num { font-size: 1.8rem; font-weight: 700; color: #a78bfa; font-family: 'JetBrains Mono', monospace; }
  .stat-lbl { font-size: 11px; color: #64748b; text-transform: uppercase; letter-spacing: 1.5px; margin-top: 2px; font-weight: 600; }
  .footer-banner {
    background: linear-gradient(135deg, #0d1a2e, #0a0a0f);
    padding: 1.5rem 2rem; text-align: center;
    border-top: 1px solid #1e2a4a;
  }
  .connect-text { font-size: 12px; color: #475569; font-family: 'JetBrains Mono', monospace; letter-spacing: 1px; }
  .pulse { display: inline-block; width: 8px; height: 8px; border-radius: 50%; background: #34d399; margin-right: 6px; animation: pulse 2s ease-in-out infinite; }
  @keyframes pulse { 0%,100%{opacity:1;} 50%{opacity:0.3;} }
  .tag-mono { font-family: 'JetBrains Mono', monospace; }
</style>

<div class="pg-wrap">
  <div class="banner">
    <div class="avatar-ring">
      <div class="avatar-inner">A</div>
    </div>
    <div class="hero-name">Asfand</div>
    <div class="hero-role">Full-Stack · Automation · AI</div>
    <div class="social-row">
      <a class="social-btn btn-github" href="#">
        <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2C6.48 2 2 6.48 2 12c0 4.42 2.87 8.17 6.84 9.5.5.09.68-.22.68-.48v-1.7c-2.78.6-3.37-1.34-3.37-1.34-.46-1.16-1.11-1.47-1.11-1.47-.91-.62.07-.61.07-.61 1 .07 1.53 1.03 1.53 1.03.89 1.52 2.34 1.08 2.91.83.09-.65.35-1.09.63-1.34-2.22-.25-4.56-1.11-4.56-4.94 0-1.09.39-1.98 1.03-2.68-.1-.25-.45-1.27.1-2.64 0 0 .84-.27 2.75 1.02A9.56 9.56 0 0112 6.8c.85.004 1.7.115 2.5.337 1.91-1.29 2.75-1.02 2.75-1.02.55 1.37.2 2.39.1 2.64.64.7 1.03 1.59 1.03 2.68 0 3.84-2.34 4.68-4.57 4.93.36.31.68.92.68 1.85v2.74c0 .27.18.58.69.48A10.01 10.01 0 0022 12c0-5.52-4.48-10-10-10z"/></svg>
        GitHub
      </a>
      <a class="social-btn btn-linkedin" href="#">
        <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M20.45 20.45h-3.55v-5.57c0-1.33-.03-3.04-1.85-3.04-1.85 0-2.13 1.45-2.13 2.94v5.67H9.37V9h3.41v1.56h.05c.47-.9 1.63-1.85 3.35-1.85 3.58 0 4.24 2.36 4.24 5.43v6.31zM5.34 7.43a2.06 2.06 0 110-4.12 2.06 2.06 0 010 4.12zM7.12 20.45H3.57V9h3.55v11.45zM22.22 0H1.77C.79 0 0 .77 0 1.72v20.56C0 23.23.79 24 1.77 24h20.45C23.2 24 24 23.23 24 22.28V1.72C24 .77 23.2 0 22.22 0z"/></svg>
        LinkedIn
      </a>
      <a class="social-btn btn-email" href="#">
        <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
        Email
      </a>
    </div>
    <div style="margin-top:10px; font-size:12px; color:#475569; font-family:'JetBrains Mono',monospace;">
      <span class="pulse"></span>open to opportunities
    </div>
  </div>

  <div class="section">
    <div class="section-label">about</div>
    <div class="about-text">
      I build <span>modern web applications</span> end-to-end — from pixel-perfect <span>Angular</span> frontends to rock-solid <span>.NET APIs</span>. I automate the boring stuff with <span>Playwright</span>, and push the frontier with <span>Agentic AI</span> systems that think and act autonomously.
    </div>
  </div>

  <div class="section">
    <div class="section-label">tech stack</div>
    <div class="stack-group">
      <div class="stack-title">Frontend</div>
      <div class="badges">
        <span class="badge b-fe"><span class="badge-dot"></span>HTML5</span>
        <span class="badge b-fe"><span class="badge-dot"></span>CSS3</span>
        <span class="badge b-fe"><span class="badge-dot"></span>JavaScript</span>
        <span class="badge b-fe"><span class="badge-dot"></span>TypeScript</span>
        <span class="badge b-fe"><span class="badge-dot"></span>Angular</span>
      </div>
    </div>
    <div class="stack-group">
      <div class="stack-title">Backend</div>
      <div class="badges">
        <span class="badge b-be"><span class="badge-dot"></span>.NET</span>
        <span class="badge b-be"><span class="badge-dot"></span>C#</span>
        <span class="badge b-be"><span class="badge-dot"></span>ASP.NET Web API</span>
        <span class="badge b-be"><span class="badge-dot"></span>MVC</span>
      </div>
    </div>
    <div class="stack-group">
      <div class="stack-title">Automation & AI</div>
      <div class="badges">
        <span class="badge b-ai"><span class="badge-dot"></span>Playwright</span>
        <span class="badge b-ai"><span class="badge-dot"></span>Python</span>
        <span class="badge b-ai"><span class="badge-dot"></span>Agentic AI</span>
        <span class="badge b-ai"><span class="badge-dot"></span>LangChain</span>
      </div>
    </div>
    <div class="stack-group">
      <div class="stack-title">Tools</div>
      <div class="badges">
        <span class="badge b-tools"><span class="badge-dot"></span>Git</span>
        <span class="badge b-tools"><span class="badge-dot"></span>GitHub</span>
        <span class="badge b-tools"><span class="badge-dot"></span>VS Code</span>
        <span class="badge b-tools"><span class="badge-dot"></span>Visual Studio</span>
      </div>
    </div>
  </div>

  <div class="section">
    <div class="section-label">github stats</div>
    <div class="stats-grid">
      <div class="stat-card"><div class="stat-num tag-mono">120+</div><div class="stat-lbl">Commits</div></div>
      <div class="stat-card"><div class="stat-num tag-mono">18+</div><div class="stat-lbl">Repos</div></div>
      <div class="stat-card"><div class="stat-num tag-mono">4+</div><div class="stat-lbl">Languages</div></div>
      <div class="stat-card"><div class="stat-num tag-mono">∞</div><div class="stat-lbl">Coffee ☕</div></div>
    </div>
    <div style="margin-top:1rem; text-align:center; font-size:11px; color:#334155; font-family:'JetBrains Mono',monospace;">(live stats powered by github-readme-stats in the actual README)</div>
  </div>

  <div class="footer-banner">
    <div class="connect-text">// let's build something remarkable together</div>
  </div>
</div>
