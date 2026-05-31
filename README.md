<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Akanksha Kesarkar — Portfolio</title>
<link rel="preconnect" href="https://fonts.googleapis.com"/>
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin/>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=Syne:wght@400;500;600;700;800&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;1,9..40,300&display=swap" rel="stylesheet"/>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css"/>
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --bg:#07080f;--bg2:#0d0e1a;
  --surface:rgba(255,255,255,0.03);
  --border:rgba(124,58,237,0.2);--border-h:rgba(124,58,237,0.5);
  --primary:#7c3aed;--primary-l:#a78bfa;
  --cyan:#22d3ee;--text:#e8e4f0;--muted:#7c7592;
}
html{scroll-behavior:smooth}
body{font-family:'DM Sans',sans-serif;background:var(--bg);color:var(--text);overflow-x:hidden;cursor:none}
.cursor{position:fixed;width:10px;height:10px;background:var(--primary-l);border-radius:50%;pointer-events:none;z-index:9999;transform:translate(-50%,-50%);transition:transform .15s,background .3s,width .3s,height .3s}
.cursor-ring{position:fixed;width:34px;height:34px;border:1.5px solid rgba(167,139,250,.45);border-radius:50%;pointer-events:none;z-index:9998;transform:translate(-50%,-50%);transition:width .3s,height .3s}
body::after{content:'';position:fixed;inset:0;background:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='300' height='300'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.85' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='.04'/%3E%3C/svg%3E");pointer-events:none;z-index:100}

/* NAV */
nav{position:fixed;top:0;left:0;right:0;z-index:500;padding:18px 64px;display:flex;justify-content:space-between;align-items:center;backdrop-filter:blur(20px);background:rgba(7,8,15,.75);border-bottom:1px solid rgba(124,58,237,.1);transition:border-color .3s}
.nav-logo{font-family:'Cormorant Garamond',serif;font-size:1.3rem;font-weight:600;color:var(--primary-l);letter-spacing:.06em}
.nav-links{display:flex;gap:36px;list-style:none}
.nav-links a{font-family:'Syne',sans-serif;font-size:.75rem;font-weight:500;letter-spacing:.14em;text-transform:uppercase;color:var(--muted);text-decoration:none;transition:color .3s}
.nav-links a:hover{color:var(--primary-l)}

/* HERO */
#hero{min-height:100vh;display:flex;align-items:center;position:relative;overflow:hidden;padding:130px 64px 80px}
.hero-grid{position:absolute;inset:0;background-image:linear-gradient(rgba(124,58,237,.04) 1px,transparent 1px),linear-gradient(90deg,rgba(124,58,237,.04) 1px,transparent 1px);background-size:58px 58px;mask-image:radial-gradient(ellipse at 50% 50%,black 40%,transparent 80%)}
.orb{position:absolute;border-radius:50%;filter:blur(90px);pointer-events:none}
.o1{width:650px;height:650px;background:radial-gradient(circle,rgba(124,58,237,.38) 0%,transparent 70%);top:-180px;right:-80px;animation:fl 9s ease-in-out infinite}
.o2{width:420px;height:420px;background:radial-gradient(circle,rgba(34,211,238,.22) 0%,transparent 70%);bottom:-80px;left:60px;animation:fl 12s ease-in-out infinite reverse}
.o3{width:280px;height:280px;background:radial-gradient(circle,rgba(167,139,250,.18) 0%,transparent 70%);top:42%;left:44%;animation:fl 7s ease-in-out 1.5s infinite}
@keyframes fl{0%,100%{transform:translate(0,0) scale(1)}40%{transform:translate(-25px,28px) scale(1.07)}70%{transform:translate(18px,-16px) scale(.94)}}
.hero-content{position:relative;z-index:2;max-width:920px}
.hero-tag{display:inline-flex;align-items:center;gap:9px;font-family:'Syne',sans-serif;font-size:.72rem;font-weight:600;letter-spacing:.16em;text-transform:uppercase;color:var(--cyan);border:1px solid rgba(34,211,238,.3);border-radius:100px;padding:6px 18px;margin-bottom:34px;opacity:0;animation:fu .8s ease .1s forwards}
.hero-tag::before{content:'';width:6px;height:6px;background:var(--cyan);border-radius:50%;animation:pls 2s infinite}
@keyframes pls{0%,100%{opacity:1;transform:scale(1)}50%{opacity:.45;transform:scale(1.6)}}
.hero-name{font-family:'Cormorant Garamond',serif;font-size:clamp(58px,8.5vw,118px);font-weight:300;line-height:.94;color:#faf5ff;letter-spacing:-.025em;margin-bottom:28px;opacity:0;animation:fu .85s ease .22s forwards}
.hero-name em{font-style:italic;color:var(--primary-l)}
.hero-sub{font-family:'Syne',sans-serif;font-size:.9rem;font-weight:500;letter-spacing:.08em;text-transform:uppercase;color:var(--primary-l);margin-bottom:18px;opacity:0;animation:fu .85s ease .35s forwards}
.hero-desc{font-size:1.05rem;font-weight:300;color:var(--muted);max-width:540px;line-height:1.85;margin-bottom:50px;opacity:0;animation:fu .85s ease .45s forwards}
.hero-cta{display:flex;gap:14px;flex-wrap:wrap;opacity:0;animation:fu .85s ease .58s forwards}
.btn-p{display:inline-flex;align-items:center;gap:10px;background:var(--primary);color:#fff;padding:14px 32px;border-radius:8px;text-decoration:none;font-family:'Syne',sans-serif;font-size:.82rem;font-weight:700;letter-spacing:.06em;transition:all .3s;border:1px solid transparent}
.btn-p:hover{background:transparent;border-color:var(--primary);color:var(--primary-l);transform:translateY(-2px)}
.btn-o{display:inline-flex;align-items:center;gap:10px;background:transparent;color:var(--text);padding:14px 32px;border-radius:8px;text-decoration:none;font-family:'Syne',sans-serif;font-size:.82rem;font-weight:700;letter-spacing:.06em;border:1px solid rgba(255,255,255,.15);transition:all .3s}
.btn-o:hover{border-color:var(--primary-l);color:var(--primary-l);transform:translateY(-2px)}
.hero-socials{position:absolute;right:64px;bottom:64px;display:flex;flex-direction:column;gap:14px;align-items:center;opacity:0;animation:fu .85s ease .7s forwards}
.hero-socials::before{content:'';width:1px;height:56px;background:linear-gradient(transparent,var(--border))}
.hero-socials a{color:var(--muted);font-size:1.05rem;text-decoration:none;transition:all .3s;width:38px;height:38px;display:flex;align-items:center;justify-content:center;border-radius:8px;border:1px solid transparent}
.hero-socials a:hover{color:var(--primary-l);border-color:var(--border);transform:translateX(-3px)}
.scroll-hint{position:absolute;bottom:36px;left:64px;display:flex;align-items:center;gap:10px;font-family:'Syne',sans-serif;font-size:.68rem;font-weight:600;letter-spacing:.18em;text-transform:uppercase;color:var(--muted);opacity:0;animation:fu .85s ease .85s forwards}
.scroll-hint::before{content:'';width:24px;height:1px;background:var(--muted)}
@keyframes fu{from{opacity:0;transform:translateY(28px)}to{opacity:1;transform:translateY(0)}}

/* SECTIONS */
section{padding:120px 64px}
.sec-label{font-family:'Syne',sans-serif;font-size:.7rem;font-weight:700;letter-spacing:.22em;text-transform:uppercase;color:var(--primary-l);margin-bottom:14px;display:flex;align-items:center;gap:14px}
.sec-label::before{content:'';width:28px;height:1px;background:var(--primary-l);flex-shrink:0}
.sec-title{font-family:'Cormorant Garamond',serif;font-size:clamp(40px,5vw,66px);font-weight:300;color:#faf5ff;line-height:1.08;margin-bottom:56px;letter-spacing:-.015em}
.sec-title em{font-style:italic;color:var(--primary-l)}

/* ABOUT */
#about{background:var(--bg2)}
.about-grid{display:grid;grid-template-columns:1fr 1fr;gap:72px;align-items:start}
.about-p{font-size:1rem;font-weight:300;line-height:1.9;color:rgba(232,228,240,.72);margin-bottom:22px}
.about-p strong{color:var(--primary-l);font-weight:500}
.stats-row{display:grid;grid-template-columns:repeat(3,1fr);gap:16px;margin-top:44px}
.stat-card{background:var(--surface);border:1px solid var(--border);border-radius:12px;padding:22px 20px;text-align:center;backdrop-filter:blur(16px)}
.stat-num{font-family:'Cormorant Garamond',serif;font-size:2.8rem;font-weight:600;color:var(--primary-l);line-height:1;margin-bottom:5px}
.stat-lbl{font-family:'Syne',sans-serif;font-size:.68rem;font-weight:600;letter-spacing:.12em;text-transform:uppercase;color:var(--muted)}
.info-card{background:var(--surface);border:1px solid var(--border);border-radius:16px;padding:32px;backdrop-filter:blur(20px)}
.info-item{display:flex;align-items:flex-start;gap:14px;padding:16px 0;border-bottom:1px solid rgba(255,255,255,.05)}
.info-item:last-child{border-bottom:none;padding-bottom:0}
.info-icon{width:36px;height:36px;background:rgba(124,58,237,.14);border-radius:8px;display:flex;align-items:center;justify-content:center;color:var(--primary-l);font-size:.88rem;flex-shrink:0}
.info-lbl{font-family:'Syne',sans-serif;font-size:.68rem;font-weight:700;letter-spacing:.12em;text-transform:uppercase;color:var(--muted);margin-bottom:4px}
.info-val{font-size:.9rem;color:var(--text);font-weight:400;line-height:1.5}

/* SKILLS */
.skills-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:20px}
.sk-cat{background:var(--surface);border:1px solid var(--border);border-radius:14px;padding:26px;backdrop-filter:blur(20px);transition:border-color .3s,transform .3s}
.sk-cat:hover{border-color:var(--border-h);transform:translateY(-4px)}
.sk-cat-ttl{font-family:'Syne',sans-serif;font-size:.72rem;font-weight:700;letter-spacing:.15em;text-transform:uppercase;color:var(--cyan);margin-bottom:18px;display:flex;align-items:center;gap:8px}
.sk-tags{display:flex;flex-wrap:wrap;gap:7px}
.sk-tag{background:rgba(124,58,237,.1);border:1px solid rgba(124,58,237,.24);border-radius:6px;padding:5px 12px;font-size:.8rem;color:var(--text);transition:all .2s}
.sk-tag:hover{background:rgba(124,58,237,.22);color:var(--primary-l)}

/* PROJECTS */
#projects{background:var(--bg2)}
.feat-proj{display:grid;grid-template-columns:1fr 1fr;gap:52px;align-items:center;background:var(--surface);border:1px solid var(--border);border-radius:20px;padding:52px;margin-bottom:36px;backdrop-filter:blur(20px);position:relative;overflow:hidden}
.feat-proj::before{content:'';position:absolute;top:0;left:0;right:0;height:2px;background:linear-gradient(90deg,var(--primary),var(--cyan))}
.proj-badge{display:inline-flex;align-items:center;gap:6px;background:rgba(34,211,238,.08);border:1px solid rgba(34,211,238,.28);border-radius:100px;padding:5px 14px;font-family:'Syne',sans-serif;font-size:.68rem;font-weight:700;letter-spacing:.14em;text-transform:uppercase;color:var(--cyan);margin-bottom:18px}
.proj-badge::before{content:'';width:5px;height:5px;background:var(--cyan);border-radius:50%;animation:pls 2s infinite}
.proj-name{font-family:'Cormorant Garamond',serif;font-size:2.6rem;font-weight:600;color:#faf5ff;line-height:1.1;margin-bottom:14px}
.proj-desc{font-size:.92rem;font-weight:300;color:var(--muted);line-height:1.78;margin-bottom:26px}
.proj-tech{display:flex;flex-wrap:wrap;gap:7px;margin-bottom:28px}
.tech-pill{background:rgba(124,58,237,.14);border:1px solid rgba(124,58,237,.28);border-radius:100px;padding:4px 13px;font-size:.76rem;color:var(--primary-l);font-weight:500}
.proj-links{display:flex;gap:12px}
.terminal{background:rgba(7,8,15,.7);border:1px solid rgba(124,58,237,.2);border-radius:12px;padding:28px;font-family:'DM Sans',monospace}
.t-bar{display:flex;gap:6px;margin-bottom:18px;align-items:center}
.t-dot{width:9px;height:9px;border-radius:50%}
.t-ttl{font-family:'Syne',sans-serif;font-size:.66rem;color:rgba(255,255,255,.28);margin-left:8px}
.t-line{margin-bottom:7px;font-size:.82rem;color:rgba(232,228,240,.55);line-height:1.5}
.t-line .kw{color:var(--primary-l)}.t-line .str{color:var(--cyan)}.t-line .cmt{color:rgba(255,255,255,.22)}
.proj-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:20px}
.proj-card{background:var(--surface);border:1px solid var(--border);border-radius:16px;padding:28px;backdrop-filter:blur(20px);transition:all .3s;position:relative;overflow:hidden}
.proj-card::after{content:'';position:absolute;inset:0;background:linear-gradient(135deg,rgba(124,58,237,.06) 0%,transparent 60%);opacity:0;transition:opacity .3s}
.proj-card:hover{transform:translateY(-5px);border-color:var(--border-h)}
.proj-card:hover::after{opacity:1}
.card-ico{width:46px;height:46px;background:rgba(124,58,237,.14);border-radius:12px;display:flex;align-items:center;justify-content:center;font-size:1.25rem;margin-bottom:18px}
.card-name{font-family:'Syne',sans-serif;font-size:1rem;font-weight:700;color:#faf5ff;margin-bottom:8px}
.card-desc{font-size:.86rem;color:var(--muted);line-height:1.7;margin-bottom:18px}
.card-link{font-family:'Syne',sans-serif;font-size:.74rem;font-weight:600;letter-spacing:.08em;color:var(--muted);text-decoration:none;display:inline-flex;align-items:center;gap:6px;transition:color .2s}
.card-link:hover{color:var(--primary-l)}

/* EXPERIENCE */
.exp-grid{display:grid;grid-template-columns:1fr 1fr;gap:72px}
.sub-label{font-family:'Syne',sans-serif;font-size:.7rem;font-weight:700;letter-spacing:.18em;text-transform:uppercase;color:var(--primary-l);margin-bottom:28px;display:flex;align-items:center;gap:12px}
.sub-label::before{content:'';width:20px;height:1px;background:var(--primary-l)}
.timeline{padding-left:24px;position:relative}
.timeline::before{content:'';position:absolute;left:0;top:6px;bottom:6px;width:1px;background:linear-gradient(to bottom,var(--primary),transparent)}
.tl-item{position:relative;margin-bottom:40px}
.tl-item::before{content:'';position:absolute;left:-28px;top:5px;width:8px;height:8px;background:var(--primary-l);border-radius:50%;box-shadow:0 0 0 4px rgba(167,139,250,.14)}
.tl-date{font-family:'Syne',sans-serif;font-size:.68rem;font-weight:700;letter-spacing:.12em;text-transform:uppercase;color:var(--cyan);margin-bottom:6px}
.tl-role{font-family:'Syne',sans-serif;font-size:.96rem;font-weight:700;color:#faf5ff;margin-bottom:3px}
.tl-co{font-size:.86rem;color:var(--primary-l);margin-bottom:8px}
.tl-desc{font-size:.86rem;color:var(--muted);line-height:1.7}
.certs{display:flex;flex-direction:column;gap:12px}
.cert-card{display:flex;align-items:center;gap:14px;background:var(--surface);border:1px solid var(--border);border-radius:12px;padding:18px;backdrop-filter:blur(20px);transition:all .3s}
.cert-card:hover{border-color:var(--border-h);transform:translateX(4px)}
.cert-ico{width:42px;height:42px;background:rgba(124,58,237,.14);border-radius:10px;display:flex;align-items:center;justify-content:center;font-size:1rem;color:var(--primary-l);flex-shrink:0}
.cert-name{font-family:'Syne',sans-serif;font-size:.86rem;font-weight:700;color:#faf5ff;margin-bottom:2px}
.cert-issuer{font-size:.76rem;color:var(--muted)}
.cert-yr{margin-left:auto;font-family:'Syne',sans-serif;font-size:.68rem;font-weight:700;letter-spacing:.1em;color:var(--cyan);white-space:nowrap}

/* CONTACT */
#contact{background:var(--bg2)}
.contact-inner{max-width:680px;margin:0 auto;text-align:center}
.contact-inner .sec-label{justify-content:center}
.contact-inner .sec-label::before{display:none}
.contact-inner .sec-title{margin-bottom:18px}
.contact-sub{font-size:1rem;color:var(--muted);font-weight:300;line-height:1.85;margin-bottom:44px}
.contact-links{display:flex;gap:14px;justify-content:center;flex-wrap:wrap}
.contact-link{display:inline-flex;align-items:center;gap:10px;background:var(--surface);border:1px solid var(--border);border-radius:12px;padding:15px 28px;color:var(--text);text-decoration:none;font-family:'Syne',sans-serif;font-size:.8rem;font-weight:700;letter-spacing:.06em;transition:all .3s;backdrop-filter:blur(20px)}
.contact-link:hover{border-color:var(--primary-l);color:var(--primary-l);transform:translateY(-3px)}

/* FOOTER */
footer{padding:36px 64px;border-top:1px solid rgba(124,58,237,.1);display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:12px}
.footer-logo{font-family:'Cormorant Garamond',serif;font-size:1.1rem;color:var(--primary-l)}
.footer-copy{font-size:.78rem;color:var(--muted)}

/* REVEAL */
.reveal{opacity:0;transform:translateY(36px);transition:opacity .75s ease,transform .75s ease}
.reveal.show{opacity:1;transform:translateY(0)}
.reveal-d1{transition-delay:.08s}.reveal-d2{transition-delay:.16s}.reveal-d3{transition-delay:.24s}.reveal-d4{transition-delay:.32s}.reveal-d5{transition-delay:.4s}.reveal-d6{transition-delay:.48s}

/* RESPONSIVE */
@media(max-width:960px){
  nav{padding:16px 24px}.nav-links{gap:18px}
  section{padding:80px 24px}
  #hero{padding:110px 24px 70px}
  .about-grid,.exp-grid,.feat-proj,.skills-grid{grid-template-columns:1fr}
  .proj-grid{grid-template-columns:1fr 1fr}
  .hero-socials,.scroll-hint{display:none}
  footer{padding:28px 24px;flex-direction:column;text-align:center}
}
@media(max-width:600px){
  .proj-grid{grid-template-columns:1fr}
  .stats-row{grid-template-columns:repeat(3,1fr)}
}
</style>
</head>
<body>

<div class="cursor" id="cursor"></div>
<div class="cursor-ring" id="cursorRing"></div>

<!-- NAV -->
<nav id="navbar">
  <div class="nav-logo">A. Kesarkar</div>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-grid"></div>
  <div class="orb o1"></div>
  <div class="orb o2"></div>
  <div class="orb o3"></div>
  <div class="hero-content">
    <div class="hero-tag">Open to Opportunities · Karnataka, India</div>
    <h1 class="hero-name">Akanksha<br/><em>Kesarkar</em></h1>
    <div class="hero-sub">Full Stack Developer &amp; AI Enthusiast</div>
    <p class="hero-desc">Crafting intelligent, data-driven web platforms with Python, FastAPI, React &amp; Machine Learning. B.E. CS Graduate · Infosys AI Certified.</p>
    <div class="hero-cta">
      <a href="#projects" class="btn-p"><i class="fas fa-rocket"></i> View Projects</a>
      <a href="https://linkedin.com/in/akanksha-kesarkar" target="_blank" class="btn-o"><i class="fab fa-linkedin"></i> LinkedIn</a>
      <a href="https://github.com/AkankshaKesarkar" target="_blank" class="btn-o"><i class="fab fa-github"></i> GitHub</a>
    </div>
  </div>
  <div class="hero-socials">
    <a href="https://github.com/AkankshaKesarkar" target="_blank" title="GitHub"><i class="fab fa-github"></i></a>
    <a href="https://linkedin.com/in/akanksha-kesarkar" target="_blank" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
  </div>
  <div class="scroll-hint">Scroll to explore</div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="about-grid">
    <div>
      <div class="sec-label reveal">Who I Am</div>
      <h2 class="sec-title reveal">Building with<br/><em>purpose</em></h2>
      <p class="about-p reveal">I'm a <strong>Computer Science graduate (B.E., 2024)</strong> from VSMK Institute of Technology, Belagavi — passionate about building AI-powered full-stack products that solve real-world problems elegantly.</p>
      <p class="about-p reveal">Currently developing the <strong>AI CSV Analyzer</strong> — a full-stack intelligence platform powered by FastAPI, React, and HuggingFace that transforms raw data into actionable insights instantly.</p>
      <p class="about-p reveal">Certified by <strong>Infosys Springboard</strong> in AI, Generative AI, NLP, Deep Learning, and Prompt Engineering (May 2026). Always building, always learning.</p>
      <div class="stats-row">
        <div class="stat-card reveal reveal-d1">
          <div class="stat-num">3</div>
          <div class="stat-lbl">Internships</div>
        </div>
        <div class="stat-card reveal reveal-d2">
          <div class="stat-num">7.6</div>
          <div class="stat-lbl">CGPA / 10</div>
        </div>
        <div class="stat-card reveal reveal-d3">
          <div class="stat-num">6+</div>
          <div class="stat-lbl">Certifications</div>
        </div>
      </div>
    </div>
    <div class="reveal">
      <div class="info-card">
        <div class="info-item">
          <div class="info-icon"><i class="fas fa-graduation-cap"></i></div>
          <div>
            <div class="info-lbl">Education</div>
            <div class="info-val">B.E. Computer Science, 2024<br/><span style="color:var(--muted);font-size:.84rem">VSMK Institute of Technology, Belagavi</span></div>
          </div>
        </div>
        <div class="info-item">
          <div class="info-icon"><i class="fas fa-map-marker-alt"></i></div>
          <div>
            <div class="info-lbl">Location</div>
            <div class="info-val">Karnataka, India 🇮🇳</div>
          </div>
        </div>
        <div class="info-item">
          <div class="info-icon"><i class="fas fa-hammer"></i></div>
          <div>
            <div class="info-lbl">Currently Building</div>
            <div class="info-val">AI CSV Analyzer — Full Stack Platform</div>
          </div>
        </div>
        <div class="info-item">
          <div class="info-icon"><i class="fas fa-search"></i></div>
          <div>
            <div class="info-lbl">Open To</div>
            <div class="info-val">Internships &amp; Full-time Roles<br/><span style="color:var(--muted);font-size:.84rem">Software Eng · Data · AI/ML · Analytics</span></div>
          </div>
        </div>
        <div class="info-item">
          <div class="info-icon"><i class="fas fa-star"></i></div>
          <div>
            <div class="info-lbl">Interests</div>
            <div class="info-val">AI/ML · Full Stack · Data Analytics · Open Source</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="sec-label reveal">Tech Stack</div>
  <h2 class="sec-title reveal">My <em>Arsenal</em></h2>
  <div class="skills-grid">
    <div class="sk-cat reveal reveal-d1">
      <div class="sk-cat-ttl"><i class="fas fa-code"></i> Languages</div>
      <div class="sk-tags">
        <span class="sk-tag">Python</span><span class="sk-tag">JavaScript</span><span class="sk-tag">Java</span><span class="sk-tag">SQL</span><span class="sk-tag">HTML5</span><span class="sk-tag">CSS3</span>
      </div>
    </div>
    <div class="sk-cat reveal reveal-d2">
      <div class="sk-cat-ttl"><i class="fas fa-layer-group"></i> Frontend</div>
      <div class="sk-tags">
        <span class="sk-tag">React</span><span class="sk-tag">Vite</span><span class="sk-tag">Tailwind CSS</span><span class="sk-tag">REST APIs</span>
      </div>
    </div>
    <div class="sk-cat reveal reveal-d3">
      <div class="sk-cat-ttl"><i class="fas fa-server"></i> Backend</div>
      <div class="sk-tags">
        <span class="sk-tag">FastAPI</span><span class="sk-tag">Flask</span><span class="sk-tag">REST APIs</span><span class="sk-tag">PostgreSQL</span>
      </div>
    </div>
    <div class="sk-cat reveal reveal-d4">
      <div class="sk-cat-ttl"><i class="fas fa-brain"></i> AI / Data</div>
      <div class="sk-tags">
        <span class="sk-tag">Pandas</span><span class="sk-tag">NumPy</span><span class="sk-tag">scikit-learn</span><span class="sk-tag">HuggingFace</span><span class="sk-tag">NLP</span><span class="sk-tag">Power BI</span>
      </div>
    </div>
    <div class="sk-cat reveal reveal-d5">
      <div class="sk-cat-ttl"><i class="fas fa-tools"></i> DevOps &amp; Tools</div>
      <div class="sk-tags">
        <span class="sk-tag">Docker</span><span class="sk-tag">Git</span><span class="sk-tag">GitHub</span><span class="sk-tag">CI/CD</span><span class="sk-tag">Vercel</span>
      </div>
    </div>
    <div class="sk-cat reveal reveal-d6">
      <div class="sk-cat-ttl"><i class="fas fa-robot"></i> AI Specialization</div>
      <div class="sk-tags">
        <span class="sk-tag">Generative AI</span><span class="sk-tag">Prompt Engineering</span><span class="sk-tag">Deep Learning</span><span class="sk-tag">LLMs</span>
      </div>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects">
  <div class="sec-label reveal">What I've Built</div>
  <h2 class="sec-title reveal">Featured <em>Projects</em></h2>

  <div class="feat-proj reveal">
    <div>
      <div class="proj-badge">Currently Building</div>
      <h3 class="proj-name">AI CSV Analyzer</h3>
      <p class="proj-desc">Upload any CSV or fetch live market data — get instant AI-powered insights, trend detection, and anomaly analysis. A production-grade full-stack intelligence platform.</p>
      <div class="proj-tech">
        <span class="tech-pill">Python</span><span class="tech-pill">FastAPI</span><span class="tech-pill">React</span><span class="tech-pill">HuggingFace</span><span class="tech-pill">Docker</span><span class="tech-pill">Pandas</span>
      </div>
      <div class="proj-links">
        <a href="https://ai-csv-analyzer-beta.vercel.app" target="_blank" class="btn-p" style="font-size:.78rem;padding:11px 22px"><i class="fas fa-external-link-alt"></i> Live Demo</a>
        <a href="https://github.com/AkankshaKesarkar/ai-csv-analyzer" target="_blank" class="btn-o" style="font-size:.78rem;padding:11px 22px"><i class="fab fa-github"></i> Source Code</a>
      </div>
    </div>
    <div class="terminal">
      <div class="t-bar">
        <div class="t-dot" style="background:#ff5f57"></div>
        <div class="t-dot" style="background:#febc2e"></div>
        <div class="t-dot" style="background:#28c840"></div>
        <span class="t-ttl">ai_csv_analyzer.py</span>
      </div>
      <div class="t-line"><span class="cmt"># Upload CSV → Instant AI Insights</span></div>
      <div class="t-line"><span class="kw">from</span> analyzer <span class="kw">import</span> AIInsights</div>
      <div class="t-line">&nbsp;</div>
      <div class="t-line">df = pd.read_csv(<span class="str">"sales_data.csv"</span>)</div>
      <div class="t-line">ai = AIInsights(model=<span class="str">"hf-llm"</span>)</div>
      <div class="t-line">result = ai.analyze(df)</div>
      <div class="t-line">&nbsp;</div>
      <div class="t-line"><span class="cmt"># ✓ Trend: Q3 revenue ↑ 24.3%</span></div>
      <div class="t-line"><span class="cmt"># ✓ Anomaly in row 142 detected</span></div>
      <div class="t-line"><span class="cmt"># ✓ Forecast: +12% next quarter</span></div>
    </div>
  </div>

  <div class="proj-grid">
    <div class="proj-card reveal reveal-d1">
      <div class="card-ico">💰</div>
      <div class="card-name">Expense Tracker</div>
      <div class="proj-tech" style="margin-bottom:12px"><span class="tech-pill">React</span><span class="tech-pill">JavaScript</span></div>
      <p class="card-desc">Intuitive expense tracking app with category breakdowns, spending trends, and real-time budget monitoring.</p>
      <a href="https://github.com/AkankshaKesarkar/Expense-Tracker" target="_blank" class="card-link"><i class="fab fa-github"></i> View on GitHub</a>
    </div>
    <div class="proj-card reveal reveal-d2">
      <div class="card-ico">✅</div>
      <div class="card-name">To-Do App</div>
      <div class="proj-tech" style="margin-bottom:12px"><span class="tech-pill">React</span><span class="tech-pill">JavaScript</span></div>
      <p class="card-desc">Responsive productivity app with task management, priority labels, and smooth state management.</p>
      <a href="https://github.com/AkankshaKesarkar/To-Do-App" target="_blank" class="card-link"><i class="fab fa-github"></i> View on GitHub</a>
    </div>
    <div class="proj-card reveal reveal-d3">
      <div class="card-ico">🍽️</div>
      <div class="card-name">Recipe App</div>
      <div class="proj-tech" style="margin-bottom:12px"><span class="tech-pill">React</span><span class="tech-pill">Vite</span></div>
      <p class="card-desc">Searchable recipe discovery app with category filters, ingredient lists, and step-by-step cooking guides.</p>
      <a href="https://github.com/AkankshaKesarkar/Recipe-App" target="_blank" class="card-link"><i class="fab fa-github"></i> View on GitHub</a>
    </div>
  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="sec-label reveal">Journey</div>
  <h2 class="sec-title reveal">Experience &amp;<br/><em>Certifications</em></h2>
  <div class="exp-grid">
    <div class="reveal">
      <div class="sub-label">Work Experience</div>
      <div class="timeline">
        <div class="tl-item">
          <div class="tl-date">Jun 2024 – May 2025</div>
          <div class="tl-role">Full Stack Developer Intern</div>
          <div class="tl-co"><i class="fas fa-building" style="font-size:.78rem;margin-right:5px"></i>Tap Academy Pvt. Ltd. · Bangalore</div>
          <p class="tl-desc">Built and maintained full-stack web applications using React, FastAPI, and Python. Developed RESTful APIs, integrated data pipelines, and collaborated on production deployments.</p>
        </div>
        <div class="tl-item">
          <div class="tl-date">Sept 2023 – Feb 2024</div>
          <div class="tl-role">Software Programming Intern</div>
          <div class="tl-co"><i class="fas fa-building" style="font-size:.78rem;margin-right:5px"></i>Seventh Sense · Bangalore</div>
          <p class="tl-desc">Contributed to backend development and software engineering projects, working with Python, database systems, and system design.</p>
        </div>
        <div class="tl-item">
          <div class="tl-date">Aug 2023 – Oct 2023</div>
          <div class="tl-role">Data Analytics Intern</div>
          <div class="tl-co"><i class="fas fa-building" style="font-size:.78rem;margin-right:5px"></i>Zeal Code Lab · Belagavi</div>
          <p class="tl-desc">Performed data analysis using Pandas and NumPy. Created interactive Power BI dashboards for business intelligence and reporting.</p>
        </div>
      </div>
    </div>
    <div class="reveal">
      <div class="sub-label">Certifications · Infosys Springboard (2026)</div>
      <div class="certs">
        <div class="cert-card">
          <div class="cert-ico"><i class="fas fa-robot"></i></div>
          <div><div class="cert-name">Artificial Intelligence</div><div class="cert-issuer">Infosys Springboard</div></div>
          <div class="cert-yr">2026</div>
        </div>
        <div class="cert-card">
          <div class="cert-ico"><i class="fas fa-magic"></i></div>
          <div><div class="cert-name">Generative AI</div><div class="cert-issuer">Infosys Springboard</div></div>
          <div class="cert-yr">2026</div>
        </div>
        <div class="cert-card">
          <div class="cert-ico"><i class="fas fa-comments"></i></div>
          <div><div class="cert-name">Prompt Engineering</div><div class="cert-issuer">Infosys Springboard</div></div>
          <div class="cert-yr">2026</div>
        </div>
        <div class="cert-card">
          <div class="cert-ico"><i class="fas fa-language"></i></div>
          <div><div class="cert-name">Natural Language Processing</div><div class="cert-issuer">Infosys Springboard</div></div>
          <div class="cert-yr">2026</div>
        </div>
        <div class="cert-card">
          <div class="cert-ico"><i class="fas fa-brain"></i></div>
          <div><div class="cert-name">Deep Learning</div><div class="cert-issuer">Infosys Springboard</div></div>
          <div class="cert-yr">2026</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="contact-inner reveal">
    <div class="sec-label">Get In Touch</div>
    <h2 class="sec-title">Let's Build<br/><em>Something</em></h2>
    <p class="contact-sub">Open to internships, full-time roles, open source collaboration, and AI/data projects. I'd love to connect and create something impactful together.</p>
    <div class="contact-links">
      <a href="https://linkedin.com/in/akanksha-kesarkar" target="_blank" class="contact-link">
        <i class="fab fa-linkedin" style="color:#0077b5"></i> LinkedIn
      </a>
      <a href="https://github.com/AkankshaKesarkar" target="_blank" class="contact-link">
        <i class="fab fa-github"></i> GitHub
      </a>
      <a href="mailto:akanksha.kesarkar@example.com" class="contact-link">
        <i class="fas fa-envelope" style="color:var(--primary-l)"></i> Email Me
      </a>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo">Akanksha Kesarkar</div>
  <div class="footer-copy">✦ Never Give Up — Accept the Challenge — Be Confident!</div>
  <div class="footer-copy">© 2025 · Made with ❤️ in Karnataka</div>
</footer>

<script>
const cursor = document.getElementById('cursor');
const ring = document.getElementById('cursorRing');
let mx=0,my=0,rx=0,ry=0;
document.addEventListener('mousemove',e=>{
  mx=e.clientX;my=e.clientY;
  cursor.style.left=mx+'px';cursor.style.top=my+'px';
});
(function animR(){
  rx+=(mx-rx)*.12;ry+=(my-ry)*.12;
  ring.style.left=rx+'px';ring.style.top=ry+'px';
  requestAnimationFrame(animR);
})();
document.querySelectorAll('a,button,.proj-card,.sk-cat,.cert-card').forEach(el=>{
  el.addEventListener('mouseenter',()=>{
    cursor.style.transform='translate(-50%,-50%) scale(2.2)';
    cursor.style.background='var(--cyan)';
    ring.style.width='58px';ring.style.height='58px';
  });
  el.addEventListener('mouseleave',()=>{
    cursor.style.transform='translate(-50%,-50%) scale(1)';
    cursor.style.background='var(--primary-l)';
    ring.style.width='34px';ring.style.height='34px';
  });
});

// Scroll reveal
const reveals=document.querySelectorAll('.reveal');
const obs=new IntersectionObserver(entries=>{
  entries.forEach(e=>{if(e.isIntersecting){e.target.classList.add('show');obs.unobserve(e.target);}});
},{threshold:0.12});
reveals.forEach(el=>obs.observe(el));

// Nav scroll
window.addEventListener('scroll',()=>{
  document.getElementById('navbar').style.borderBottomColor=
    window.scrollY>60?'rgba(124,58,237,.25)':'rgba(124,58,237,.1)';
});
</script>
</body>
</html>
PORTFOLIO_EOF
echo "File written: $(wc -l < /mnt/user-data/outputs/portfolio.html) lines"
