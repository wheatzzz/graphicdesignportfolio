<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Zimai Gao — Design Portfolio</title>
<meta name="description" content="Zimai Gao — Graphic & UI/UX Design Portfolio (2024–2026)">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Archivo+Black&family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#0a0a0a;
    --paper:#fdfdfb;
    --accent:#e8532c;
    --accent2:#1c2b57;
    --grey:#8a8a86;
    --line:#e3e2dc;
    --max:1040px;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--paper);
    color:var(--ink);
    font-family:'Inter',system-ui,sans-serif;
    -webkit-font-smoothing:antialiased;
  }
  h1,h2,h3,.display{
    font-family:'Archivo Black','Inter',sans-serif;
    letter-spacing:-0.01em;
    text-transform:uppercase;
    margin:0;
  }

  /* ---- Nav ---- */
  header.nav{
    position:sticky;
    top:0;
    z-index:50;
    background:rgba(253,253,251,0.9);
    backdrop-filter:blur(8px);
    border-bottom:1px solid var(--line);
  }
  .nav-inner{
    max-width:var(--max);
    margin:0 auto;
    padding:16px 24px;
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap:16px;
  }
  .nav-name{
    font-family:'Archivo Black',sans-serif;
    font-size:15px;
    text-transform:uppercase;
    letter-spacing:0.02em;
  }
  .nav-links{
    display:flex;
    gap:22px;
    list-style:none;
    padding:0;
    margin:0;
    flex-wrap:wrap;
  }
  .nav-links a{
    color:var(--ink);
    text-decoration:none;
    font-size:13px;
    font-weight:600;
    text-transform:uppercase;
    letter-spacing:0.04em;
    padding-bottom:2px;
    border-bottom:2px solid transparent;
    transition:border-color .15s ease, color .15s ease;
  }
  .nav-links a:hover{
    border-color:var(--accent);
    color:var(--accent);
  }

  /* ---- Hero ---- */
  .hero{
    max-width:var(--max);
    margin:0 auto;
    padding:72px 24px 48px;
  }
  .hero-eyebrow{
    color:var(--accent);
    font-weight:700;
    font-size:13px;
    letter-spacing:0.12em;
    text-transform:uppercase;
    margin-bottom:14px;
  }
  .hero h1{
    font-size:clamp(40px,7vw,84px);
    line-height:0.94;
  }
  .hero h1 span{color:var(--accent);}
  .hero-sub{
    max-width:620px;
    margin-top:24px;
    font-size:17px;
    line-height:1.6;
    color:#333;
  }
  .hero-meta{
    margin-top:32px;
    display:flex;
    flex-wrap:wrap;
    gap:12px 28px;
    font-size:13px;
    color:var(--grey);
    text-transform:uppercase;
    letter-spacing:0.03em;
    font-weight:600;
  }
  .hero-meta a{color:var(--grey); text-decoration:none;}
  .hero-meta a:hover{color:var(--accent);}

  .hero-cover{
    max-width:var(--max);
    margin:0 auto;
    padding:0 24px 64px;
  }
  .hero-cover img{
    width:100%;
    display:block;
    border-radius:2px;
    border:1px solid var(--line);
  }

  /* ---- About ---- */
  .about{
    max-width:var(--max);
    margin:0 auto;
    padding:56px 24px;
    border-top:1px solid var(--line);
    display:grid;
    grid-template-columns:220px 1fr;
    gap:40px;
  }
  .about h2{font-size:14px; letter-spacing:0.1em; color:var(--grey);}
  .about p{
    font-size:18px;
    line-height:1.7;
    margin:0 0 18px;
  }
  .about .tags{
    display:flex;
    flex-wrap:wrap;
    gap:8px;
    margin-top:20px;
  }
  .about .tags span{
    border:1px solid var(--line);
    padding:6px 12px;
    font-size:12px;
    text-transform:uppercase;
    letter-spacing:0.04em;
    font-weight:600;
    border-radius:20px;
  }
  .roles{
    margin-top:26px;
    display:grid;
    gap:10px;
  }
  .roles div{
    display:flex;
    justify-content:space-between;
    gap:12px;
    font-size:14px;
    border-bottom:1px dashed var(--line);
    padding-bottom:8px;
  }
  .roles .role-title{font-weight:700;}
  .roles .role-date{color:var(--grey); white-space:nowrap;}

  @media (max-width:700px){
    .about{grid-template-columns:1fr;}
  }

  /* ---- Sections ---- */
  section.work{
    padding:70px 0 20px;
    border-top:1px solid var(--line);
  }
  .work-head{
    max-width:var(--max);
    margin:0 auto;
    padding:0 24px 36px;
  }
  .work-index{
    font-size:13px;
    color:var(--accent);
    font-weight:700;
    letter-spacing:0.08em;
    margin-bottom:10px;
  }
  .work-head h2{
    font-size:clamp(30px,5vw,52px);
  }
  .work-head p{
    max-width:640px;
    margin-top:16px;
    font-size:16px;
    line-height:1.65;
    color:#333;
  }
  .plate{
    max-width:var(--max);
    margin:0 auto 28px;
    padding:0 24px;
  }
  .plate img{
    width:100%;
    display:block;
    border:1px solid var(--line);
    border-radius:2px;
  }
  .plate-full{
    margin:0 0 28px;
  }
  .plate-full img{
    border-left:none;
    border-right:none;
    border-radius:0;
  }

  /* ---- Footer ---- */
  footer{
    background:var(--accent2);
    color:#fff;
    margin-top:60px;
  }
  .footer-inner{
    max-width:var(--max);
    margin:0 auto;
    padding:80px 24px 56px;
    text-align:center;
  }
  footer h2{
    font-size:clamp(36px,7vw,64px);
    color:#fff;
  }
  footer p{
    margin-top:16px;
    color:#c9d1e6;
    font-size:15px;
  }
  .contact-card{
    display:inline-block;
    text-align:left;
    background:#fff;
    color:var(--ink);
    border-radius:4px;
    padding:22px 28px;
    margin-top:32px;
  }
  .contact-card div{
    font-size:15px;
    padding:6px 0;
    border-bottom:1px solid var(--line);
  }
  .contact-card div:last-child{border-bottom:none;}
  .contact-card a{color:var(--ink); text-decoration:none;}
  .contact-card a:hover{color:var(--accent);}
  .footer-note{
    margin-top:40px;
    font-size:12px;
    letter-spacing:0.06em;
    text-transform:uppercase;
    color:#8f9bc2;
  }

  .back-top{
    display:block;
    text-align:center;
    padding:26px 0;
    font-size:12px;
    letter-spacing:0.08em;
    text-transform:uppercase;
    color:var(--grey);
    text-decoration:none;
    font-weight:600;
  }
  .back-top:hover{color:var(--accent);}
</style>
</head>
<body>

<header class="nav">
  <div class="nav-inner">
    <div class="nav-name">Zimai Gao</div>
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#rebranding">(Re)Branding</a></li>
      <li><a href="#cover">Cover Design</a></li>
      <li><a href="#typography">Typography</a></li>
      <li><a href="#hobby">Hobby Projects</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </div>
</header>

<div class="hero">
  <div class="hero-eyebrow">Design Portfolio · 2024–2026</div>
  <h1>Zimai Gao<br><span>Graphic &amp; UI/UX Design</span></h1>
  <p class="hero-sub">A third-year Graphic Design and UI/UX Design student at the University of Melbourne, translating design concepts into real-world products — with a focus on branding, typography, and visual communication for the beauty, food, and music industries.</p>
  <div class="hero-meta">
    <span>Based in Melbourne</span>
    <a href="mailto:wheatzzz515@gmail.com">wheatzzz515@gmail.com</a>
    <span>0421 298 689</span>
    <span>EN · 中文 (普通话)</span>
  </div>
</div>

<div class="hero-cover">
  <img src="images/page-01.jpg" alt="Zimai Gao design portfolio cover">
</div>

<div class="about" id="about">
  <h2>About</h2>
  <div>
    <p>I am a third-year student studying Graphic Design and UI/UX Design at the University of Melbourne. As a soon-to-be graduate, I am seeking work experience beyond the scope of my university coursework, with the goal of translating design concepts into real-world products.</p>
    <p>My interests include branding, typography, product design, and visual communication, with a particular focus on the beauty, food, and music industries. I am proficient in the Affinity suite and Canva, with developing skills in Adobe Creative Suite and Figma.</p>
    <div class="tags">
      <span>Branding</span>
      <span>Typography</span>
      <span>Product Design</span>
      <span>Visual Communication</span>
      <span>Affinity Suite</span>
      <span>Canva</span>
      <span>Adobe Creative Suite</span>
      <span>Figma</span>
    </div>
    <div class="roles">
      <div><span class="role-title">Design Officer — CISSA (Computing and Information Systems Students Association)</span><span class="role-date">Nov 2025 – Present</span></div>
      <div><span class="role-title">Secretary — Unimelb Kpop Club</span><span class="role-date">Nov 2025 – Present</span></div>
      <div><span class="role-title">Events Officer — Unimelb Kpop Club</span><span class="role-date">Feb 2025 – Nov 2025</span></div>
    </div>
  </div>
</div>

<!-- SECTION 1: (Re)Branding -->
<section class="work" id="rebranding">
  <div class="work-head">
    <div class="work-index">01 / 04</div>
    <h2>(Re)Branding</h2>
    <p>This section explores rebranding through the lens of heritage and cultural memory. The project is inspired by Sony's classic Walkman, translating brand heritage into a contemporary campaign-driven visual identity.</p>
  </div>
  <div class="plate"><img src="images/page-04.jpg" alt="(Re)Branding — Colour Pinpoint, 2025"></div>
  <div class="plate"><img src="images/page-05.jpg" alt="(Re)Branding — Banner Design, 2025"></div>
  <div class="plate"><img src="images/page-06.jpg" alt="(Re)Branding — packaging mockup, 2025"></div>
  <div class="plate"><img src="images/page-07.jpg" alt="(Re)Branding — Poster Design 1, 2025"></div>
  <div class="plate"><img src="images/page-08.jpg" alt="(Re)Branding — Poster Design 1 continued, 2025"></div>
  <div class="plate"><img src="images/page-09.jpg" alt="(Re)Branding — outdoor poster mockup, 2025"></div>
</section>

<!-- SECTION 2: Cover Design -->
<section class="work" id="cover">
  <div class="work-head">
    <div class="work-index">02 / 04</div>
    <h2>Cover Design</h2>
    <p>This collection presents cover designs created in reflection of existing media, including painting and music. The works reinterpret emotional tone and narrative through form, typography, and material, showcased through a book cover for Picasso's <em>The Weeping Woman</em> and a vinyl design for Dept's <em>Rainy Day</em>.</p>
  </div>
  <div class="plate"><img src="images/page-11.jpg" alt="Cover Design — Vinyl Cover, 2024"></div>
  <div class="plate"><img src="images/page-12.jpg" alt="Cover Design — vinyl front mockup, 2024"></div>
  <div class="plate"><img src="images/page-13.jpg" alt="Cover Design — vinyl back mockup, 2024"></div>
  <div class="plate"><img src="images/page-14.jpg" alt="Cover Design — vinyl Side A / Side B, 2024"></div>
  <div class="plate"><img src="images/page-15.jpg" alt="Cover Design — Promotional Poster, 2024"></div>
  <div class="plate"><img src="images/page-16.jpg" alt="Cover Design — Book Cover, 2025"></div>
  <div class="plate"><img src="images/page-17.jpg" alt="Cover Design — book cover mockup, 2025"></div>
</section>

<!-- SECTION 3: Typography -->
<section class="work" id="typography">
  <div class="work-head">
    <div class="work-index">03 / 04</div>
    <h2>Typography</h2>
    <p>This typography project explores modular type design through the use of simple geometric forms. By limiting the system to a small set of shapes, the work focuses on structure, consistency, and visual logic to construct a complete character set, including the alphabet and numerals.</p>
  </div>
  <div class="plate"><img src="images/page-19.jpg" alt="Typography — UNITY, 2024"></div>
  <div class="plate"><img src="images/page-20.jpg" alt="Typography — UNITY applied mockup, 2024"></div>
  <div class="plate"><img src="images/page-21.jpg" alt="Typography — Extension, 2024"></div>
  <div class="plate"><img src="images/page-22.jpg" alt="Typography — Extension applied mockup, 2024"></div>
</section>

<!-- SECTION 4: Hobby Projects -->
<section class="work" id="hobby">
  <div class="work-head">
    <div class="work-index">04 / 04</div>
    <h2>Hobby Projects</h2>
    <p>This section presents passion projects developed through graphic explorations of K-pop idols. The works function as a creative playground to practice design skills, test visual styles, and expand artistic expression and communication. A more detailed collection can be found on Instagram: <strong>@m2x_udio</strong>.</p>
  </div>
  <div class="plate"><img src="images/page-24.jpg" alt="Passion Projects — Postcard Design, 2026"></div>
  <div class="plate"><img src="images/page-25.jpg" alt="Passion Projects — Wallpaper Design, 2026"></div>
</section>

<a href="#top" class="back-top">↑ Back to top</a>

<footer id="contact">
  <div class="footer-inner">
    <h2>Thank you!</h2>
    <p>The design journey does not end here…</p>
    <div class="contact-card">
      <div><strong>Zimai Gao</strong></div>
      <div><a href="mailto:wheatzzz515@gmail.com">wheatzzz515@gmail.com</a></div>
      <div>0421 298 689</div>
      <div>Based in Melbourne</div>
    </div>
    <div class="footer-note">Portfolio · 2024 – 2026</div>
  </div>
</footer>

</body>
</html>
