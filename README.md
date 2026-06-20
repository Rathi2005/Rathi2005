<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Harshit Rathi · Full Stack Dev</title>
  <!-- Font Awesome 6 (free) -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" />
  <!-- Google Font: Inter + Fira Code -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,500;14..32,600;14..32,700&family=Fira+Code:wght@400;500&display=swap" rel="stylesheet" />
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #0b0f1a;
      font-family: 'Inter', sans-serif;
      color: #e8edf5;
      line-height: 1.6;
      padding: 2rem 1.5rem;
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .container {
      max-width: 1100px;
      width: 100%;
      margin: 0 auto;
      background: rgba(18, 25, 40, 0.7);
      backdrop-filter: blur(4px);
      -webkit-backdrop-filter: blur(4px);
      border-radius: 3rem 3rem 2rem 2rem;
      padding: 2.5rem 2rem;
      box-shadow: 0 25px 50px -10px rgba(0, 0, 0, 0.8), 0 0 0 1px rgba(44, 151, 247, 0.15);
      border: 1px solid rgba(44, 151, 247, 0.1);
      transition: all 0.2s ease;
    }

    /* ---------- header / title ---------- */
    .profile-header {
      text-align: center;
      margin-bottom: 2.5rem;
    }

    .profile-header h1 {
      font-size: 3rem;
      font-weight: 700;
      letter-spacing: -0.5px;
      background: linear-gradient(135deg, #e0eaff 0%, #7bb3ff 80%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      display: inline-block;
      padding-bottom: 0.1rem;
    }

    .profile-header .subhead {
      font-size: 1.2rem;
      font-weight: 400;
      color: #9bb5d9;
      margin-top: 0.25rem;
      letter-spacing: 0.3px;
      border-bottom: 1px dashed rgba(44, 151, 247, 0.3);
      padding-bottom: 0.75rem;
      display: inline-block;
    }

    .typing-wrapper {
      margin-top: 1rem;
      font-family: 'Fira Code', monospace;
      font-size: 1.25rem;
      background: rgba(0, 20, 50, 0.4);
      padding: 0.6rem 1.2rem;
      border-radius: 60px;
      display: inline-block;
      backdrop-filter: blur(4px);
      border: 1px solid rgba(44, 151, 247, 0.2);
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
    }

    .typing-wrapper i {
      color: #2c97f7;
      margin-right: 8px;
    }

    /* ---------- about card ---------- */
    .about-card {
      background: rgba(12, 20, 35, 0.7);
      backdrop-filter: blur(2px);
      border-radius: 2rem;
      padding: 1.8rem 2rem;
      margin-bottom: 2.5rem;
      border: 1px solid rgba(44, 151, 247, 0.08);
      box-shadow: 0 8px 20px -8px rgba(0, 0, 0, 0.5);
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 1rem 2rem;
    }

    .about-card .emoji-big {
      font-size: 2.8rem;
      line-height: 1;
    }

    .about-text {
      flex: 1;
      min-width: 200px;
    }

    .about-text p {
      font-size: 1.05rem;
      color: #ccddf5;
      margin-bottom: 0.35rem;
    }

    .about-text .highlight {
      color: #7bb3ff;
      font-weight: 500;
    }

    .about-text .tag {
      display: inline-block;
      background: #1a2b44;
      padding: 0.2rem 1rem;
      border-radius: 40px;
      font-size: 0.8rem;
      font-weight: 500;
      color: #b3d0ff;
      border: 1px solid #2c4a7a;
      margin-right: 0.5rem;
      margin-top: 0.4rem;
    }

    .contact-links {
      display: flex;
      gap: 0.75rem;
      flex-wrap: wrap;
      margin-top: 0.5rem;
    }

    .contact-links a {
      color: #c3d9ff;
      background: #18273f;
      padding: 0.4rem 1rem;
      border-radius: 40px;
      font-size: 0.85rem;
      font-weight: 500;
      text-decoration: none;
      transition: all 0.2s;
      border: 1px solid transparent;
      display: inline-flex;
      align-items: center;
      gap: 8px;
    }

    .contact-links a:hover {
      background: #2c97f7;
      color: #0b0f1a;
      border-color: #2c97f7;
      transform: scale(1.02);
      box-shadow: 0 4px 12px rgba(44, 151, 247, 0.3);
    }

    /* ---------- skills ---------- */
    .skills-section {
      margin-bottom: 2.5rem;
    }

    .skills-section h2 {
      font-size: 1.5rem;
      font-weight: 600;
      letter-spacing: -0.2px;
      margin-bottom: 1rem;
      display: flex;
      align-items: center;
      gap: 10px;
      color: #b8d0f0;
    }

    .skills-section h2 i {
      color: #2c97f7;
      font-size: 1.6rem;
    }

    .skills-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 0.8rem 1.2rem;
      background: rgba(8, 16, 30, 0.5);
      padding: 1.2rem 1.5rem;
      border-radius: 2rem;
      backdrop-filter: blur(2px);
      border: 1px solid rgba(44, 151, 247, 0.06);
    }

    .skill-badge {
      background: #1b2942;
      padding: 0.4rem 1.2rem;
      border-radius: 50px;
      font-family: 'Fira Code', monospace;
      font-size: 0.9rem;
      font-weight: 500;
      color: #c7dcff;
      border: 1px solid #2e4570;
      transition: all 0.15s;
      display: inline-flex;
      align-items: center;
      gap: 8px;
    }

    .skill-badge i {
      color: #5f9eff;
      font-size: 1rem;
    }

    .skill-badge:hover {
      background: #2c97f7;
      color: #0b0f1a;
      border-color: #2c97f7;
      transform: translateY(-2px);
      box-shadow: 0 6px 14px rgba(44, 151, 247, 0.25);
    }

    /* ---------- featured project ---------- */
    .featured-section {
      margin-bottom: 2.5rem;
    }

    .featured-section h2 {
      font-size: 1.5rem;
      font-weight: 600;
      letter-spacing: -0.2px;
      margin-bottom: 1rem;
      color: #b8d0f0;
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .featured-section h2 i {
      color: #f7b731;
    }

    .project-card {
      background: rgba(12, 22, 40, 0.7);
      backdrop-filter: blur(2px);
      border-radius: 2rem;
      padding: 1.5rem 2rem;
      border: 1px solid rgba(44, 151, 247, 0.08);
      box-shadow: 0 8px 24px -8px rgba(0, 0, 0, 0.6);
      transition: all 0.25s;
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 1.5rem 2rem;
    }

    .project-card:hover {
      border-color: #2c97f7;
      box-shadow: 0 12px 28px -10px rgba(44, 151, 247, 0.2);
      transform: scale(1.003);
    }

    .project-info {
      flex: 2;
      min-width: 200px;
    }

    .project-info h3 {
      font-size: 1.7rem;
      font-weight: 700;
      letter-spacing: -0.3px;
      color: #d6e5ff;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .project-info h3 i {
      color: #5f9eff;
      font-size: 1.8rem;
    }

    .project-info .project-desc {
      margin: 0.5rem 0 0.8rem 0;
      color: #b3cae9;
      font-weight: 400;
    }

    .project-info ul {
      list-style: none;
      padding: 0;
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem 1.2rem;
      margin-bottom: 0.8rem;
    }

    .project-info ul li {
      font-size: 0.9rem;
      color: #b0c9ee;
      display: flex;
      align-items: center;
      gap: 6px;
    }

    .project-info ul li i {
      color: #2c97f7;
      font-size: 0.8rem;
    }

    .project-link {
      background: #1a2b44;
      padding: 0.5rem 1.2rem;
      border-radius: 60px;
      color: #c3d9ff;
      text-decoration: none;
      font-weight: 500;
      border: 1px solid #2e4a7a;
      transition: all 0.2s;
      display: inline-flex;
      align-items: center;
      gap: 8px;
    }

    .project-link:hover {
      background: #2c97f7;
      color: #0b0f1a;
      border-color: #2c97f7;
      box-shadow: 0 4px 12px rgba(44, 151, 247, 0.3);
    }

    .project-stack {
      font-family: 'Fira Code', monospace;
      font-size: 0.8rem;
      background: #0f1c31;
      padding: 0.2rem 1rem;
      border-radius: 40px;
      border: 1px solid #2e4570;
      color: #9bb9ee;
    }

    /* ---------- stats ---------- */
    .stats-section {
      display: flex;
      flex-wrap: wrap;
      gap: 1.5rem;
      justify-content: center;
      margin-bottom: 2rem;
    }

    .stat-card {
      background: rgba(10, 20, 38, 0.7);
      backdrop-filter: blur(2px);
      border-radius: 1.8rem;
      padding: 0.8rem 1.2rem;
      border: 1px solid rgba(44, 151, 247, 0.06);
      flex: 1 1 200px;
      min-width: 150px;
      text-align: center;
      box-shadow: 0 6px 16px rgba(0, 0, 0, 0.3);
      transition: all 0.2s;
    }

    .stat-card:hover {
      border-color: #2c97f7;
      transform: translateY(-4px);
    }

    .stat-card .stat-number {
      font-size: 2rem;
      font-weight: 700;
      color: #d6e5ff;
      letter-spacing: -0.5px;
    }

    .stat-card .stat-label {
      font-size: 0.8rem;
      text-transform: uppercase;
      letter-spacing: 1px;
      color: #8db0e0;
    }

    .stat-card i {
      color: #2c97f7;
      margin-right: 6px;
    }

    /* ---------- footer / view count ---------- */
    .footer-meta {
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      margin-top: 1.5rem;
      padding-top: 1rem;
      border-top: 1px solid rgba(44, 151, 247, 0.08);
      font-size: 0.9rem;
      color: #6f8bb0;
    }

    .footer-meta span i {
      margin-right: 6px;
      color: #2c97f7;
    }

    .footer-meta .view-badge {
      background: #121f36;
      padding: 0.3rem 1.2rem;
      border-radius: 60px;
      border: 1px solid #2e4570;
    }

    /* responsive */
    @media (max-width: 600px) {
      .container {
        padding: 1.5rem 1rem;
      }
      .profile-header h1 {
        font-size: 2.2rem;
      }
      .typing-wrapper {
        font-size: 1rem;
        padding: 0.4rem 1rem;
      }
      .about-card {
        flex-direction: column;
        align-items: flex-start;
      }
      .project-card {
        flex-direction: column;
        align-items: flex-start;
      }
    }

    /* small glow */
    .glow-text {
      text-shadow: 0 0 12px rgba(44, 151, 247, 0.15);
    }
  </style>
</head>
<body>
<div class="container">

  <!-- HEADER -->
  <div class="profile-header">
    <h1>👋 Harshit Rathi</h1>
    <div class="subhead">Full Stack Developer · India</div>
    <div class="typing-wrapper">
      <i class="fas fa-code"></i>
      <span id="typing-text">React · Node.js · MySQL</span>
    </div>
  </div>

  <!-- ABOUT + CONTACT -->
  <div class="about-card">
    <div class="emoji-big">🚀</div>
    <div class="about-text">
      <p><span class="highlight">Building real-world products</span> — currently working on <strong>ServerLink</strong>, a Cloud Management Platform.</p>
      <p style="font-size:0.95rem; color:#a6c1e8;">
        <i class="fas fa-brain" style="color:#2c97f7;"></i> DSA · System Design · SpringBoot
      </p>
      <div style="display: flex; flex-wrap: wrap; gap: 0.4rem 0.8rem; margin-top: 0.3rem;">
        <span class="tag"><i class="fas fa-code"></i> Full Stack</span>
        <span class="tag"><i class="fas fa-cloud"></i> Cloud</span>
        <span class="tag"><i class="fas fa-database"></i> MySQL</span>
      </div>
      <div class="contact-links">
        <a href="https://www.linkedin.com/in/harshit-rathi-70a079299" target="_blank"><i class="fab fa-linkedin"></i> LinkedIn</a>
        <a href="https://leetcode.com/u/Harshit_Rathi/" target="_blank"><i class="fas fa-code"></i> LeetCode</a>
        <a href="mailto:h0rshitr0thi2005@gmail.com"><i class="fas fa-envelope"></i> Gmail</a>
      </div>
    </div>
  </div>

  <!-- SKILLS -->
  <div class="skills-section">
    <h2><i class="fas fa-cogs"></i> Languages & Tools</h2>
    <div class="skills-grid">
      <span class="skill-badge"><i class="fab fa-python"></i> Python</span>
      <span class="skill-badge"><i class="fab fa-java"></i> Java</span>
      <span class="skill-badge"><i class="fab fa-js-square"></i> JavaScript</span>
      <span class="skill-badge"><i class="fab fa-react"></i> React</span>
      <span class="skill-badge"><i class="fab fa-node-js"></i> Node.js</span>
      <span class="skill-badge"><i class="fas fa-server"></i> Express</span>
      <span class="skill-badge"><i class="fas fa-flask"></i> Flask</span>
      <span class="skill-badge"><i class="fas fa-database"></i> MySQL</span>
      <span class="skill-badge"><i class="fas fa-leaf"></i> MongoDB</span>
      <span class="skill-badge"><i class="fab fa-html5"></i> HTML</span>
      <span class="skill-badge"><i class="fab fa-css3-alt"></i> CSS</span>
      <span class="skill-badge"><i class="fab fa-git-alt"></i> Git</span>
      <span class="skill-badge"><i class="fas fa-code"></i> Postman</span>
    </div>
  </div>

  <!-- FEATURED PROJECT -->
  <div class="featured-section">
    <h2><i class="fas fa-star"></i> Featured Project</h2>
    <div class="project-card">
      <div class="project-info">
        <h3><i class="fas fa-globe"></i> ServerLink</h3>
        <div class="project-desc"><strong>Cloud Server Management Platform</strong> · VM provisioning, integrated billing & dashboard</div>
        <ul>
          <li><i class="fas fa-check-circle"></i> VM Provisioning & Management</li>
          <li><i class="fas fa-check-circle"></i> Integrated Billing & Dashboard</li>
          <li><i class="fas fa-check-circle"></i> React + SpringBoot + MySQL</li>
        </ul>
        <div style="display: flex; flex-wrap: wrap; gap: 0.8rem; align-items: center;">
          <a href="https://github.com/Harshitrathi2005/ServerLink" target="_blank" class="project-link">
            <i class="fab fa-github"></i> View on GitHub
          </a>
          <span class="project-stack"><i class="fas fa-layer-group"></i> React · SpringBoot · MySQL</span>
        </div>
      </div>
    </div>
  </div>

  <!-- STATS -->
  <div class="stats-section">
    <div class="stat-card">
      <div class="stat-number"><i class="fas fa-code"></i> 12+</div>
      <div class="stat-label">Projects</div>
    </div>
    <div class="stat-card">
      <div class="stat-number"><i class="fas fa-star"></i> 4.2k</div>
      <div class="stat-label">LeetCode Rank</div>
    </div>
    <div class="stat-card">
      <div class="stat-number"><i class="fas fa-users"></i> 300+</div>
      <div class="stat-label">Connections</div>
    </div>
  </div>

  <!-- GITHUB STATS (visual) -->
  <div style="display: flex; flex-wrap: wrap; gap: 1.2rem; justify-content: center; margin: 1rem 0 0.5rem 0;">
    <img src="https://github-readme-stats.vercel.app/api?username=Rathi2005&show_icons=true&theme=tokyonight&hide_border=true&locale=en&bg_color=0a1428&title_color=7bb3ff&text_color=bbd4ff" alt="GitHub Stats" style="border-radius: 20px; max-width: 100%; height: auto; flex:1 1 280px;" />
    <img src="https://github-readme-stats.vercel.app/api/top-langs?username=Rathi2005&show_icons=true&theme=tokyonight&hide_border=true&locale=en&layout=compact&bg_color=0a1428&title_color=7bb3ff&text_color=bbd4ff" alt="Top Languages" style="border-radius: 20px; max-width: 100%; height: auto; flex:1 1 240px;" />
  </div>
  <div style="display: flex; justify-content: center; margin-top: 0.5rem;">
    <img src="https://github-readme-streak-stats.herokuapp.com/?user=Rathi2005&theme=tokyonight&hide_border=true&background=0a1428&ring=2c97f7&fire=2c97f7&currStreakLabel=7bb3ff" alt="GitHub Streak" style="border-radius: 20px; max-width: 100%; height: auto; width: 100%; max-width: 480px;" />
  </div>

  <!-- FOOTER -->
  <div class="footer-meta">
    <span><i class="fas fa-map-pin"></i> India · Full Stack Developer</span>
    <span class="view-badge"><i class="fas fa-eye"></i> Profile views · 1.2k</span>
  </div>

  <p style="text-align: center; margin-top: 1rem; font-size: 0.75rem; color: #385278; letter-spacing: 1px;">
    <i class="fas fa-crown" style="color: #f7b731;"></i> built with passion · 2026
  </p>
</div>

<!-- small typing animation -->
<script>
  (function() {
    const phrases = [
      'React · Node.js · MySQL',
      'SpringBoot · Flask · MongoDB',
      'Cloud · DSA · System Design',
      'Building ServerLink 🚀'
    ];
    let idx = 0;
    const el = document.getElementById('typing-text');
    if (!el) return;
    function updateText() {
      el.textContent = phrases[idx];
      idx = (idx + 1) % phrases.length;
    }
    updateText();
    setInterval(updateText, 3800);
  })();
</script>

</body>
</html>
