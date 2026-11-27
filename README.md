<!-- Portfolio.md with embedded CSS. Renders styled in VS Code preview, Typora, Obsidian and other viewers that allow inline HTML/CSS. GitHub strips <style>, so use index.html or GitHub Pages there. -->
<style>
  :root{--bg:#f6f9fc;--surface:#fff;--ink:#1e293b;--muted:#64748b;--line:#e2e8f0;--accent:#3b82f6;--accent-soft:#dbeafe;--teal-soft:#ccfbf1;--violet-soft:#ede9fe}
  body,.markdown-body,.vscode-body{background:var(--bg)!important;color:var(--ink)!important;font-family:system-ui,-apple-system,"Segoe UI",Roboto,sans-serif!important;line-height:1.65}
  .pf{max-width:1000px;margin:0 auto;padding:0 16px}
  .pf h1{font-size:2.4rem;letter-spacing:-.03em;border:0;margin-top:40px}
  .pf h2{letter-spacing:-.02em;border:0;margin-top:56px}
  .pf hr{border:0;height:1px;background:var(--line);margin:40px 0}
  .pf a{color:#1d4ed8;text-decoration:none}
  .pf a:hover{text-decoration:underline}
  .pf code{background:#f1f5f9;border:1px solid var(--line);border-radius:999px;padding:2px 10px;font-size:.82em;transition:transform .25s,border-color .25s;display:inline-block}
  .pf code:hover{transform:translateY(-3px) scale(1.06);border-color:var(--accent)}
  .pf blockquote{display:inline-block;margin:0 0 12px;padding:4px 14px;border:0;border-radius:999px;background:var(--teal-soft);color:#0f766e;font-weight:600}
  .pf blockquote p{margin:0}

  /* cards with a bubble that grows on hover */
  .pf .cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:18px;margin:18px 0}
  .pf .card{position:relative;overflow:hidden;isolation:isolate;background:var(--surface);border:1px solid var(--line);border-radius:18px;padding:8px 22px 14px;box-shadow:0 1px 2px rgba(15,23,42,.04),0 8px 24px rgba(15,23,42,.06);transition:transform .3s,border-color .3s}
  .pf .card::before{content:"";position:absolute;left:50%;top:50%;width:0;height:0;border-radius:50%;background:var(--accent-soft);transform:translate(-50%,-50%);transition:width .6s ease,height .6s ease;z-index:-1}
  .pf .card:hover{transform:translateY(-6px);border-color:#bfdbfe}
  .pf .card:hover::before{width:620px;height:620px}
  .pf .card.teal::before{background:var(--teal-soft)}   .pf .card.teal:hover{border-color:#99f6e4}
  .pf .card.violet::before{background:var(--violet-soft)} .pf .card.violet:hover{border-color:#ddd6fe}
  .pf .card h3{margin:14px 0 4px;font-size:1.1rem}
  .pf .card ul{padding-left:18px}
  .pf .card p{margin:6px 0}
  .pf .card table{width:100%}

  .pf .links a{display:inline-block;margin:4px 6px 4px 0;padding:9px 20px;border:1px solid var(--line);border-radius:999px;background:var(--surface);font-weight:600;transition:transform .25s,box-shadow .25s}
  .pf .links a:hover{transform:translateY(-3px);box-shadow:0 8px 24px rgba(15,23,42,.08);text-decoration:none}
  @media(prefers-reduced-motion:reduce){.pf *{transition:none!important}}
</style>

<div class="pf">

# Leela Krishna — Python Full Stack Developer

> Open to fresher roles

I build database-driven web apps with Python, Django and React, add AI/ML where it helps, and I'm learning identity governance with **SailPoint IdentityIQ**.

<div class="links">

[View projects](#projects) [Email me](mailto:lethavadlaleelakrishna@gmail.com) [GitHub](https://github.com/lethavadlaLeelaKrishna)

</div>

---

## About Me

B.Tech Computer Science graduate (JNTUK, 2022–2026, CGPA 7.71) from Guntur, Andhra Pradesh.

<div class="cards">

<div class="card">

### Full stack
*Python · Django · React*

Database-driven apps with REST APIs, authentication, carts and orders.

</div>

<div class="card teal">

### AI & ML
*NLP · Scikit-learn*

Data preprocessing, feature engineering, model training and evaluation.

</div>

<div class="card violet">

### Identity & access
*SailPoint IIQ · IAM/IGA*

Currently learning identity governance concepts and IdentityIQ.

</div>

</div>

---

## Technical Skills

<div class="cards">

<div class="card">

### Frontend

`HTML5` `CSS3` `JavaScript` `ReactJS` `Bootstrap` `Tailwind CSS`

</div>

<div class="card teal">

### Backend & Database

`Python` `Django` `REST APIs` `SQL` `MySQL` `SQLite`

</div>

<div class="card violet">

### AI / ML

`Machine Learning` `NLP` `EDA` `NumPy` `Pandas` `Scikit-learn`

</div>

<div class="card">

### Tools & Cloud

`Git` `GitHub` `VS Code` `AWS basics` `CI/CD` `Netlify` `Render`

</div>

<div class="card violet">

### SailPoint & IAM *(learning)*

`SailPoint IdentityIQ (IIQ)` `IAM` `IGA` `Access certifications` `Provisioning` `Roles & policies`

</div>

</div>

---

## Experience & Training

<div class="cards">

<div class="card">

### Python Full Stack Developer & Generative AI Training
**Achievers IT** · Offline · Apr 2026 – Aug 2026

- Trained in HTML5, CSS3, Bootstrap, Tailwind CSS, JavaScript, React, Python, SQL, MySQL and Django.
- Built full stack practice apps: React frontend, Django backend, SQL/MySQL integration.
- Learned Git, GitHub, CI/CD, AWS deployment fundamentals, and deployment on Netlify and Render.

</div>

<div class="card teal">

### AI & Machine Learning
**Inlignx Global Pvt. Ltd.** · Remote · Nov 2025 – Mar 2026

- Built ML solutions with Python, Pandas, NumPy and Scikit-learn: preprocessing, feature engineering, training and evaluation.
- Created an NLP text classification project with text preprocessing and feature extraction.
- Implemented end-to-end ML workflows including testing and performance optimisation.

</div>

</div>

---

## Projects

<div class="cards">

<div class="card">

### Price Negotiating Chatbot
*Text + voice · AI & NLP*

- E-commerce chatbot that evaluates offers and generates counter-offers.
- REST APIs and Web Speech API for chat, voice, cart and orders.
- Database for auth, products, sessions, chat history and orders.

`Python` `Django` `NLP`

</div>

<div class="card teal">

### Emotion Detection System
*AI & ML web app*

- Django app that detects emotions with a trained ML model.
- Python training script integrated into the web app.
- Results stored in SQLite and shown in the UI.

`Django` `ML` `SQLite`

</div>

<div class="card violet">

### Aegon Order
*E-commerce frontend*

- Multi-page site: home, products, details, offers, cart, login, signup.
- Responsive layouts and consistent UI.
- Client-side interactivity with JavaScript.

`HTML5` `CSS3` `JavaScript`

[View live →](https://lethavadlaleelakrishna.github.io/aegon_Order/)

</div>

<div class="card">

### KUSBLAKS · Training Institute Platform *(in progress)*
*ReactJS · Tailwind CSS · Space-inspired UI*

A modern, responsive platform for courses, training programs and institute information.

</div>

</div>

---

## Education & Certifications

<div class="cards">

<div class="card">

### B.Tech, Computer Science Engineering
Sri Mittapalli College of Engineering (JNTUK) · 2022–2026

CGPA 7.71

</div>

<div class="card teal">

### Certifications

- Full Stack UI Development, Coding Brains (2025)
- AI and Machine Learning Internship, Inlignx Global (2026)
- Python Full Stack & Generative AI, Achievers IT (2026)

*Languages: English, Telugu*

</div>

</div>

---

## Let's Connect

Looking for a fresher role in Python full stack, React or AI/ML, and happy to talk IAM too.

<div class="links">

[lethavadlaleelakrishna@gmail.com](mailto:lethavadlaleelakrishna@gmail.com) [+91 63093 69021](tel:+916309369021) [LinkedIn](https://www.linkedin.com/in/lethavadlaLeelaKrishna) [GitHub](https://github.com/lethavadlaLeelaKrishna)

</div>

---

© 2026 Lethavadla Leela Krishna · Guntur, Andhra Pradesh, India

</div>
