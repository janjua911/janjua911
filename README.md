<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
  <title>Hassan Janjua · AI & ML Engineer</title>
  <!-- Google Fonts + modern font stack -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700;14..32,800&display=swap" rel="stylesheet">
  <!-- Font Awesome 6 (free icons) -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: radial-gradient(circle at 10% 30%, #0B0F1C, #03050B);
      font-family: 'Inter', system-ui, -apple-system, 'Segoe UI', sans-serif;
      color: #EFF3FC;
      line-height: 1.5;
      padding: 2rem 1.5rem;
    }

    /* smooth blur effect container */
    .glass-card {
      background: rgba(15, 25, 45, 0.55);
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      border-radius: 2.5rem;
      border: 1px solid rgba(72, 187, 255, 0.18);
      box-shadow: 0 20px 35px -12px rgba(0,0,0,0.4), inset 0 1px 0 rgba(255,255,255,0.05);
      transition: transform 0.2s ease, border-color 0.2s;
    }

    .glass-card:hover {
      border-color: rgba(56, 189, 248, 0.5);
    }

    .container {
      max-width: 1280px;
      margin: 0 auto;
    }

    /* header area */
    .profile-header {
      text-align: center;
      padding: 2rem 2rem 1.8rem;
      margin-bottom: 2rem;
    }

    h1 {
      font-size: 3rem;
      font-weight: 800;
      background: linear-gradient(135deg, #FFFFFF, #A0D8FF, #5BC0FF);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
      letter-spacing: -0.02em;
      margin-bottom: 0.5rem;
    }

    .subhead {
      font-size: 1.25rem;
      font-weight: 500;
      color: #B9D0F0;
      border-bottom: 2px dashed rgba(91, 192, 255, 0.4);
      display: inline-block;
      padding-bottom: 6px;
      margin-top: 0.25rem;
    }

    .tagline {
      margin-top: 1rem;
      font-size: 1.1rem;
      color: #C7DEFC;
      background: rgba(0, 20, 40, 0.6);
      display: inline-block;
      padding: 0.5rem 1.8rem;
      border-radius: 60px;
      backdrop-filter: blur(4px);
      font-weight: 500;
    }

    /* social links */
    .social-links {
      display: flex;
      justify-content: center;
      gap: 1.5rem;
      margin-top: 1.8rem;
      flex-wrap: wrap;
    }

    .social-btn {
      background: rgba(20, 35, 55, 0.7);
      padding: 0.7rem 1.4rem;
      border-radius: 60px;
      font-weight: 600;
      font-size: 0.95rem;
      display: inline-flex;
      align-items: center;
      gap: 0.7rem;
      transition: all 0.25s;
      border: 1px solid rgba(72, 187, 255, 0.2);
      color: #EFF9FF;
      text-decoration: none;
      backdrop-filter: blur(4px);
    }

    .social-btn i {
      font-size: 1.2rem;
    }

    .social-btn:hover {
      background: #1E3A5F;
      border-color: #3b82f6;
      transform: translateY(-2px);
      box-shadow: 0 8px 18px rgba(0,160,255,0.2);
    }

    /* Grid layout 2 columns */
    .grid-2col {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
      gap: 1.8rem;
      margin-bottom: 2rem;
    }

    /* sections general style */
    .section-card {
      padding: 1.7rem 1.8rem;
      height: 100%;
    }

    .section-title {
      font-size: 1.5rem;
      font-weight: 700;
      margin-bottom: 1.2rem;
      display: flex;
      align-items: center;
      gap: 0.7rem;
      border-left: 4px solid #2E9AFF;
      padding-left: 1rem;
    }

    .section-title i {
      color: #2E9AFF;
      font-size: 1.4rem;
    }

    .about-text {
      font-size: 1rem;
      color: #DAECFF;
      line-height: 1.6;
    }

    .about-text p {
      margin-bottom: 0.8rem;
    }

    .tech-stack {
      display: flex;
      flex-wrap: wrap;
      gap: 0.65rem;
      margin-top: 1rem;
    }

    .tech-badge {
      background: rgba(40, 55, 85, 0.7);
      padding: 0.35rem 1rem;
      border-radius: 30px;
      font-size: 0.8rem;
      font-weight: 500;
      letter-spacing: 0.3px;
      backdrop-filter: blur(2px);
      transition: 0.2s;
      border: 1px solid rgba(100, 181, 246, 0.3);
    }

    .tech-badge i {
      margin-right: 6px;
      font-size: 0.75rem;
    }

    .tech-badge:hover {
      background: #2563eb40;
      border-color: #3b82f6;
    }

    /* Stats area */
    .stats-wrapper {
      display: flex;
      flex-direction: column;
      gap: 1.5rem;
    }

    .stat-block {
      background: rgba(10, 20, 35, 0.6);
      border-radius: 1.4rem;
      padding: 1rem;
      text-align: center;
      border: 1px solid rgba(72, 187, 255, 0.2);
    }

    .stat-img {
      width: 100%;
      max-width: 480px;
      margin: 0 auto;
      border-radius: 1rem;
    }

    .stat-img img {
      width: 100%;
      border-radius: 0.9rem;
      background: #0A1222;
    }

    /* achievements special */
    .trophy-row {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      margin: 1rem 0;
    }

    .trophy-row img {
      max-width: 100%;
      height: auto;
      background: transparent;
    }

    /* quote section */
    .quote-box {
      text-align: center;
      padding: 1.2rem;
      font-size: 1.1rem;
      font-style: italic;
      background: linear-gradient(115deg, rgba(25, 50, 75, 0.5), rgba(10, 25, 45, 0.7));
      border-radius: 2rem;
      margin-top: 1rem;
    }

    .quote-box i {
      color: #5bc0ff;
      margin: 0 8px;
    }

    .visit-count {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 12px;
      margin-top: 2rem;
      font-size: 0.9rem;
      color: #90b4e6;
    }

    hr {
      border: none;
      height: 1px;
      background: linear-gradient(90deg, transparent, #2E9AFF, #A855F7, transparent);
      margin: 1rem 0;
    }

    footer {
      text-align: center;
      font-size: 0.75rem;
      opacity: 0.7;
      margin-top: 2rem;
    }

    @media (max-width: 740px) {
      body {
        padding: 1rem;
      }
      h1 {
        font-size: 2.2rem;
      }
      .section-card {
        padding: 1.2rem;
      }
      .social-btn {
        padding: 0.5rem 1rem;
        font-size: 0.8rem;
      }
    }

    a {
      text-decoration: none;
    }

    /* badges inline for languages */
    .lang-badge-row {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin: 12px 0 0;
    }
  </style>
</head>
<body>
<div class="container">
  
  <!-- HEADER section with glass effect -->
  <div class="glass-card profile-header">
    <h1>Hi 👋, I'm Hassan Janjua</h1>
    <div class="subhead">CS Student · AI & Machine Learning Enthusiast 🤖</div>
    <div class="tagline">
      <i class="fas fa-code"></i> Building real-world projects • Learning by doing • Always improving 🚀
    </div>
    
    <!-- socials - modern interactive -->
    <div class="social-links">
      <a href="https://bsky.app/profile/janjua911" target="_blank" class="social-btn"><i class="fab fa-bluesky"></i> Bluesky</a>
      <a href="https://mastodon.social/@Hassan Afzal" target="_blank" class="social-btn"><i class="fab fa-mastodon"></i> Mastodon</a>
      <a href="mailto:hassanjanjua911@gmail.com" class="social-btn"><i class="fas fa-envelope"></i> Email</a>
    </div>
  </div>

  <!-- MAIN 2-COLUMN GRID: About + Tech Overview -->
  <div class="grid-2col">
    <!-- About Me area -->
    <div class="glass-card section-card">
      <div class="section-title">
        <i class="fas fa-user-astronaut"></i>
        <span>💫 About Me</span>
      </div>
      <div class="about-text">
        <p>🎓 Computer Science student at <strong>COMSATS University Islamabad</strong></p>
        <p>🤖 Interested in <strong>AI, Machine Learning & Model Training</strong></p>
        <p>🔐 Exploring <strong>Cryptography & System Design</strong></p>
        <p>💻 Backend + Frontend developer mindset</p>
        <p>🌱 Always curious. Always learning.</p>
      </div>
    </div>

    <!-- Tech Stack (compact, modern badges) -->
    <div class="glass-card section-card">
      <div class="section-title">
        <i class="fas fa-laptop-code"></i>
        <span>💻 Core Stack</span>
      </div>
      <div>
        <div style="margin-bottom: 1rem;"><strong>🚀 Languages:</strong></div>
        <div class="tech-stack">
          <span class="tech-badge"><i class="fab fa-cuttlefish"></i> C</span>
          <span class="tech-badge"><i class="fab fa-cuttlefish"></i> C++</span>
          <span class="tech-badge"><i class="fab fa-python"></i> Python</span>
          <span class="tech-badge"><i class="fab fa-java"></i> Java</span>
        </div>
        <div style="margin: 1rem 0 0.6rem;"><strong>🌐 Web & App:</strong></div>
        <div class="tech-stack">
          <span class="tech-badge">HTML5</span>
          <span class="tech-badge">JavaScript</span>
          <span class="tech-badge">React</span>
          <span class="tech-badge">Angular</span>
          <span class="tech-badge">FastAPI</span>
          <span class="tech-badge">Flask</span>
          <span class="tech-badge">Flutter</span>
        </div>
        <div style="margin: 1rem 0 0.6rem;"><strong>🧠 AI/ML:</strong></div>
        <div class="tech-stack">
          <span class="tech-badge">NumPy</span>
          <span class="tech-badge">Pandas</span>
          <span class="tech-badge">TensorFlow</span>
          <span class="tech-badge">PyTorch</span>
          <span class="tech-badge">Scikit-Learn</span>
        </div>
        <div style="margin: 1rem 0 0.6rem;"><strong>☁️ Cloud & DB:</strong></div>
        <div class="tech-stack">
          <span class="tech-badge">AWS</span>
          <span class="tech-badge">Azure</span>
          <span class="tech-badge">Firebase</span>
          <span class="tech-badge">PostgreSQL</span>
          <span class="tech-badge">MySQL</span>
        </div>
      </div>
    </div>
  </div>

  <!-- STATS SECTION: GitHub Stats, Streak, Top Languages in a clean row using flex/grid -->
  <div class="glass-card section-card" style="margin-bottom: 2rem;">
    <div class="section-title">
      <i class="fas fa-chart-line"></i>
      <span>📊 GitHub Analytics</span>
    </div>
    <div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 1.2rem; align-items: center;">
      <!-- GitHub Stats Card -->
      <div class="stat-block" style="flex: 1; min-width: 240px;">
        <img class="stat-img" src="https://github-readme-stats.vercel.app/api?username=janjua911&show_icons=true&theme=dark&hide_border=true&bg_color=0D1117&title_color=5BC0FF&icon_color=5BC0FF" alt="GitHub Stats">
      </div>
      <!-- Streak Stats -->
      <div class="stat-block" style="flex: 1; min-width: 240px;">
        <img class="stat-img" src="https://github-readme-streak-stats.herokuapp.com/?user=janjua911&theme=dark&hide_border=true&background=0D1117&ring=5BC0FF&fire=FFA500&currStreakLabel=5BC0FF" alt="Streak Stats">
      </div>
      <!-- Top Languages -->
      <div class="stat-block" style="flex: 1; min-width: 240px;">
        <img class="stat-img" src="https://github-readme-stats.vercel.app/api/top-langs/?username=janjua911&layout=compact&theme=dark&hide_border=true&bg_color=0D1117&title_color=5BC0FF" alt="Top Languages">
      </div>
    </div>
  </div>

  <!-- ACHIEVEMENTS + Trophy with modern styling -->
  <div class="glass-card section-card" style="margin-bottom: 2rem;">
    <div class="section-title">
      <i class="fas fa-trophy"></i>
      <span>🏆 Achievements & Milestones</span>
    </div>
    <div class="trophy-row">
      <img src="https://github-profile-trophy.vercel.app/?username=janjua911&theme=radical&no-frame=true&margin-w=10&column=4" alt="GitHub Trophies" style="max-width: 100%; border-radius: 16px;">
    </div>
    <div style="text-align: center; margin-top: 12px; font-size: 0.85rem; color: #b3d4ff;">
      <i class="fas fa-medal"></i> Open source contributor · AI model experiments · Hackathon participant
    </div>
  </div>

  <!-- DEV QUOTE + VISIT COUNT combined row -->
  <div class="grid-2col" style="margin-bottom: 1rem;">
    <div class="glass-card section-card" style="display: flex; flex-direction: column; justify-content: center;">
      <div class="section-title">
        <i class="fas fa-quote-right"></i>
        <span>✍️ Dev Quote</span>
      </div>
      <div class="quote-box">
        <i class="fas fa-code"></i>  
        <!-- Embed dynamic quote from API but keep design stable, fallback inline text -->
        <span id="dynamic-quote">Loading wisdom...</span>
        <i class="fas fa-microchip"></i>
      </div>
      <p style="font-size: 0.7rem; text-align: center; margin-top: 12px;">✨ “Code. Train. Deploy. Repeat.”</p>
    </div>

    <!-- Visit Counter widget + additional clean info -->
    <div class="glass-card section-card" style="display: flex; flex-direction: column; align-items: center; justify-content: center;">
      <div class="section-title">
        <i class="fas fa-eye"></i>
        <span>Profile Radar</span>
      </div>
      <div class="visit-count">
        <i class="fas fa-globe" style="font-size: 1.3rem;"></i>
        <span style="font-weight: 500;">Total visits:</span>
        <!-- professional counter badge from visitcount.itsvg.in (original style but matching) -->
        <img src="https://visitcount.itsvg.in/api?id=janjua911&icon=5&color=6" alt="visit counter" style="border-radius: 30px; background: rgba(21, 32, 55, 0.8); padding: 4px 12px;">
      </div>
      <hr style="width: 80%;">
      <div style="text-align: center; margin-top: 8px;">
        <i class="fas fa-map-marker-alt"></i> Pakistan · <i class="fas fa-clock"></i> UTC+5
        <br>
        <i class="fas fa-brain"></i> Currently: LLM fine-tuning & crypto protocols
      </div>
    </div>
  </div>

  <!-- footer with extra social vibe -->
  <footer>
    <i class="fas fa-satellite-dish"></i> constantly building & iterating — always open to collab
    <br>© Hassan Janjua · AI/ML Student
  </footer>
</div>

<!-- Fetch a random programming quote for polish (public API) -->
<script>
  (async function fetchQuote() {
    const quoteElement = document.getElementById('dynamic-quote');
    try {
      const response = await fetch('https://api.quotable.io/random?tags=technology|programming');
      if (response.ok) {
        const data = await response.json();
        quoteElement.innerHTML = `❝ ${data.content} ❞ — ${data.author}`;
      } else {
        quoteElement.innerHTML = `❝ First, solve the problem. Then, write the code. ❞ — John Johnson`;
      }
    } catch (err) {
      quoteElement.innerHTML = `❝ The only way to learn a new programming language is by writing programs in it. ❞ — Dennis Ritchie`;
    }
  })();
</script>

<!-- optional dynamic hover enhancements: no extra library, just styles -->
</body>
</html>
