<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Leela Krishna · Python Full Stack Developer</title>
<meta name="description" content="Portfolio of Lethavadla Leela Krishna: Python Full Stack, React, Django, AI/ML and SailPoint IdentityIQ (IAM/IGA).">
<style>
  :root{
    --bg:#f6f9fc; --surface:#ffffff; --ink:#1e293b; --muted:#64748b;
    --line:#e2e8f0; --accent:#3b82f6; --accent-soft:#dbeafe;
    --teal:#14b8a6; --teal-soft:#ccfbf1; --violet:#8b5cf6; --violet-soft:#ede9fe;
    --radius:18px; --shadow:0 1px 2px rgba(15,23,42,.04),0 8px 24px rgba(15,23,42,.06);
  }
  *{box-sizing:border-box;margin:0}
  html{scroll-behavior:smooth}
  body{font:16px/1.65 system-ui,-apple-system,"Segoe UI",Roboto,sans-serif;color:var(--ink);background:var(--bg);overflow-x:hidden}
  a{color:inherit;text-decoration:none}
  .wrap{max-width:1080px;margin:0 auto;padding:0 20px}
  section{padding:72px 0}
  h2{font-size:clamp(1.5rem,3vw,2rem);letter-spacing:-.02em;margin-bottom:8px}
  .sub{color:var(--muted);margin-bottom:32px;max-width:60ch}

  /* floating background bubbles */
  .bg{position:fixed;inset:0;z-index:-1;overflow:hidden;pointer-events:none}
  .bg i{position:absolute;border-radius:50%;filter:blur(2px);opacity:.55;animation:float 18s ease-in-out infinite}
  .bg i:nth-child(1){width:320px;height:320px;left:-80px;top:10%;background:var(--accent-soft)}
  .bg i:nth-child(2){width:220px;height:220px;right:-40px;top:30%;background:var(--teal-soft);animation-delay:-6s}
  .bg i:nth-child(3){width:260px;height:260px;left:40%;bottom:-90px;background:var(--violet-soft);animation-delay:-11s}
  @keyframes float{50%{transform:translateY(-28px) scale(1.06)}}

  /* nav */
  nav{position:sticky;top:0;z-index:10;background:rgba(246,249,252,.82);backdrop-filter:blur(10px);border-bottom:1px solid var(--line)}
  nav .wrap{display:flex;align-items:center;justify-content:space-between;height:60px}
  .logo{font-weight:700;letter-spacing:-.02em}
  .logo b{color:var(--accent)}
  nav ul{display:flex;gap:6px;list-style:none;padding:0}
  nav a{padding:7px 12px;border-radius:999px;font-size:.92rem;color:var(--muted);transition:.25s}
  nav a:hover{background:var(--accent-soft);color:#1d4ed8;transform:translateY(-2px)}

  /* hero */
  .hero{padding:88px 0 56px}
  .hero .wrap{display:grid;grid-template-columns:1.3fr .7fr;gap:40px;align-items:center}
  .tag{display:inline-block;background:var(--teal-soft);color:#0f766e;padding:5px 14px;border-radius:999px;font-size:.85rem;font-weight:600}
  h1{font-size:clamp(2.1rem,5vw,3.4rem);line-height:1.1;letter-spacing:-.03em;margin:16px 0 14px}
  h1 span{background:linear-gradient(90deg,var(--accent),var(--teal));-webkit-background-clip:text;background-clip:text;color:transparent}
  .lead{color:var(--muted);max-width:56ch;margin-bottom:26px}
  .btns{display:flex;flex-wrap:wrap;gap:12px}
  .btn{position:relative;overflow:hidden;padding:11px 22px;border-radius:999px;font-weight:600;font-size:.95rem;border:1px solid var(--line);background:var(--surface);transition:transform .25s,box-shadow .25s}
  .btn.primary{background:var(--accent);color:#fff;border-color:var(--accent)}
  .btn:hover{transform:translateY(-3px);box-shadow:var(--shadow)}
  .avatar{aspect-ratio:1;width:100%;border-radius:50%;max-width:280px;margin:auto;display:grid;place-items:center;font-size:4.5rem;font-weight:800;color:#fff;
    background:radial-gradient(circle at 30% 25%,#93c5fd,var(--accent) 55%,#0d9488);box-shadow:0 20px 50px rgba(59,130,246,.3);animation:float 9s ease-in-out infinite}

  /* bubble hover: a circle grows from the cursor position */
  .bubble{position:relative;overflow:hidden;isolation:isolate}
  .bubble::before{content:"";position:absolute;left:var(--x,50%);top:var(--y,50%);width:0;height:0;border-radius:50%;
    background:var(--hover,var(--accent-soft));transform:translate(-50%,-50%);transition:width .55s ease,height .55s ease;z-index:-1}
  .bubble:hover::before{width:520px;height:520px}

  /* cards */
  .grid{display:grid;gap:18px}
  .g2{grid-template-columns:repeat(2,1fr)} .g3{grid-template-columns:repeat(3,1fr)}
  .card{background:var(--surface);border:1px solid var(--line);border-radius:var(--radius);padding:24px;box-shadow:var(--shadow);transition:transform .3s,border-color .3s}
  .card:hover{transform:translateY(-6px);border-color:#bfdbfe}
  .card h3{font-size:1.08rem;margin-bottom:4px}
  .meta{color:var(--muted);font-size:.88rem;margin-bottom:10px}
  .card ul{padding-left:18px;color:#334155;font-size:.95rem} .card li{margin:5px 0}
  .card.teal{--hover:var(--teal-soft)} .card.violet{--hover:var(--violet-soft)}
  .card.teal:hover{border-color:#99f6e4} .card.violet:hover{border-color:#ddd6fe}

  /* chips */
  .chips{display:flex;flex-wrap:wrap;gap:8px;margin-top:12px}
  .chip{padding:6px 14px;border-radius:999px;background:#f1f5f9;border:1px solid var(--line);font-size:.86rem;font-weight:500;transition:transform .25s,border-color .25s}
  .chip:hover{transform:translateY(-3px) scale(1.06);border-color:var(--accent)}
  .badge{display:inline-block;margin-left:8px;background:var(--violet-soft);color:#6d28d9;padding:2px 10px;border-radius:999px;font-size:.72rem;font-weight:700;vertical-align:middle}

  .timeline{border-left:2px solid var(--line);padding-left:22px;display:grid;gap:18px}
  .timeline .card{position:relative}
  .timeline .card::after{content:"";position:absolute;left:-30px;top:30px;width:12px;height:12px;border-radius:50%;background:var(--accent);box-shadow:0 0 0 4px var(--accent-soft)}

  .contact{text-align:center}
  .contact .btns{justify-content:center}
  footer{text-align:center;color:var(--muted);font-size:.88rem;padding:28px 0 40px}

  .reveal{opacity:0;transform:translateY(18px);transition:opacity .7s,transform .7s}
  .reveal.in{opacity:1;transform:none}

  @media(max-width:820px){
    .hero .wrap,.g2,.g3{grid-template-columns:1fr}
    .avatar{max-width:200px;order:-1}
    nav ul{display:none}
  }
  @media(prefers-reduced-motion:reduce){
    *{animation:none!important;transition:none!important} .reveal{opacity:1;transform:none}
  }
</style>
</head>
<body>
<div class="bg" aria-hidden="true"><i></i><i></i><i></i></div>

<nav>
  <div class="wrap">
    <a class="logo" href="#top">Leela<b>.</b>Krishna</a>
    <ul>
      <li><a href="#about">About</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#experience">Experience</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </div>
</nav>

<header class="hero" id="top">
  <div class="wrap">
    <div>
      <span class="tag">Open to fresher roles</span>
      <h1>Hi, I'm <span>Leela Krishna</span><br>Python Full Stack Developer</h1>
      <p class="lead">I build database-driven web apps with Python, Django and React, add AI/ML where it helps, and I'm learning identity governance with SailPoint IdentityIQ.</p>
      <div class="btns">
        <a class="btn primary bubble" style="--hover:#2563eb" href="#projects">View projects</a>
        <a class="btn bubble" href="mailto:lethavadlaleelakrishna@gmail.com">Email me</a>
        <a class="btn bubble" href="https://github.com/lethavadlaLeelaKrishna" target="_blank" rel="noopener">GitHub</a>
      </div>
    </div>
    <div class="avatar" aria-label="Initials LK">LK</div>
  </div>
</header>

<section id="about">
  <div class="wrap reveal">
    <h2>About me</h2>
    <p class="sub">B.Tech Computer Science graduate (JNTUK, 2022–2026, CGPA 7.71) from Guntur, Andhra Pradesh.</p>
    <div class="grid g3">
      <div class="card bubble"><h3>Full stack</h3><p class="meta">Python · Django · React</p><p>Database-driven apps with REST APIs, authentication, carts and orders.</p></div>
      <div class="card teal bubble"><h3>AI &amp; ML</h3><p class="meta">NLP · Scikit-learn</p><p>Data preprocessing, feature engineering, model training and evaluation.</p></div>
      <div class="card violet bubble"><h3>Identity &amp; access</h3><p class="meta">SailPoint IIQ · IAM/IGA</p><p>Currently learning identity governance concepts and IdentityIQ.</p></div>
    </div>
  </div>
</section>

<section id="skills">
  <div class="wrap reveal">
    <h2>Technical skills</h2>
    <p class="sub">Tools I use to design, build and ship.</p>
    <div class="grid g2">
      <div class="card bubble"><h3>Frontend</h3><div class="chips"><span class="chip">HTML5</span><span class="chip">CSS3</span><span class="chip">JavaScript</span><span class="chip">ReactJS</span><span class="chip">Bootstrap</span><span class="chip">Tailwind CSS</span></div></div>
      <div class="card teal bubble"><h3>Backend &amp; database</h3><div class="chips"><span class="chip">Python</span><span class="chip">Django</span><span class="chip">REST APIs</span><span class="chip">SQL</span><span class="chip">MySQL</span><span class="chip">SQLite</span></div></div>
      <div class="card violet bubble"><h3>AI / ML</h3><div class="chips"><span class="chip">Machine Learning</span><span class="chip">NLP</span><span class="chip">EDA</span><span class="chip">NumPy</span><span class="chip">Pandas</span><span class="chip">Scikit-learn</span></div></div>
      <div class="card bubble"><h3>Tools &amp; cloud</h3><div class="chips"><span class="chip">Git</span><span class="chip">GitHub</span><span class="chip">VS Code</span><span class="chip">AWS basics</span><span class="chip">CI/CD</span><span class="chip">Netlify</span><span class="chip">Render</span></div></div>
    </div>
    <div class="card violet bubble" style="margin-top:18px">
      <h3>SailPoint &amp; IAM <span class="badge">Learning</span></h3>
      <p class="meta">Identity governance and administration</p>
      <div class="chips"><span class="chip">SailPoint IdentityIQ (IIQ)</span><span class="chip">IAM</span><span class="chip">IGA</span><span class="chip">Access certifications</span><span class="chip">Provisioning</span><span class="chip">Roles &amp; policies</span></div>
    </div>
  </div>
</section>

<section id="experience">
  <div class="wrap reveal">
    <h2>Experience &amp; training</h2>
    <p class="sub">Hands-on internship and structured full stack training.</p>
    <div class="timeline">
      <div class="card bubble">
        <h3>Python Full Stack Developer &amp; Generative AI Training</h3>
        <p class="meta">Achievers IT · Offline · Apr 2026 – Aug 2026</p>
        <ul>
          <li>Trained in HTML5, CSS3, Bootstrap, Tailwind CSS, JavaScript, React, Python, SQL, MySQL and Django.</li>
          <li>Built full stack practice apps: React frontend, Django backend, SQL/MySQL integration.</li>
          <li>Learned Git, GitHub, CI/CD, AWS deployment fundamentals, and deployment on Netlify and Render.</li>
        </ul>
      </div>
      <div class="card teal bubble">
        <h3>AI &amp; Machine Learning</h3>
        <p class="meta">Inlignx Global Pvt. Ltd. · Remote · Nov 2025 – Mar 2026</p>
        <ul>
          <li>Built ML solutions with Python, Pandas, NumPy and Scikit-learn: preprocessing, feature engineering, training and evaluation.</li>
          <li>Created an NLP text classification project with text preprocessing and feature extraction.</li>
          <li>Implemented end-to-end ML workflows including testing and performance optimisation.</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<section id="projects">
  <div class="wrap reveal">
    <h2>Projects</h2>
    <p class="sub">Selected work across AI, full stack and frontend.</p>
    <div class="grid g3">
      <article class="card bubble">
        <h3>Price Negotiating Chatbot</h3>
        <p class="meta">Text + voice · AI &amp; NLP</p>
        <ul><li>E-commerce chatbot that evaluates offers and generates counter-offers.</li><li>REST APIs and Web Speech API for chat, voice, cart and orders.</li><li>Database for auth, products, sessions, chat history and orders.</li></ul>
        <div class="chips"><span class="chip">Python</span><span class="chip">Django</span><span class="chip">NLP</span></div>
      </article>
      <article class="card teal bubble">
        <h3>Emotion Detection System</h3>
        <p class="meta">AI &amp; ML web app</p>
        <ul><li>Django app that detects emotions with a trained ML model.</li><li>Python training script integrated into the web app.</li><li>Results stored in SQLite and shown in the UI.</li></ul>
        <div class="chips"><span class="chip">Django</span><span class="chip">ML</span><span class="chip">SQLite</span></div>
      </article>
      <article class="card violet bubble">
        <h3>Aegon Order</h3>
        <p class="meta">E-commerce frontend</p>
        <ul><li>Multi-page site: home, products, details, offers, cart, login, signup.</li><li>Responsive layouts and consistent UI.</li><li>Client-side interactivity with JavaScript.</li></ul>
        <div class="chips"><span class="chip">HTML5</span><span class="chip">CSS3</span><span class="chip">JavaScript</span></div>
        <p style="margin-top:12px"><a href="https://lethavadlaleelakrishna.github.io/aegon_Order/" target="_blank" rel="noopener" style="color:#6d28d9;font-weight:600">View live →</a></p>
      </article>
    </div>
    <div class="card bubble" style="margin-top:18px">
      <h3>KUSBLAKS · Training Institute Platform <span class="badge">In progress</span></h3>
      <p class="meta">ReactJS · Tailwind CSS · Space-inspired UI</p>
      <p>A modern, responsive platform for courses, training programs and institute information.</p>
    </div>
  </div>
</section>

<section id="education">
  <div class="wrap reveal">
    <h2>Education &amp; certifications</h2>
    <p class="sub">&nbsp;</p>
    <div class="grid g2">
      <div class="card bubble"><h3>B.Tech, Computer Science Engineering</h3><p class="meta">Sri Mittapalli College of Engineering (JNTUK) · 2022–2026</p><p>CGPA 7.71</p></div>
      <div class="card teal bubble"><h3>Certifications</h3>
        <ul><li>Full Stack UI Development, Coding Brains (2025)</li><li>AI and Machine Learning Internship, Inlignx Global (2026)</li><li>Python Full Stack &amp; Generative AI, Achievers IT (2026)</li></ul>
        <p class="meta" style="margin-top:10px">Languages: English, Telugu</p></div>
    </div>
  </div>
</section>

<section id="contact" class="contact">
  <div class="wrap reveal">
    <h2>Let's connect</h2>
    <p class="sub" style="margin-inline:auto">Looking for a fresher role in Python full stack, React or AI/ML, and happy to talk IAM too.</p>
    <div class="btns">
      <a class="btn primary bubble" style="--hover:#2563eb" href="mailto:lethavadlaleelakrishna@gmail.com">lethavadlaleelakrishna@gmail.com</a>
      <a class="btn bubble" href="tel:+916309369021">+91 63093 69021</a>
      <a class="btn bubble" href="https://www.linkedin.com/in/lethavadlaLeelaKrishna" target="_blank" rel="noopener">LinkedIn</a>
      <a class="btn bubble" href="https://github.com/lethavadlaLeelaKrishna" target="_blank" rel="noopener">GitHub</a>
    </div>
  </div>
</section>

<footer>© 2026 Lethavadla Leela Krishna · Guntur, Andhra Pradesh, India</footer>

<script>
  // Bubble hover: start the growing circle at the cursor position
  document.querySelectorAll('.bubble').forEach(el=>{
    el.addEventListener('pointerenter',e=>{
      const r=el.getBoundingClientRect();
      el.style.setProperty('--x',(e.clientX-r.left)+'px');
      el.style.setProperty('--y',(e.clientY-r.top)+'px');
    });
  });
  // Fade-in on scroll
  const io=new IntersectionObserver(es=>es.forEach(x=>{if(x.isIntersecting){x.target.classList.add('in');io.unobserve(x.target)}}),{threshold:.12});
  document.querySelectorAll('.reveal').forEach(el=>io.observe(el));
</script>
</body>
</html>
