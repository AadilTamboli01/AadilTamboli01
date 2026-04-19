<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Aadil Tamboli — GitHub Profile</title>
  <link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500;600&family=Space+Grotesk:wght@300;400;500;600;700&display=swap" rel="stylesheet"/>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }

    body {
      background: #010409;
      font-family: 'Space Grotesk', sans-serif;
      display: flex;
      justify-content: center;
      padding: 40px 16px;
      min-height: 100vh;
    }

    .readme-wrap {
      background: #0d1117;
      color: #c9d1d9;
      padding: 40px 36px;
      border-radius: 14px;
      max-width: 880px;
      width: 100%;
      font-size: 14px;
      line-height: 1.7;
      border: 1px solid #21262d;
    }

    /* HERO */
    .hero {
      text-align: center;
      padding: 40px 20px 36px;
      border-bottom: 1px solid #21262d;
      margin-bottom: 36px;
    }

    .avatar-ring {
      width: 108px;
      height: 108px;
      border-radius: 50%;
      background: linear-gradient(135deg, #00d4ff, #7928ca, #ff0080);
      padding: 3px;
      margin: 0 auto 18px;
      display: inline-block;
    }

    .avatar-inner {
      width: 100%;
      height: 100%;
      border-radius: 50%;
      background: #161b22;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 38px;
      font-family: 'Fira Code', monospace;
      color: #58a6ff;
      font-weight: 600;
    }

    .hero h1 {
      font-size: 30px;
      font-weight: 700;
      color: #f0f6fc;
      letter-spacing: -0.5px;
      margin-bottom: 8px;
    }

    .typing-line {
      font-family: 'Fira Code', monospace;
      font-size: 13px;
      color: #7ee787;
      margin-bottom: 12px;
    }

    .typing-line span { color: #ff7b72; }

    .hero-meta {
      font-size: 13px;
      color: #8b949e;
      margin-bottom: 18px;
    }

    .badge-row {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      justify-content: center;
    }

    .badge {
      padding: 5px 14px;
      border-radius: 20px;
      font-size: 11px;
      font-weight: 600;
      font-family: 'Fira Code', monospace;
      letter-spacing: 0.5px;
    }

    .badge-blue   { background: #0d2137; color: #58a6ff; border: 1px solid #1f4d7a; }
    .badge-green  { background: #0d2614; color: #7ee787; border: 1px solid #1a5c26; }
    .badge-purple { background: #1c1040; color: #d2a8ff; border: 1px solid #3d2080; }
    .badge-orange { background: #2d1f0a; color: #ffa657; border: 1px solid #6b4517; }

    /* SECTION */
    .section { margin-bottom: 36px; }

    .section-title {
      font-size: 12px;
      font-weight: 600;
      color: #8b949e;
      text-transform: uppercase;
      letter-spacing: 1.5px;
      font-family: 'Fira Code', monospace;
      display: flex;
      align-items: center;
      gap: 10px;
      margin-bottom: 18px;
    }

    .section-title::after {
      content: '';
      flex: 1;
      height: 1px;
      background: #21262d;
    }

    /* ABOUT */
    .about-box {
      background: #161b22;
      border: 1px solid #21262d;
      border-radius: 10px;
      padding: 22px 26px;
      border-left: 3px solid #58a6ff;
    }

    .about-box p { color: #c9d1d9; font-size: 14px; line-height: 1.9; margin-bottom: 16px; }

    .info-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 10px;
    }

    .info-item {
      display: flex;
      align-items: center;
      gap: 8px;
      font-family: 'Fira Code', monospace;
      font-size: 12px;
      color: #8b949e;
    }

    .info-item .dot { color: #58a6ff; }
    .info-item strong { color: #c9d1d9; }

    /* SKILLS */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
      gap: 14px;
    }

    .skill-card {
      background: #161b22;
      border: 1px solid #21262d;
      border-radius: 10px;
      padding: 18px;
      transition: border-color 0.2s;
    }

    .skill-card:hover { border-color: #30363d; }

    .skill-card-title {
      font-size: 11px;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 1px;
      margin-bottom: 12px;
      font-family: 'Fira Code', monospace;
    }

    .skill-tags { display: flex; flex-wrap: wrap; gap: 6px; }

    .tag {
      padding: 3px 10px;
      border-radius: 6px;
      font-size: 11px;
      font-family: 'Fira Code', monospace;
      font-weight: 500;
    }

    .tag-blue   { background: #0d2137; color: #79c0ff; border: 1px solid #1f4d7a; }
    .tag-green  { background: #0d2614; color: #56d364; border: 1px solid #1a5c26; }
    .tag-orange { background: #2d1f0a; color: #ffa657; border: 1px solid #6b4517; }
    .tag-purple { background: #1c1040; color: #d2a8ff; border: 1px solid #3d2080; }
    .tag-gray   { background: #1c2128; color: #8b949e; border: 1px solid #30363d; }
    .tag-red    { background: #2d0e0e; color: #ff7b72; border: 1px solid #6b1c1c; }
    .tag-teal   { background: #061d1d; color: #3fb950; border: 1px solid #0d4a3a; }

    /* PROJECTS */
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
      gap: 14px;
    }

    .project-card {
      background: #161b22;
      border: 1px solid #21262d;
      border-radius: 10px;
      padding: 20px 22px;
      position: relative;
      overflow: hidden;
      transition: border-color 0.2s, transform 0.2s;
    }

    .project-card:hover { border-color: #30363d; transform: translateY(-2px); }

    .project-card::before {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0;
      height: 2px;
    }

    .project-card.blue::before   { background: linear-gradient(90deg, #58a6ff, #1f6feb); }
    .project-card.green::before  { background: linear-gradient(90deg, #56d364, #2ea043); }
    .project-card.purple::before { background: linear-gradient(90deg, #d2a8ff, #8957e5); }

    .project-name {
      font-size: 15px;
      font-weight: 600;
      color: #f0f6fc;
      margin-bottom: 8px;
      font-family: 'Fira Code', monospace;
    }

    .project-desc {
      font-size: 12px;
      color: #8b949e;
      line-height: 1.7;
      margin-bottom: 14px;
    }

    .project-stack { display: flex; flex-wrap: wrap; gap: 5px; margin-bottom: 14px; }

    .project-links { display: flex; gap: 8px; }

    .link-btn {
      padding: 5px 14px;
      border-radius: 6px;
      font-size: 11px;
      font-family: 'Fira Code', monospace;
      font-weight: 500;
      cursor: pointer;
      text-decoration: none;
      display: inline-block;
    }

    .link-btn.primary   { background: #21262d; color: #c9d1d9; border: 1px solid #30363d; }
    .link-btn.secondary { background: #0d2137; color: #58a6ff; border: 1px solid #1f4d7a; }

    /* STATS */
    .stats-row {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 14px;
    }

    .stat-card {
      background: #161b22;
      border: 1px solid #21262d;
      border-radius: 10px;
      padding: 22px;
      text-align: center;
    }

    .stat-number {
      font-size: 28px;
      font-weight: 700;
      color: #58a6ff;
      font-family: 'Fira Code', monospace;
    }

    .stat-label {
      font-size: 11px;
      color: #8b949e;
      text-transform: uppercase;
      letter-spacing: 1px;
      margin-top: 6px;
      font-family: 'Fira Code', monospace;
    }

    /* SOCIAL */
    .social-row { display: flex; flex-wrap: wrap; gap: 10px; }

    .social-btn {
      display: flex;
      align-items: center;
      gap: 8px;
      padding: 10px 18px;
      border-radius: 8px;
      font-size: 12px;
      font-family: 'Fira Code', monospace;
      font-weight: 500;
      cursor: pointer;
      background: #161b22;
      text-decoration: none;
      transition: opacity 0.2s, transform 0.2s;
    }

    .social-btn:hover { opacity: 0.8; transform: translateY(-1px); }
    .social-btn.github   { color: #c9d1d9; border: 1px solid #30363d; }
    .social-btn.linkedin { color: #58a6ff; border: 1px solid #1f4d7a; }
    .social-btn.email    { color: #ffa657; border: 1px solid #6b4517; }
    .social-btn.phone    { color: #56d364; border: 1px solid #1a5c26; }

    /* FOOTER */
    .footer {
      text-align: center;
      padding-top: 28px;
      border-top: 1px solid #21262d;
      margin-top: 8px;
      font-family: 'Fira Code', monospace;
      font-size: 11px;
      color: #484f58;
    }
  </style>
</head>
<body>
  <div class="readme-wrap">

    <!-- HERO -->
    <div class="hero">
      <div class="avatar-ring">
        <div class="avatar-inner">AT</div>
      </div>
      <h1>Aadil Tamboli</h1>
      <div class="typing-line">
        <span>const</span> role = <span>"Full Stack Developer"</span> | <span>"MERN Stack"</span>
      </div>
      <div class="hero-meta">📍 Pune, India &nbsp;•&nbsp; B.Tech IT @ GH Raisoni College &nbsp;•&nbsp; CGPA 8.2/10</div>
      <div class="badge-row">
        <span class="badge badge-blue">Open to Work</span>
        <span class="badge badge-green">MERN Stack</span>
        <span class="badge badge-purple">Java &amp; Python</span>
        <span class="badge badge-orange">Final Year 2026</span>
      </div>
    </div>

    <!-- ABOUT -->
    <div class="section">
      <div class="section-title">// about me</div>
      <div class="about-box">
        <p>Final-year IT student passionate about building <strong style="color:#58a6ff;">scalable backend systems</strong>, clean REST APIs, and full-stack web applications. I love open-source technologies, problem-solving, and crafting reliable software — one commit at a time.</p>
        <div class="info-grid">
          <div class="info-item"><span class="dot">▸</span><span>Email: <strong>aadiltamboli07@gmail.com</strong></span></div>
          <div class="info-item"><span class="dot">▸</span><span>Phone: <strong>+91 7219014209</strong></span></div>
          <div class="info-item"><span class="dot">▸</span><span>Status: <strong>Final Year Student</strong></span></div>
          <div class="info-item"><span class="dot">▸</span><span>Focus: <strong>Backend &amp; Full Stack</strong></span></div>
        </div>
      </div>
    </div>

    <!-- SKILLS -->
    <div class="section">
      <div class="section-title">// tech stack</div>
      <div class="skills-grid">
        <div class="skill-card">
          <div class="skill-card-title" style="color:#58a6ff;">Languages</div>
          <div class="skill-tags">
            <span class="tag tag-blue">Java</span>
            <span class="tag tag-blue">Python</span>
            <span class="tag tag-orange">JavaScript</span>
            <span class="tag tag-gray">C</span>
            <span class="tag tag-orange">HTML/CSS</span>
          </div>
        </div>
        <div class="skill-card">
          <div class="skill-card-title" style="color:#56d364;">Frameworks</div>
          <div class="skill-tags">
            <span class="tag tag-blue">React.js</span>
            <span class="tag tag-green">Node.js</span>
            <span class="tag tag-green">Express.js</span>
            <span class="tag tag-purple">Redux Toolkit</span>
            <span class="tag tag-teal">Hibernate</span>
          </div>
        </div>
        <div class="skill-card">
          <div class="skill-card-title" style="color:#ffa657;">Databases</div>
          <div class="skill-tags">
            <span class="tag tag-blue">MongoDB</span>
            <span class="tag tag-orange">MySQL</span>
          </div>
        </div>
        <div class="skill-card">
          <div class="skill-card-title" style="color:#d2a8ff;">Tools &amp; Concepts</div>
          <div class="skill-tags">
            <span class="tag tag-orange">Git</span>
            <span class="tag tag-gray">GitHub</span>
            <span class="tag tag-red">Linux</span>
            <span class="tag tag-gray">VS Code</span>
            <span class="tag tag-green">Postman</span>
            <span class="tag tag-purple">REST APIs</span>
            <span class="tag tag-teal">Agile</span>
            <span class="tag tag-gray">OOP</span>
            <span class="tag tag-gray">DSA</span>
          </div>
        </div>
      </div>
    </div>

    <!-- PROJECTS -->
    <div class="section">
      <div class="section-title">// featured projects</div>
      <div class="projects-grid">

        <div class="project-card blue">
          <div class="project-name">DreamPixels</div>
          <div class="project-desc">Full-stack AI text-to-image web app with 10+ REST API endpoints, JWT authentication, MongoDB storage &amp; Cloudinary for image management.</div>
          <div class="project-stack">
            <span class="tag tag-blue">React.js</span>
            <span class="tag tag-green">Node.js</span>
            <span class="tag tag-green">Express.js</span>
            <span class="tag tag-blue">MongoDB</span>
            <span class="tag tag-orange">JWT</span>
          </div>
          <div class="project-links">
            <a class="link-btn secondary" href="#">Live Demo</a>
            <a class="link-btn primary" href="https://github.com/AadilTamboli01" target="_blank">GitHub</a>
          </div>
        </div>

        <div class="project-card green">
          <div class="project-name">Twitter API</div>
          <div class="project-desc">RESTful backend for a Twitter-like platform — posts, likes, comments, follows, notifications &amp; Cloudinary image uploads.</div>
          <div class="project-stack">
            <span class="tag tag-green">Node.js</span>
            <span class="tag tag-green">Express.js</span>
            <span class="tag tag-blue">MongoDB</span>
            <span class="tag tag-orange">JWT</span>
            <span class="tag tag-purple">REST API</span>
          </div>
          <div class="project-links">
            <a class="link-btn primary" href="https://github.com/AadilTamboli01" target="_blank">GitHub</a>
          </div>
        </div>

        <div class="project-card purple">
          <div class="project-name">MessageHub</div>
          <div class="project-desc">Real-time chat system using Socket.io with 8+ endpoints, MongoDB schemas, and a responsive React frontend.</div>
          <div class="project-stack">
            <span class="tag tag-blue">React.js</span>
            <span class="tag tag-purple">Socket.io</span>
            <span class="tag tag-green">Node.js</span>
            <span class="tag tag-blue">MongoDB</span>
          </div>
          <div class="project-links">
            <a class="link-btn primary" href="https://github.com/AadilTamboli01" target="_blank">GitHub</a>
          </div>
        </div>

      </div>
    </div>

    <!-- STATS -->
    <div class="section">
      <div class="section-title">// highlights</div>
      <div class="stats-row">
        <div class="stat-card">
          <div class="stat-number">8.2</div>
          <div class="stat-label">CGPA / 10</div>
        </div>
        <div class="stat-card">
          <div class="stat-number">3+</div>
          <div class="stat-label">Projects Built</div>
        </div>
        <div class="stat-card">
          <div class="stat-number">4th</div>
          <div class="stat-label">B.Tech Competition</div>
        </div>
      </div>
    </div>

    <!-- SOCIAL -->
    <div class="section">
      <div class="section-title">// connect with me</div>
      <div class="social-row">
        <a class="social-btn github" href="https://github.com/AadilTamboli01" target="_blank">⌥ GitHub — AadilTamboli01</a>
        <a class="social-btn linkedin" href="https://linkedin.com/in/aadiltamboli/" target="_blank">in LinkedIn — aadiltamboli</a>
        <a class="social-btn email" href="mailto:aadiltamboli07@gmail.com">@ Email — aadiltamboli07</a>
        <a class="social-btn phone" href="tel:+917219014209">☎ +91 7219014209</a>
      </div>
    </div>

    <!-- FOOTER -->
    <div class="footer">
      ✦ crafted with passion &amp; lots of console.log() ✦ &nbsp;|&nbsp; Aadil Tamboli © 2026
    </div>

  </div>
</body>
</html>
