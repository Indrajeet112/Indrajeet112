<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Indrajeet Chauhan — GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Syne:wght@400;600;700;800&display=swap" rel="stylesheet"/>
<style>
  :root {
    --bg: #0d1117;
    --card: #161b22;
    --border: #30363d;
    --accent: #58a6ff;
    --accent2: #3fb950;
    --accent3: #f78166;
    --accent4: #d2a8ff;
    --text: #e6edf3;
    --muted: #8b949e;
    --glow: rgba(88,166,255,0.15);
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Syne', sans-serif;
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* Grid background */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(88,166,255,0.04) 1px, transparent 1px),
      linear-gradient(90deg, rgba(88,166,255,0.04) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
    z-index: 0;
  }

  .container {
    max-width: 860px;
    margin: 0 auto;
    padding: 40px 20px 80px;
    position: relative;
    z-index: 1;
  }

  /* HEADER */
  .header {
    text-align: center;
    margin-bottom: 48px;
    animation: fadeUp 0.8s ease both;
  }

  .avatar-ring {
    width: 90px; height: 90px;
    border-radius: 50%;
    margin: 0 auto 20px;
    background: linear-gradient(135deg, var(--accent), var(--accent4), var(--accent2));
    padding: 3px;
    animation: spin-slow 8s linear infinite;
  }
  .avatar-inner {
    width: 100%; height: 100%;
    border-radius: 50%;
    background: var(--bg);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 2rem;
    animation: spin-slow 8s linear infinite reverse;
  }
  @keyframes spin-slow { from{transform:rotate(0)} to{transform:rotate(360deg)} }

  h1 {
    font-family: 'Syne', sans-serif;
    font-size: clamp(1.8rem, 5vw, 2.8rem);
    font-weight: 800;
    background: linear-gradient(135deg, var(--accent), var(--accent4));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    line-height: 1.1;
    margin-bottom: 8px;
  }

  .tagline {
    color: var(--muted);
    font-size: 0.95rem;
    font-family: 'Space Mono', monospace;
    letter-spacing: 0.5px;
    margin-bottom: 20px;
  }

  .tagline span {
    color: var(--accent2);
  }

  .badges {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 8px;
    margin-bottom: 24px;
  }

  .badge {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 6px 14px;
    border-radius: 20px;
    font-size: 0.78rem;
    font-family: 'Space Mono', monospace;
    border: 1px solid var(--border);
    background: var(--card);
    color: var(--text);
    text-decoration: none;
    transition: all 0.2s;
  }
  .badge:hover {
    border-color: var(--accent);
    box-shadow: 0 0 12px var(--glow);
    transform: translateY(-2px);
    color: var(--accent);
  }
  .badge .dot { width: 8px; height: 8px; border-radius: 50%; background: var(--accent2); }
  .badge.gmail .dot { background: #ea4335; }
  .badge.li .dot { background: #0a66c2; }
  .badge.loc .dot { background: var(--accent3); }

  /* SECTION */
  .section {
    margin-bottom: 40px;
    animation: fadeUp 0.8s ease both;
  }
  .section:nth-child(2) { animation-delay: 0.1s; }
  .section:nth-child(3) { animation-delay: 0.2s; }
  .section:nth-child(4) { animation-delay: 0.3s; }
  .section:nth-child(5) { animation-delay: 0.4s; }
  .section:nth-child(6) { animation-delay: 0.5s; }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  .section-title {
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 1rem;
    font-weight: 700;
    color: var(--accent);
    text-transform: uppercase;
    letter-spacing: 1.5px;
    margin-bottom: 16px;
    font-family: 'Space Mono', monospace;
  }
  .section-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, var(--border), transparent);
  }

  /* ABOUT CARD */
  .about-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px 24px;
    line-height: 1.7;
    color: #c9d1d9;
    font-size: 0.95rem;
    position: relative;
    overflow: hidden;
  }
  .about-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 4px; height: 100%;
    background: linear-gradient(180deg, var(--accent), var(--accent4));
    border-radius: 4px 0 0 4px;
  }
  .about-bullets {
    list-style: none;
    margin-top: 12px;
    display: flex;
    flex-direction: column;
    gap: 6px;
  }
  .about-bullets li::before {
    content: '▹ ';
    color: var(--accent2);
  }

  /* TECH STACK */
  .tech-categories {
    display: flex;
    flex-direction: column;
    gap: 16px;
  }

  .tech-row {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 14px 18px;
    display: flex;
    align-items: flex-start;
    gap: 16px;
    flex-wrap: wrap;
    transition: border-color 0.2s, box-shadow 0.2s;
  }
  .tech-row:hover {
    border-color: var(--accent);
    box-shadow: 0 0 20px var(--glow);
  }

  .tech-label {
    font-family: 'Space Mono', monospace;
    font-size: 0.72rem;
    color: var(--muted);
    text-transform: uppercase;
    letter-spacing: 1px;
    min-width: 110px;
    padding-top: 4px;
    flex-shrink: 0;
  }

  .tech-chips {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .chip {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    background: #1c2128;
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 5px 10px;
    font-size: 0.8rem;
    font-family: 'Space Mono', monospace;
    transition: all 0.2s;
    cursor: default;
  }
  .chip:hover {
    transform: translateY(-2px);
    border-color: var(--chip-color, var(--accent));
    box-shadow: 0 4px 12px rgba(0,0,0,0.3);
    color: var(--chip-color, var(--accent));
  }
  .chip img {
    width: 16px; height: 16px;
    object-fit: contain;
    filter: brightness(1);
  }

  /* PROJECTS */
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(380px, 1fr));
    gap: 16px;
  }

  .project-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px;
    transition: all 0.3s;
    position: relative;
    overflow: hidden;
  }
  .project-card::after {
    content: '';
    position: absolute;
    inset: 0;
    border-radius: 12px;
    background: linear-gradient(135deg, var(--proj-color, var(--accent)) 0%, transparent 60%);
    opacity: 0;
    transition: opacity 0.3s;
    pointer-events: none;
  }
  .project-card:hover {
    border-color: var(--proj-color, var(--accent));
    transform: translateY(-4px);
    box-shadow: 0 8px 24px rgba(0,0,0,0.4);
  }
  .project-card:hover::after { opacity: 0.04; }

  .project-header {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 10px;
  }
  .project-icon {
    font-size: 1.4rem;
    flex-shrink: 0;
  }
  .project-name {
    font-size: 1rem;
    font-weight: 700;
    color: var(--text);
  }
  .project-period {
    font-size: 0.7rem;
    color: var(--muted);
    font-family: 'Space Mono', monospace;
    margin-left: auto;
  }
  .project-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
    margin-bottom: 12px;
  }
  .tag {
    font-size: 0.68rem;
    font-family: 'Space Mono', monospace;
    padding: 2px 8px;
    border-radius: 4px;
    background: rgba(88,166,255,0.1);
    color: var(--accent);
    border: 1px solid rgba(88,166,255,0.2);
  }
  .project-desc {
    font-size: 0.85rem;
    color: #8b949e;
    line-height: 1.6;
  }
  .project-metric {
    display: inline-block;
    margin-top: 10px;
    font-size: 0.78rem;
    font-family: 'Space Mono', monospace;
    color: var(--accent2);
    background: rgba(63,185,80,0.1);
    padding: 3px 10px;
    border-radius: 4px;
    border: 1px solid rgba(63,185,80,0.2);
  }

  /* EXPERIENCE */
  .exp-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px 24px;
    position: relative;
    overflow: hidden;
  }
  .exp-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 100%; height: 3px;
    background: linear-gradient(90deg, var(--accent2), var(--accent));
  }
  .exp-header {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 8px;
    margin-bottom: 12px;
  }
  .exp-role { font-size: 1.05rem; font-weight: 700; }
  .exp-company { color: var(--accent2); font-size: 0.85rem; margin-top: 2px; }
  .exp-date {
    font-family: 'Space Mono', monospace;
    font-size: 0.72rem;
    color: var(--muted);
    background: #1c2128;
    padding: 4px 10px;
    border-radius: 6px;
    border: 1px solid var(--border);
    white-space: nowrap;
  }
  .exp-bullets {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 6px;
  }
  .exp-bullets li {
    font-size: 0.85rem;
    color: #8b949e;
    line-height: 1.6;
  }
  .exp-bullets li::before { content: '▹ '; color: var(--accent2); }
  .exp-bullets strong { color: var(--text); }

  /* EDUCATION */
  .edu-list {
    display: flex;
    flex-direction: column;
    gap: 12px;
  }
  .edu-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 14px 18px;
    display: flex;
    align-items: center;
    gap: 14px;
    flex-wrap: wrap;
    transition: border-color 0.2s;
  }
  .edu-card:hover { border-color: var(--accent4); }
  .edu-icon { font-size: 1.5rem; flex-shrink: 0; }
  .edu-info { flex: 1; min-width: 200px; }
  .edu-degree { font-size: 0.95rem; font-weight: 700; }
  .edu-inst { font-size: 0.8rem; color: var(--muted); margin-top: 2px; }
  .edu-score {
    font-family: 'Space Mono', monospace;
    font-size: 0.8rem;
    color: var(--accent4);
    background: rgba(210,168,255,0.1);
    padding: 4px 10px;
    border-radius: 6px;
    border: 1px solid rgba(210,168,255,0.2);
    white-space: nowrap;
  }

  /* CERTS */
  .cert-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
    gap: 10px;
  }
  .cert-item {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 12px 14px;
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 0.82rem;
    transition: all 0.2s;
  }
  .cert-item:hover {
    border-color: var(--accent);
    background: #1c2128;
  }
  .cert-icon { font-size: 1.1rem; }
  .cert-status {
    margin-left: auto;
    font-size: 0.65rem;
    font-family: 'Space Mono', monospace;
    color: var(--accent2);
    background: rgba(63,185,80,0.1);
    padding: 2px 6px;
    border-radius: 4px;
    border: 1px solid rgba(63,185,80,0.2);
    white-space: nowrap;
  }
  .cert-status.wip { color: var(--accent3); background: rgba(247,129,102,0.1); border-color: rgba(247,129,102,0.2); }

  /* SKILLS PILLS */
  .skills-wrap {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }
  .skill-pill {
    padding: 6px 14px;
    border-radius: 20px;
    font-size: 0.8rem;
    border: 1px solid var(--border);
    background: var(--card);
    color: var(--muted);
    transition: all 0.2s;
    font-family: 'Space Mono', monospace;
  }
  .skill-pill:hover {
    border-color: var(--accent4);
    color: var(--accent4);
    transform: translateY(-2px);
  }

  /* FOOTER QUOTE */
  .footer-quote {
    margin-top: 60px;
    text-align: center;
    font-style: italic;
    color: var(--muted);
    font-size: 0.85rem;
    font-family: 'Space Mono', monospace;
    border-top: 1px solid var(--border);
    padding-top: 24px;
  }
  .footer-quote span { color: var(--accent); }

  /* STATS ROW */
  .stats-row {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    margin-bottom: 40px;
    justify-content: center;
  }
  .stat-box {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 14px 20px;
    text-align: center;
    min-width: 120px;
    flex: 1;
    transition: all 0.2s;
  }
  .stat-box:hover {
    border-color: var(--accent);
    box-shadow: 0 0 16px var(--glow);
  }
  .stat-num {
    font-size: 1.5rem;
    font-weight: 800;
    background: linear-gradient(135deg, var(--accent), var(--accent4));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    display: block;
  }
  .stat-label {
    font-size: 0.7rem;
    color: var(--muted);
    font-family: 'Space Mono', monospace;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    margin-top: 4px;
  }

  /* RESPONSIVE */
  @media (max-width: 600px) {
    .projects-grid { grid-template-columns: 1fr; }
    .tech-label { min-width: 80px; font-size: 0.65rem; }
    .chip { font-size: 0.72rem; padding: 4px 8px; }
    .cert-grid { grid-template-columns: 1fr; }
    .stat-box { min-width: 90px; }
  }
</style>
</head>
<body>
<div class="container">

  <!-- HEADER -->
  <div class="header">
    <div class="avatar-ring">
      <div class="avatar-inner">🧑‍💻</div>
    </div>
    <h1>Indrajeet Chauhan</h1>
    <p class="tagline">Data Analyst · <span>Python</span> · SQL · Power BI · Machine Learning</p>
    <div class="badges">
      <a class="badge gmail" href="mailto:indrajeetchauhaann@gmail.com">
        <span class="dot"></span> indrajeetchauhaann@gmail.com
      </a>
      <a class="badge li" href="https://linkedin.com/in/indrajeetchauhan" target="_blank">
        <span class="dot"></span> linkedin.com/in/indrajeetchauhan
      </a>
      <span class="badge loc">
        <span class="dot"></span> Bhopal, MP · India
      </span>
    </div>
  </div>

  <!-- STATS -->
  <div class="stats-row section">
    <div class="stat-box">
      <span class="stat-num">4+</span>
      <div class="stat-label">Projects</div>
    </div>
    <div class="stat-box">
      <span class="stat-num">100K+</span>
      <div class="stat-label">Records Analyzed</div>
    </div>
    <div class="stat-box">
      <span class="stat-num">35%</span>
      <div class="stat-label">Latency Reduced</div>
    </div>
    <div class="stat-box">
      <span class="stat-num">60%</span>
      <div class="stat-label">Report Time Saved</div>
    </div>
    <div class="stat-box">
      <span class="stat-num">7.38</span>
      <div class="stat-label">CGPA / 10</div>
    </div>
  </div>

  <!-- ABOUT -->
  <div class="section">
    <div class="section-title">🙋 About Me</div>
    <div class="about-card">
      Final-year BCA student at <strong>LNCT University, Bhopal</strong> with hands-on experience in data analysis, SQL, Python, and Power BI dashboards. I love turning messy data into clean, actionable stories that move the needle.
      <ul class="about-bullets">
        <li>🎯 Actively seeking a <strong>Data Analyst (Fresher)</strong> role</li>
        <li>📊 Comfortable across the full analytics pipeline — raw data → business recommendation</li>
        <li>🤖 Exploring <strong>Computer Vision</strong> and <strong>NLP</strong> through real projects</li>
        <li>🌐 Languages: Hindi (Native) · English (Professional)</li>
      </ul>
    </div>
  </div>

  <!-- TECH STACK -->
  <div class="section">
    <div class="section-title">🛠️ Tech Stack</div>
    <div class="tech-categories">

      <div class="tech-row">
        <span class="tech-label">Languages</span>
        <div class="tech-chips">
          <span class="chip" style="--chip-color:#3776ab"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg"/> Python</span>
          <span class="chip" style="--chip-color:#f7df1e"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg"/> JavaScript</span>
          <span class="chip" style="--chip-color:#a8b9cc"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg"/> C</span>
        </div>
      </div>

      <div class="tech-row">
        <span class="tech-label">Data & Analytics</span>
        <div class="tech-chips">
          <span class="chip" style="--chip-color:#336791"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg"/> PostgreSQL</span>
          <span class="chip" style="--chip-color:#00758f"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg"/> MySQL</span>
          <span class="chip" style="--chip-color:#e3773c"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pandas/pandas-original.svg"/> Pandas</span>
          <span class="chip" style="--chip-color:#4c77cb"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/numpy/numpy-original.svg"/> NumPy</span>
        </div>
      </div>

      <div class="tech-row">
        <span class="tech-label">Visualization</span>
        <div class="tech-chips">
          <span class="chip" style="--chip-color:#f2c811">📊 Power BI</span>
          <span class="chip" style="--chip-color:#11557c">📉 Matplotlib</span>
          <span class="chip" style="--chip-color:#4c72b0">📈 Seaborn</span>
          <span class="chip" style="--chip-color:#217346"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/microsoftsqlserver/microsoftsqlserver-plain.svg"/> Excel</span>
        </div>
      </div>

      <div class="tech-row">
        <span class="tech-label">ML / AI</span>
        <div class="tech-chips">
          <span class="chip" style="--chip-color:#f7931e">🤖 Scikit-learn</span>
          <span class="chip" style="--chip-color:#5c3ee8">👁️ OpenCV</span>
          <span class="chip" style="--chip-color:#4285f4">💬 NLP</span>
        </div>
      </div>

      <div class="tech-row">
        <span class="tech-label">Web / Backend</span>
        <div class="tech-chips">
          <span class="chip" style="--chip-color:#000000"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/flask/flask-original.svg"/> Flask</span>
          <span class="chip" style="--chip-color:#e34f26"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg"/> HTML</span>
          <span class="chip" style="--chip-color:#1572b6"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg"/> CSS</span>
          <span class="chip" style="--chip-color:#58a6ff">🔌 REST APIs</span>
        </div>
      </div>

      <div class="tech-row">
        <span class="tech-label">Tools</span>
        <div class="tech-chips">
          <span class="chip" style="--chip-color:#f05032"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg"/> Git</span>
          <span class="chip" style="--chip-color:#ffffff"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg"/> GitHub</span>
          <span class="chip" style="--chip-color:#f9a825"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jupyter/jupyter-original.svg"/> Jupyter</span>
          <span class="chip" style="--chip-color:#007acc"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg"/> VS Code</span>
        </div>
      </div>

    </div>
  </div>

  <!-- PROJECTS -->
  <div class="section">
    <div class="section-title">🚀 Featured Projects</div>
    <div class="projects-grid">

      <div class="project-card" style="--proj-color:#f2c811">
        <div class="project-header">
          <span class="project-icon">📦</span>
          <span class="project-name">Market Basket Analysis</span>
          <span class="project-period">Nov–Dec 2025</span>
        </div>
        <div class="project-tags">
          <span class="tag">Power BI</span>
          <span class="tag">Python</span>
          <span class="tag">mlxtend</span>
          <span class="tag">Excel</span>
        </div>
        <p class="project-desc">Applied Apriori algorithm to mine association rules from 50,000+ retail transactions. Built interactive drill-through dashboards for cross-selling insights.</p>
        <span class="project-metric">78% lift score · ~60% reporting time saved</span>
      </div>

      <div class="project-card" style="--proj-color:#58a6ff">
        <div class="project-header">
          <span class="project-icon">🏏</span>
          <span class="project-name">IPL Performance Analytics</span>
          <span class="project-period">Ongoing</span>
        </div>
        <div class="project-tags">
          <span class="tag">Power BI</span>
          <span class="tag">SQL</span>
          <span class="tag">Excel</span>
          <span class="tag">Star Schema</span>
        </div>
        <p class="project-desc">End-to-end BI solution with star schema design, dynamic filters, drill-downs, and KPI cards (strike rate, economy, win %). Referenced by 3 peers.</p>
        <span class="project-metric">Player-level + Team-level analysis</span>
      </div>

      <div class="project-card" style="--proj-color:#3fb950">
        <div class="project-header">
          <span class="project-icon">🚖</span>
          <span class="project-name">Ola Ride Booking Analysis</span>
          <span class="project-period">2025</span>
        </div>
        <div class="project-tags">
          <span class="tag">Power BI</span>
          <span class="tag">Python</span>
          <span class="tag">Excel</span>
        </div>
        <p class="project-desc">Analyzed 100K+ ride records to identify peak demand windows, cancellation patterns, and high-value segments for operational improvements.</p>
        <span class="project-metric">3 operational recommendations delivered</span>
      </div>

      <div class="project-card" style="--proj-color:#d2a8ff">
        <div class="project-header">
          <span class="project-icon">🤖</span>
          <span class="project-name">VIDSANP — AI Web App</span>
          <span class="project-period">2025</span>
        </div>
        <div class="project-tags">
          <span class="tag">Flask</span>
          <span class="tag">OpenCV</span>
          <span class="tag">NLP</span>
          <span class="tag">Python</span>
        </div>
        <p class="project-desc">Full-stack AI platform integrating Computer Vision and NLP pipelines via Flask REST APIs. Batch normalization cut inference latency significantly.</p>
        <span class="project-metric">35% latency reduction</span>
      </div>

    </div>
  </div>

  <!-- EXPERIENCE -->
  <div class="section">
    <div class="section-title">💼 Experience</div>
    <div class="exp-card">
      <div class="exp-header">
        <div>
          <div class="exp-role">Python & Data Analytics Intern</div>
          <div class="exp-company">Jyesta Corporate Entity · Remote</div>
        </div>
        <span class="exp-date">Oct 2025 – Nov 2025</span>
      </div>
      <ul class="exp-bullets">
        <li>Processed and cleaned <strong>5+ datasets</strong> using Python (Pandas) and SQL; resolved <strong>1,200+ inconsistent records</strong></li>
        <li>Generated weekly reports with Matplotlib/Excel visualizations supporting <strong>4 active business use cases</strong></li>
        <li>Documented end-to-end data workflows and maintained version-controlled code on <strong>GitHub</strong></li>
        <li>Collaborated with senior analysts to translate business requirements into SQL queries and dashboard specs</li>
      </ul>
    </div>
  </div>

  <!-- EDUCATION -->
  <div class="section">
    <div class="section-title">🎓 Education</div>
    <div class="edu-list">
      <div class="edu-card">
        <span class="edu-icon">🏛️</span>
        <div class="edu-info">
          <div class="edu-degree">Bachelor of Computer Applications (BCA) · Final Year</div>
          <div class="edu-inst">LNCT University, Bhopal · 2023 – Present</div>
        </div>
        <span class="edu-score">CGPA 7.38 / 10</span>
      </div>
      <div class="edu-card">
        <span class="edu-icon">📚</span>
        <div class="edu-info">
          <div class="edu-degree">Class XII</div>
          <div class="edu-inst">Ramrati Adarsh Intercollege, Rasra UP · 2021</div>
        </div>
        <span class="edu-score">77%</span>
      </div>
      <div class="edu-card">
        <span class="edu-icon">📖</span>
        <div class="edu-info">
          <div class="edu-degree">Class X</div>
          <div class="edu-inst">St. Francis Intercollege, Rasra · 2019</div>
        </div>
        <span class="edu-score">68.4%</span>
      </div>
    </div>
  </div>

  <!-- CERTS -->
  <div class="section">
    <div class="section-title">📜 Certifications</div>
    <div class="cert-grid">
      <div class="cert-item"><span class="cert-icon">🐍</span> Python for Data Science<span class="cert-status wip">In Progress</span></div>
      <div class="cert-item"><span class="cert-icon">📊</span> Microsoft Power BI PL-300<span class="cert-status wip">Pursuing</span></div>
      <div class="cert-item"><span class="cert-icon">💾</span> SQL — HackerRank / LeetCode<span class="cert-status">Active</span></div>
      <div class="cert-item"><span class="cert-icon">📈</span> Google Data Analytics<span class="cert-status wip">In Progress</span></div>
    </div>
  </div>

  <!-- SOFT SKILLS -->
  <div class="section">
    <div class="section-title">🤝 Soft Skills</div>
    <div class="skills-wrap">
      <span class="skill-pill">Analytical Thinking</span>
      <span class="skill-pill">Problem Solving</span>
      <span class="skill-pill">Data Storytelling</span>
      <span class="skill-pill">Documentation</span>
      <span class="skill-pill">Cross-functional Collaboration</span>
      <span class="skill-pill">Self-directed Learning</span>
      <span class="skill-pill">Attention to Detail</span>
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer-quote">
    <span>"Without data, you're just another person with an opinion."</span><br/>
    — W. Edwards Deming<br/><br/>
    📬 Reach me at <a href="mailto:indrajeetchauhaann@gmail.com" style="color:var(--accent);text-decoration:none;">indrajeetchauhaann@gmail.com</a>
  </div>

</div>
</body>
</html>
