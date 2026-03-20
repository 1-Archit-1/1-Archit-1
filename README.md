<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Archit Sengupta — GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Mono:wght@300;400;500&family=Syne:wght@400;600;700;800&display=swap" rel="stylesheet"/>
<style>
  :root {
    --bg: #0a0c10;
    --surface: #111318;
    --border: #1e2230;
    --accent: #3b82f6;
    --accent2: #06b6d4;
    --accent3: #8b5cf6;
    --text: #e2e8f0;
    --muted: #64748b;
    --green: #10b981;
    --orange: #f59e0b;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Mono', monospace;
    font-size: 14px;
    line-height: 1.7;
    max-width: 860px;
    margin: 0 auto;
    padding: 48px 32px;
  }

  /* ── HEADER ────────────────────────────────── */
  .header {
    position: relative;
    padding: 48px 40px;
    border: 1px solid var(--border);
    border-radius: 16px;
    background: linear-gradient(135deg, #111318 0%, #0d1117 100%);
    overflow: hidden;
    margin-bottom: 32px;
  }

  .header::before {
    content: '';
    position: absolute;
    top: -80px; right: -80px;
    width: 300px; height: 300px;
    background: radial-gradient(circle, rgba(59,130,246,0.12) 0%, transparent 70%);
    pointer-events: none;
  }
  .header::after {
    content: '';
    position: absolute;
    bottom: -60px; left: -60px;
    width: 250px; height: 250px;
    background: radial-gradient(circle, rgba(139,92,246,0.1) 0%, transparent 70%);
    pointer-events: none;
  }

  .header-top {
    display: flex;
    align-items: flex-start;
    gap: 28px;
    flex-wrap: wrap;
  }

  .avatar {
    width: 72px; height: 72px;
    border-radius: 50%;
    background: linear-gradient(135deg, var(--accent), var(--accent3));
    display: flex; align-items: center; justify-content: center;
    font-family: 'Syne', sans-serif;
    font-size: 28px;
    font-weight: 800;
    color: white;
    flex-shrink: 0;
    box-shadow: 0 0 0 3px rgba(59,130,246,0.25);
  }

  .header-text h1 {
    font-family: 'Syne', sans-serif;
    font-size: 32px;
    font-weight: 800;
    color: #f8fafc;
    letter-spacing: -0.5px;
    line-height: 1.1;
  }

  .header-text .tagline {
    margin-top: 6px;
    color: var(--accent2);
    font-size: 13px;
    letter-spacing: 0.08em;
    text-transform: uppercase;
  }

  .status-row {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-top: 20px;
  }

  .badge {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    background: rgba(255,255,255,0.04);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 5px 12px;
    font-size: 12px;
    color: var(--muted);
  }
  .badge .dot {
    width: 7px; height: 7px;
    border-radius: 50%;
    background: var(--green);
    box-shadow: 0 0 6px var(--green);
    animation: pulse 2s ease-in-out infinite;
  }
  @keyframes pulse {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.4; }
  }

  .bio {
    margin-top: 24px;
    color: #94a3b8;
    font-size: 13.5px;
    max-width: 600px;
    border-left: 2px solid var(--accent);
    padding-left: 16px;
  }

  /* ── SECTION WRAPPER ───────────────────────── */
  .section {
    border: 1px solid var(--border);
    border-radius: 12px;
    background: var(--surface);
    margin-bottom: 20px;
    overflow: hidden;
  }

  .section-header {
    display: flex;
    align-items: center;
    gap: 10px;
    padding: 16px 24px;
    border-bottom: 1px solid var(--border);
    background: rgba(255,255,255,0.02);
  }

  .section-icon {
    font-size: 16px;
  }

  .section-title {
    font-family: 'Syne', sans-serif;
    font-size: 13px;
    font-weight: 700;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--text);
  }

  .section-body {
    padding: 24px;
  }

  /* ── HIGHLIGHTS ────────────────────────────── */
  .highlights {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 14px;
  }

  .highlight-card {
    background: rgba(255,255,255,0.025);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 16px 18px;
    position: relative;
    overflow: hidden;
    transition: border-color 0.2s;
  }
  .highlight-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 3px; height: 100%;
    border-radius: 2px 0 0 2px;
  }
  .highlight-card.blue::before  { background: var(--accent); }
  .highlight-card.cyan::before  { background: var(--accent2); }
  .highlight-card.purple::before { background: var(--accent3); }
  .highlight-card.green::before  { background: var(--green); }

  .highlight-label {
    font-size: 10px;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 4px;
  }
  .highlight-value {
    font-family: 'Syne', sans-serif;
    font-size: 14px;
    font-weight: 700;
    color: var(--text);
  }

  /* ── TECH GRID ─────────────────────────────── */
  .tech-category {
    margin-bottom: 20px;
  }
  .tech-category:last-child { margin-bottom: 0; }

  .tech-label {
    font-size: 10px;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 10px;
  }

  .pill-row {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .pill {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 5px 12px;
    border-radius: 6px;
    font-size: 12px;
    font-weight: 500;
    border: 1px solid transparent;
    transition: all 0.15s;
  }

  .pill-blue   { background: rgba(59,130,246,0.1);  border-color: rgba(59,130,246,0.25);  color: #93c5fd; }
  .pill-cyan   { background: rgba(6,182,212,0.1);   border-color: rgba(6,182,212,0.25);   color: #67e8f9; }
  .pill-purple { background: rgba(139,92,246,0.1);  border-color: rgba(139,92,246,0.25);  color: #c4b5fd; }
  .pill-green  { background: rgba(16,185,129,0.1);  border-color: rgba(16,185,129,0.25);  color: #6ee7b7; }
  .pill-orange { background: rgba(245,158,11,0.1);  border-color: rgba(245,158,11,0.25);  color: #fcd34d; }

  /* ── TERMINAL BLOCK ────────────────────────── */
  .terminal {
    background: #080b0f;
    border: 1px solid #1e2230;
    border-radius: 10px;
    overflow: hidden;
  }

  .terminal-bar {
    display: flex;
    align-items: center;
    gap: 7px;
    padding: 10px 14px;
    background: #0f1218;
    border-bottom: 1px solid var(--border);
  }
  .terminal-bar span {
    width: 11px; height: 11px;
    border-radius: 50%;
  }
  .t-red    { background: #ff5f57; }
  .t-yellow { background: #febc2e; }
  .t-green  { background: #28c840; }

  .terminal-body {
    padding: 18px 20px;
    font-size: 12.5px;
    line-height: 2;
  }

  .t-prompt { color: var(--accent); }
  .t-cmd    { color: var(--text); }
  .t-key    { color: var(--accent2); }
  .t-val    { color: #a3e635; }
  .t-str    { color: #fb923c; }
  .t-comment{ color: var(--muted); }
  .t-sep { color: var(--border); user-select: none; }

  /* ── INTERESTS ─────────────────────────────── */
  .interests {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
  }

  .interest-chip {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 8px 16px;
    background: rgba(255,255,255,0.03);
    border: 1px solid var(--border);
    border-radius: 999px;
    font-size: 12.5px;
    color: #94a3b8;
  }

  /* ── CONNECT ───────────────────────────────── */
  .connect-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
  }

  .connect-card {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    padding: 12px 20px;
    background: rgba(255,255,255,0.03);
    border: 1px solid var(--border);
    border-radius: 10px;
    text-decoration: none;
    color: var(--text);
    font-size: 13px;
    transition: border-color 0.2s, background 0.2s;
  }
  .connect-card:hover {
    border-color: var(--accent);
    background: rgba(59,130,246,0.06);
  }

  .connect-icon {
    font-size: 18px;
  }

  .connect-label {
    font-size: 10px;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    color: var(--muted);
  }
  .connect-value {
    font-size: 13px;
    color: var(--text);
  }

  /* ── DIVIDER ───────────────────────────────── */
  .divider {
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--border), transparent);
    margin: 4px 0;
  }

  /* ── FOOTER ────────────────────────────────── */
  .footer {
    text-align: center;
    margin-top: 32px;
    font-size: 11px;
    color: var(--muted);
    letter-spacing: 0.08em;
  }
</style>
</head>
<body>

<!-- ═══════════════ HEADER ═══════════════ -->
<div class="header">
  <div class="header-top">
    <div class="avatar">AS</div>
    <div class="header-text">
      <h1>Archit Sengupta</h1>
      <div class="tagline">Backend Engineer · Data Systems · Service Architecture</div>
    </div>
  </div>

  <div class="status-row">
    <div class="badge"><span class="dot"></span> Open to Connect</div>
    <div class="badge">📍 Atlanta, GA</div>
    <div class="badge">🏢 Zurich Insurance Group</div>
    <div class="badge">🎓 Georgia Tech MSCS · 4.0 GPA</div>
  </div>

  <p class="bio">
    Backend-focused engineer who loves wrangling complex data, designing efficient algorithms,
    and building scalable platforms. Whether it's dialing in database performance or
    architecting a new system from scratch — I enjoy solving hard problems from the ground up.
  </p>
</div>


<!-- ═══════════════ HIGHLIGHTS ═══════════════ -->
<div class="section">
  <div class="section-header">
    <span class="section-icon">✦</span>
    <span class="section-title">At a Glance</span>
  </div>
  <div class="section-body">
    <div class="highlights">
      <div class="highlight-card blue">
        <div class="highlight-label">Degree</div>
        <div class="highlight-value">M.S. Computer Science</div>
      </div>
      <div class="highlight-card cyan">
        <div class="highlight-label">Institution</div>
        <div class="highlight-value">Georgia Tech</div>
      </div>
      <div class="highlight-card purple">
        <div class="highlight-label">CGPA</div>
        <div class="highlight-value">4.0 / 4.0</div>
      </div>
      <div class="highlight-card green">
        <div class="highlight-label">Current Role</div>
        <div class="highlight-value">SWE · Catastrophe Modeling</div>
      </div>
    </div>
  </div>
</div>


<!-- ═══════════════ TECH STACK ═══════════════ -->
<div class="section">
  <div class="section-header">
    <span class="section-icon">⚙</span>
    <span class="section-title">Tech Stack</span>
  </div>
  <div class="section-body">

    <div class="tech-category">
      <div class="tech-label">Languages</div>
      <div class="pill-row">
        <span class="pill pill-blue">🐍 Python</span>
        <span class="pill pill-blue">📊 R</span>
        <span class="pill pill-orange">JS JavaScript</span>
        <span class="pill pill-purple">🐘 PHP</span>
      </div>
    </div>

    <div class="divider" style="margin: 18px 0;"></div>

    <div class="tech-category">
      <div class="tech-label">Databases</div>
      <div class="pill-row">
        <span class="pill pill-cyan">🐘 PostgreSQL</span>
        <span class="pill pill-cyan">🗄 MS SQL Server</span>
        <span class="pill pill-green">🍃 MongoDB</span>
        <span class="pill pill-orange">⚡ Redis</span>
      </div>
    </div>

    <div class="divider" style="margin: 18px 0;"></div>

    <div class="tech-category">
      <div class="tech-label">Frameworks &amp; Libraries</div>
      <div class="pill-row">
        <span class="pill pill-green">⚡ FastAPI</span>
        <span class="pill pill-blue">📈 R-Shiny</span>
        <span class="pill pill-purple">🔵 Django</span>
        <span class="pill pill-orange">🔴 Laravel</span>
        <span class="pill pill-cyan">⚛ React</span>
        <span class="pill pill-blue">🔗 REST APIs</span>
      </div>
    </div>

    <div class="divider" style="margin: 18px 0;"></div>

    <div class="tech-category">
      <div class="tech-label">Infrastructure &amp; DevOps</div>
      <div class="pill-row">
        <span class="pill pill-blue">☁ Azure</span>
        <span class="pill pill-orange">☁ AWS</span>
        <span class="pill pill-cyan">🐳 Docker</span>
        <span class="pill pill-green">🔁 GitHub Actions</span>
        <span class="pill pill-purple">🔄 Airflow</span>
        <span class="pill pill-blue">🌐 Nginx</span>
      </div>
    </div>

  </div>
</div>


<!-- ═══════════════ TERMINAL ═══════════════ -->
<div class="section">
  <div class="section-header">
    <span class="section-icon">$</span>
    <span class="section-title">archit.json</span>
  </div>
  <div class="section-body" style="padding:0;">
    <div class="terminal">
      <div class="terminal-bar">
        <span class="t-red"></span>
        <span class="t-yellow"></span>
        <span class="t-green"></span>
      </div>
      <div class="terminal-body">
        <span class="t-comment">// archit_sengupta.config</span><br/>
        <span class="t-sep">{</span><br/>
        &nbsp;&nbsp;<span class="t-key">"focus"</span><span class="t-sep">:</span> <span class="t-str">"Backend Engineering + Data Systems"</span><span class="t-sep">,</span><br/>
        &nbsp;&nbsp;<span class="t-key">"strengths"</span><span class="t-sep">:</span> <span class="t-sep">[</span><span class="t-str">"database optimization"</span><span class="t-sep">,</span> <span class="t-str">"system design"</span><span class="t-sep">,</span> <span class="t-str">"algorithmic problem-solving"</span><span class="t-sep">],</span><br/>
        &nbsp;&nbsp;<span class="t-key">"interests"</span><span class="t-sep">:</span> <span class="t-sep">[</span><span class="t-str">"client-facing products"</span><span class="t-sep">,</span> <span class="t-str">"modern web frameworks"</span><span class="t-sep">,</span> <span class="t-str">"data optimization"</span><span class="t-sep">],</span><br/>
        &nbsp;&nbsp;<span class="t-key">"currently_building"</span><span class="t-sep">:</span> <span class="t-str">"Catastrophe modeling pipelines @ Zurich Insurance"</span><span class="t-sep">,</span><br/>
        &nbsp;&nbsp;<span class="t-key">"education"</span><span class="t-sep">:</span> <span class="t-sep">{</span><br/>
        &nbsp;&nbsp;&nbsp;&nbsp;<span class="t-key">"degree"</span><span class="t-sep">:</span> <span class="t-str">"MSCS"</span><span class="t-sep">,</span><br/>
        &nbsp;&nbsp;&nbsp;&nbsp;<span class="t-key">"school"</span><span class="t-sep">:</span> <span class="t-str">"Georgia Institute of Technology"</span><span class="t-sep">,</span><br/>
        &nbsp;&nbsp;&nbsp;&nbsp;<span class="t-key">"gpa"</span><span class="t-sep">:</span> <span class="t-val">4.0</span><br/>
        &nbsp;&nbsp;<span class="t-sep">},</span><br/>
        &nbsp;&nbsp;<span class="t-key">"fun"</span><span class="t-sep">:</span> <span class="t-sep">[</span><span class="t-str">"Docker media server"</span><span class="t-sep">,</span> <span class="t-str">"Linux gaming"</span><span class="t-sep">,</span> <span class="t-str">"sports"</span><span class="t-sep">]</span><br/>
        <span class="t-sep">}</span>
      </div>
    </div>
  </div>
</div>


<!-- ═══════════════ OUTSIDE CODE ═══════════════ -->
<div class="section">
  <div class="section-header">
    <span class="section-icon">⚡</span>
    <span class="section-title">Outside of Code</span>
  </div>
  <div class="section-body">
    <div class="interests">
      <span class="interest-chip">🐳 Self-hosted Docker media server</span>
      <span class="interest-chip">🐧 Stable Linux gaming setups</span>
      <span class="interest-chip">⚽ Sports</span>
      <span class="interest-chip">🔧 Tinkering with CI/CD pipelines</span>
    </div>
  </div>
</div>


<!-- ═══════════════ CONNECT ═══════════════ -->
<div class="section">
  <div class="section-header">
    <span class="section-icon">📡</span>
    <span class="section-title">Let's Connect</span>
  </div>
  <div class="section-body">
    <div class="connect-grid">
      <a class="connect-card" href="https://linkedin.com/in/architsengupta">
        <span class="connect-icon">💼</span>
        <div>
          <div class="connect-label">LinkedIn</div>
          <div class="connect-value">linkedin.com/in/architsengupta</div>
        </div>
      </a>
      <a class="connect-card" href="mailto:architsengupta@gmail.com">
        <span class="connect-icon">✉</span>
        <div>
          <div class="connect-label">Email</div>
          <div class="connect-value">architsengupta@gmail.com</div>
        </div>
      </a>
    </div>
  </div>
</div>

<div class="footer">
  ── built with precision · deployed with care ──
</div>

</body>
</html>
