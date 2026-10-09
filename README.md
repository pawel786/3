<!DOCTYPE html>
<html lang="pl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>The Body Katowice — Salon zabiegów na ciało</title>
<meta name="description" content="The Body Katowice — salon zabiegów na ciało i twarz przy Barcelońskiej. Terapia blizn, drenaż limfatyczny, modelowanie sylwetki, masaż misami tybetańskimi i pełna oferta zabiegów.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,wght@0,300;0,400;0,500;0,600;1,400;1,500&family=Manrope:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --stone:#E4DCCD;
    --stone-2:#D7CBB4;
    --ink:#201A15;
    --ink-2:#2B241C;
    --bronze:#9C6B45;
    --bronze-dark:#7C5334;
    --green:#3F4A3B;
    --gold:#BFA05E;
    --cream:#F4EFE5;
    --line: rgba(32,26,21,0.14);
    --line-light: rgba(244,239,229,0.22);
    --max: 1180px;
    --serif: 'Fraunces', serif;
    --sans: 'Manrope', sans-serif;
  }

  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  html,body{max-width:100%;overflow-x:hidden;}
  body{
    margin:0;
    background:var(--stone);
    color:var(--ink);
    font-family:var(--sans);
    font-size:16px;
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
  }
  img,svg{display:block;max-width:100%;}
  a{color:inherit;text-decoration:none;}
  ul{margin:0;padding:0;list-style:none;}
  h1,h2,h3,h4{font-family:var(--serif);font-weight:500;margin:0;letter-spacing:-0.01em;}
  p{margin:0;}
  .wrap{max-width:var(--max);margin:0 auto;padding:0 20px;}
  section{position:relative;}

  @media (prefers-reduced-motion: reduce){
    *{animation-duration:0.001ms !important; animation-iteration-count:1 !important; transition-duration:0.001ms !important; scroll-behavior:auto !important;}
  }

  /* ---------- Buttons ---------- */
  .btn{
    display:inline-flex;
    align-items:center;
    gap:10px;
    padding:14px 24px;
    font-family:var(--sans);
    font-size:14.5px;
    font-weight:600;
    border-radius:2px;
    border:1px solid transparent;
    cursor:pointer;
    transition:background .25s ease, color .25s ease, border-color .25s ease;
    white-space:nowrap;
  }
  .btn-primary{background:var(--ink);color:var(--cream);}
  .btn-primary:hover{background:var(--bronze-dark);}
  .btn-ghost{background:transparent;border-color:var(--ink);color:var(--ink);}
  .btn-ghost:hover{background:var(--ink);color:var(--cream);}
  .btn-ghost-light{background:transparent;border-color:rgba(244,239,229,0.5);color:var(--cream);}
  .btn-ghost-light:hover{background:var(--cream);color:var(--ink);border-color:var(--cream);}

  /* ---------- Header ---------- */
  header{
    position:fixed;top:0;left:0;right:0;z-index:100;
    padding:20px 0;
    transition:padding .3s ease, background .3s ease, box-shadow .3s ease;
  }
  header.scrolled{
    padding:13px 0;
    background:rgba(228,220,205,0.94);
    backdrop-filter:blur(10px);
    box-shadow:0 1px 0 var(--line);
  }
  header .wrap{display:flex;align-items:center;justify-content:space-between;gap:18px;}
  .logo{display:flex;flex-direction:column;line-height:1;}
  .logo .mark{font-family:var(--serif);font-size:21px;font-weight:500;letter-spacing:0.01em;}
  .logo .sub{font-size:10px;letter-spacing:0.22em;font-weight:600;color:var(--bronze-dark);margin-top:4px;}
  nav.primary-nav{display:flex;align-items:center;gap:26px;}
  nav.primary-nav a{font-size:14px;font-weight:500;position:relative;padding:4px 0;}
  nav.primary-nav a::after{content:"";position:absolute;left:0;right:100%;bottom:0;height:1px;background:var(--ink);transition:right .3s ease;}
  nav.primary-nav a:hover::after{right:0;}
  .header-actions{display:flex;align-items:center;gap:12px;}
  .call-btn{
    display:flex;align-items:center;justify-content:center;
    width:38px;height:38px;border:1px solid var(--ink);border-radius:50%;
    flex-shrink:0;transition:background .25s ease, color .25s ease;
  }
  .call-btn:hover{background:var(--ink);color:var(--cream);}
  .burger{display:none;flex-direction:column;gap:5px;background:none;border:none;cursor:pointer;padding:6px;flex-shrink:0;}
  .burger span{width:22px;height:1.5px;background:var(--ink);display:block;}

  /* ---------- Mobile nav ---------- */
  .mobile-nav{
    position:fixed;inset:0;background:var(--ink);color:var(--cream);z-index:200;
    display:flex;flex-direction:column;justify-content:center;padding:36px 30px;
    transform:translateY(-100%);transition:transform .4s ease;
    overflow-y:auto;
  }
  .mobile-nav.open{transform:translateY(0);}
  .mobile-nav a{font-family:var(--serif);font-size:clamp(24px,7vw,32px);padding:12px 0;border-bottom:1px solid var(--line-light);display:block;}
  .mobile-nav .call-line{
    margin-top:24px;font-family:var(--sans);font-size:16px;font-weight:600;
    display:flex;align-items:center;gap:10px;color:var(--gold);border:none;
  }
  .mobile-nav .close-btn{position:absolute;top:22px;right:22px;background:none;border:none;color:var(--cream);font-size:28px;cursor:pointer;line-height:1;}

  /* ---------- Hero ---------- */
  .hero{padding:150px 0 90px;overflow:hidden;}
  .hero .wrap{display:grid;grid-template-columns:1fr 1fr;gap:56px;align-items:center;}
  .hero-eyebrow{font-size:13.5px;color:var(--bronze-dark);font-weight:600;margin-bottom:20px;display:flex;align-items:center;gap:10px;flex-wrap:wrap;}
  .hero-eyebrow .dot{width:6px;height:6px;border-radius:50%;background:var(--bronze);flex-shrink:0;}
  .hero h1{font-size:clamp(36px,6vw,70px);line-height:1.05;font-weight:400;}
  .hero h1 em{font-style:italic;font-weight:400;color:var(--bronze-dark);}
  .hero-sub{margin-top:24px;max-width:480px;font-size:17.5px;color:var(--ink-2);opacity:0.85;}
  .hero-cta{margin-top:36px;display:flex;gap:14px;flex-wrap:wrap;}
  .hero-cta .call-link{display:inline-flex;align-items:center;gap:8px;font-size:14.5px;font-weight:600;padding:14px 4px;}
  .hero-cta .call-link svg{flex-shrink:0;}
  .hero-meta{margin-top:52px;display:flex;gap:32px;flex-wrap:wrap;}
  .hero-meta .stat{display:flex;flex-direction:column;gap:4px;}
  .hero-meta .stat .num{font-family:var(--serif);font-size:25px;}
  .hero-meta .stat .label{font-size:12px;color:var(--ink-2);opacity:0.7;}
  .hero-art{position:relative;min-width:0;}
  .hero-photo{position:relative;}
  .hero-photo::before{
    content:"";position:absolute;top:16px;left:16px;right:-16px;bottom:-16px;
    border:1px solid var(--gold);z-index:0;
  }
  .hero-photo img{
    position:relative;z-index:1;width:100%;height:auto;aspect-ratio:3/2;
    object-fit:cover;border-radius:2px;background:var(--ink);
  }

  .fade-up{opacity:0;transform:translateY(16px);animation:fadeUp .8s ease forwards;}
  @keyframes fadeUp{to{opacity:1;transform:translateY(0);}}

  /* ---------- Section headings ---------- */
  .section-head{display:flex;justify-content:space-between;align-items:flex-end;gap:26px;margin-bottom:40px;flex-wrap:wrap;}
  .section-head h2{font-size:clamp(28px,4vw,44px);font-weight:400;max-width:560px;}
  .section-head p{max-width:340px;font-size:15px;opacity:0.75;}
  .kicker{font-size:12.5px;font-weight:700;color:var(--bronze-dark);margin-bottom:12px;display:block;}

  /* ---------- About ---------- */
  .about{padding:100px 0;border-top:1px solid var(--line);}
  .about-grid{display:grid;grid-template-columns:0.9fr 1.1fr;gap:56px;align-items:start;}
  .about-copy p{font-size:16.5px;margin-bottom:18px;color:var(--ink-2);}
  .about-copy p.lede{font-family:var(--serif);font-size:24px;line-height:1.4;font-weight:400;color:var(--ink);}
  .zones{display:flex;flex-direction:column;}
  .zone{padding:30px 0;border-top:1px solid var(--line);display:grid;grid-template-columns:64px 1fr;gap:18px;}
  .zone:last-child{border-bottom:1px solid var(--line);}
  .zone .zone-tag{font-family:var(--serif);font-style:italic;font-size:18px;color:var(--bronze-dark);}
  .zone h3{font-size:19px;margin-bottom:8px;font-weight:500;}
  .zone p{font-size:14.5px;color:var(--ink-2);}
  @media(max-width:640px){.zone{grid-template-columns:1fr;gap:6px;}}

  /* ---------- Treatments ---------- */
  .treatments{padding:100px 0;background:var(--ink);color:var(--cream);}
  .treatments .kicker{color:var(--gold);}
  .treatments .section-head p{color:var(--cream);opacity:0.65;}

  .treat-tabs{
    display:flex;gap:8px;overflow-x:auto;padding-bottom:6px;margin-bottom:8px;
    scrollbar-width:thin;
  }
  .treat-tabs::-webkit-scrollbar{height:4px;}
  .treat-tabs::-webkit-scrollbar-thumb{background:var(--bronze);border-radius:4px;}
  .tab-btn{
    flex-shrink:0;
    background:transparent;
    border:1px solid var(--line-light);
    color:var(--cream);
    opacity:0.6;
    padding:10px 18px;
    font-family:var(--sans);
    font-size:13.5px;
    font-weight:600;
    border-radius:20px;
    cursor:pointer;
    transition:all .25s ease;
    white-space:nowrap;
  }
  .tab-btn:hover{opacity:0.85;}
  .tab-btn.active{background:var(--gold);border-color:var(--gold);color:var(--ink);opacity:1;}

  .treat-panel{display:none;border-top:1px solid var(--line-light);}
  .treat-panel.active{display:block;}

  .treat-row{display:grid;grid-template-columns:32px 1.3fr 1.3fr 110px;gap:18px;align-items:center;padding:22px 0;border-bottom:1px solid var(--line-light);transition:padding-left .3s ease;}
  .treat-row:hover{padding-left:12px;}
  .treat-row .idx{font-size:12.5px;color:var(--gold);font-weight:600;}
  .treat-row h3{font-size:19px;font-weight:400;}
  .treat-row h3 .promo{
    display:inline-block;margin-left:10px;font-family:var(--sans);font-size:10.5px;font-weight:700;
    letter-spacing:0.04em;text-transform:uppercase;color:var(--ink);background:var(--gold);
    padding:2px 8px;border-radius:10px;vertical-align:middle;
  }
  .treat-row .desc{font-size:13.5px;opacity:0.65;}
  .treat-row .price{font-size:14px;letter-spacing:0.01em;color:var(--gold);justify-self:end;text-align:right;font-weight:600;white-space:nowrap;}
  .treat-more{
    margin-top:28px;display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:16px;
    padding-top:26px;
  }
  .treat-more p{font-size:14px;opacity:0.65;max-width:420px;}
  @media(max-width:780px){
    .treat-row{grid-template-columns:22px 1fr;grid-template-areas:"i h" ". d" ". p";row-gap:6px;padding:18px 0;}
    .treat-row .idx{grid-area:i;}
    .treat-row h3{grid-area:h;font-size:17px;}
    .treat-row .desc{grid-area:d;}
    .treat-row .price{grid-area:p;justify-self:start;text-align:left;}
    .treat-row:hover{padding-left:0;}
  }

  /* ---------- Process ---------- */
  .process{padding:100px 0;}
  .process-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:1px;background:var(--line);border:1px solid var(--line);}
  .step{background:var(--stone);padding:32px 26px;}
  .step .num{font-family:var(--serif);font-style:italic;font-size:30px;color:var(--bronze);margin-bottom:18px;}
  .step h3{font-size:17px;margin-bottom:10px;font-weight:500;}
  .step p{font-size:14px;color:var(--ink-2);}
  @media(max-width:900px){.process-grid{grid-template-columns:repeat(2,1fr);}}
  @media(max-width:520px){.process-grid{grid-template-columns:1fr;}}

  /* ---------- Team ---------- */
  .team{padding:100px 0;border-top:1px solid var(--line);}
  .team-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:0 24px;}
  .person{display:flex;align-items:center;gap:14px;padding:18px 0;border-bottom:1px solid var(--line);min-width:0;}
  .avatar{width:50px;height:50px;border-radius:50%;background:var(--ink);color:var(--cream);display:flex;align-items:center;justify-content:center;font-family:var(--serif);font-size:16px;flex-shrink:0;}
  .person div{min-width:0;}
  .person h4{font-size:16px;font-weight:500;overflow-wrap:break-word;}
  .person span{font-size:12.5px;color:var(--bronze-dark);}
  @media(max-width:780px){.team-grid{grid-template-columns:1fr;}}

  /* ---------- Testimonials ---------- */
  .testimonials{padding:100px 0;background:var(--green);color:var(--cream);}
  .testi-wrap{max-width:720px;margin:0 auto;text-align:center;}
  .testi-rating{font-size:13.5px;color:var(--gold);font-weight:700;margin-bottom:24px;letter-spacing:0.02em;}
  .testi-quote{font-family:var(--serif);font-style:italic;font-size:clamp(20px,3.4vw,30px);line-height:1.5;min-height:170px;transition:opacity .3s ease;}
  .testi-author{margin-top:26px;font-size:14px;opacity:0.75;}
  .testi-dots{display:flex;gap:10px;justify-content:center;margin-top:26px;}
  .testi-dots button{width:8px;height:8px;border-radius:50%;border:1px solid var(--gold);background:transparent;cursor:pointer;padding:0;}
  .testi-dots button.active{background:var(--gold);}

  /* ---------- Contact ---------- */
  .contact{padding:100px 0;}
  .contact-grid{display:grid;grid-template-columns:1fr 1fr;border:1px solid var(--line);}
  .contact-info{padding:46px;border-right:1px solid var(--line);min-width:0;}
  .contact-info h2{font-size:clamp(24px,3.5vw,34px);margin-bottom:26px;font-weight:400;}
  .info-row{padding:16px 0;border-top:1px solid var(--line);}
  .info-row:last-of-type{border-bottom:1px solid var(--line);}
  .info-row .label{font-size:11.5px;color:var(--bronze-dark);font-weight:700;margin-bottom:6px;display:block;}
  .info-row .value{font-size:15.5px;overflow-wrap:break-word;}
  .info-row .value a{border-bottom:1px solid currentColor;}
  .socials{display:flex;gap:14px;margin-top:24px;}
  .socials a{width:38px;height:38px;border:1px solid var(--ink);border-radius:50%;display:flex;align-items:center;justify-content:center;transition:background .25s ease,color .25s ease;flex-shrink:0;}
  .socials a:hover{background:var(--ink);color:var(--cream);}
  .contact-map{position:relative;min-height:340px;}
  .contact-map iframe{width:100%;height:100%;border:0;position:absolute;inset:0;filter:grayscale(45%) contrast(1.05);}
  @media(max-width:860px){
    .contact-grid{grid-template-columns:1fr;}
    .contact-info{border-right:none;border-bottom:1px solid var(--line);padding:34px 26px;}
    .contact-map{min-height:260px;}
  }

  /* ---------- CTA band ---------- */
  .cta-band{padding:80px 0;text-align:center;border-top:1px solid var(--line);}
  .cta-band h2{font-size:clamp(26px,4vw,40px);max-width:620px;margin:0 auto 30px;font-weight:400;}
  .cta-band .cta-actions{display:flex;gap:14px;justify-content:center;flex-wrap:wrap;}

  /* ---------- Footer ---------- */
  footer{background:var(--ink);color:var(--cream);padding:56px 0 26px;}
  .footer-grid{display:flex;justify-content:space-between;flex-wrap:wrap;gap:26px;padding-bottom:32px;border-bottom:1px solid var(--line-light);}
  footer .logo .mark{color:var(--cream);}
  .footer-nav{display:flex;gap:26px;flex-wrap:wrap;}
  .footer-nav a{font-size:13.5px;opacity:0.75;}
  .footer-nav a:hover{opacity:1;}
  .footer-bottom{display:flex;justify-content:space-between;align-items:center;padding-top:22px;font-size:12px;opacity:0.55;flex-wrap:wrap;gap:10px;}

  @media(max-width:960px){
    nav.primary-nav{display:none;}
    .burger{display:flex;}
    .hero .wrap{grid-template-columns:1fr;}
    .hero-art{order:-1;width:100%;margin:0 0 28px;padding-right:16px;}
    .hero-photo::before{top:12px;left:12px;right:-12px;bottom:-12px;}
  }
  @media(max-width:600px){
    .wrap{padding:0 16px;}
    .hero{padding:120px 0 60px;}
    .about,.treatments,.process,.team,.testimonials,.contact{padding:70px 0;}
    .cta-band{padding:60px 0;}
  }
</style>
</head>
<body>

<header id="siteHeader">
  <div class="wrap">
    <a href="#top" class="logo">
      <span class="mark">The Body</span>
      <span class="sub">KATOWICE</span>
    </a>
    <nav class="primary-nav">
      <a href="#o-nas">O nas</a>
      <a href="#zabiegi">Zabiegi</a>
      <a href="#proces">Wizyta</a>
      <a href="#zespol">Zespół</a>
      <a href="#opinie">Opinie</a>
      <a href="#kontakt">Kontakt</a>
    </nav>
    <div class="header-actions">
      <a href="tel:+48881471411" class="call-btn" aria-label="Zadzwoń: 881 471 411" title="Zadzwoń: 881 471 411">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M6.6 10.8c1.4 2.8 3.8 5.2 6.6 6.6l2.2-2.2c.3-.3.7-.4 1-.2 1.1.4 2.3.6 3.6.6.6 0 1 .4 1 1V20c0 .6-.4 1-1 1C10.6 21 3 13.4 3 4c0-.6.4-1 1-1h3.4c.6 0 1 .4 1 1 0 1.3.2 2.5.6 3.6.1.4 0 .8-.2 1L6.6 10.8Z"/></svg>
      </a>
      <a href="https://booksy.com/pl-pl/238094_the-body-katowice_trening-i-dieta_11597_katowice" target="_blank" rel="noopener" class="btn btn-primary">Zarezerwuj</a>
      <button class="burger" id="burgerBtn" aria-label="Otwórz menu">
        <span></span><span></span><span></span>
      </button>
    </div>
  </div>
</header>

<div class="mobile-nav" id="mobileNav">
  <button class="close-btn" id="closeMobileNav" aria-label="Zamknij menu">&times;</button>
  <a href="#o-nas">O nas</a>
  <a href="#zabiegi">Zabiegi</a>
  <a href="#proces">Wizyta</a>
  <a href="#zespol">Zespół</a>
  <a href="#opinie">Opinie</a>
  <a href="#kontakt">Kontakt</a>
  <a href="tel:+48881471411" class="call-line">
    <svg width="17" height="17" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M6.6 10.8c1.4 2.8 3.8 5.2 6.6 6.6l2.2-2.2c.3-.3.7-.4 1-.2 1.1.4 2.3.6 3.6.6.6 0 1 .4 1 1V20c0 .6-.4 1-1 1C10.6 21 3 13.4 3 4c0-.6.4-1 1-1h3.4c.6 0 1 .4 1 1 0 1.3.2 2.5.6 3.6.1.4 0 .8-.2 1L6.6 10.8Z"/></svg>
    881 471 411
  </a>
</div>

<main id="top">

  <!-- HERO -->
  <section class="hero">
    <div class="wrap">
      <div class="hero-copy">
        <div class="hero-eyebrow fade-up" style="animation-delay:.05s"><span class="dot"></span> Salon zabiegów na ciało — Katowice, Barcelońska 82</div>
        <h1 class="fade-up" style="animation-delay:.15s">Ciało to <em>projekt</em>,<br>nie przypadek.</h1>
        <p class="hero-sub fade-up" style="animation-delay:.28s">Terapia blizn, drenaż limfatyczny, modelowanie sylwetki i relaksujący masaż misami tybetańskimi — zabiegi dobrane indywidualnie, prowadzone przez specjalistki, które znają Twoje ciało lepiej niż niejeden trener.</p>
        <div class="hero-cta fade-up" style="animation-delay:.4s">
          <a href="https://booksy.com/pl-pl/238094_the-body-katowice_trening-i-dieta_11597_katowice" target="_blank" rel="noopener" class="btn btn-primary">Zarezerwuj wizytę</a>
          <a href="#zabiegi" class="btn btn-ghost">Zobacz zabiegi</a>
          <a href="tel:+48881471411" class="call-link">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M6.6 10.8c1.4 2.8 3.8 5.2 6.6 6.6l2.2-2.2c.3-.3.7-.4 1-.2 1.1.4 2.3.6 3.6.6.6 0 1 .4 1 1V20c0 .6-.4 1-1 1C10.6 21 3 13.4 3 4c0-.6.4-1 1-1h3.4c.6 0 1 .4 1 1 0 1.3.2 2.5.6 3.6.1.4 0 .8-.2 1L6.6 10.8Z"/></svg>
            881 471 411
          </a>
        </div>
        <div class="hero-meta fade-up" style="animation-delay:.55s">
          <div class="stat"><span class="num">5.0</span><span class="label">ocena Google · 54 opinie</span></div>
          <div class="stat"><span class="num">244</span><span class="label">opinii na Booksy</span></div>
          <div class="stat"><span class="num">90+</span><span class="label">zabiegów w ofercie</span></div>
        </div>
      </div>
      <div class="hero-art fade-up" style="animation-delay:.3s">
        <div class="hero-photo">
          <img src="hero.jpg" alt="The Body Katowice — profil kobiety i logo salonu" width="640" height="427">
        </div>
      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <section class="about" id="o-nas">
    <div class="wrap about-grid">
      <div class="about-copy">
        <span class="kicker">O salonie</span>
        <p class="lede">The Body to miejsce, w którym o ciało dba się kompleksowo — z uważnością, wiedzą i sprzętem, na jaki zasługuje.</p>
        <p>Powstaliśmy z myślą o dwóch potrzebach: skutecznej regeneracji skóry i sylwetki oraz realnym treningu, który wspiera efekty zabiegowe. Każdy plan układamy indywidualnie — po konsultacji, nie z cennika.</p>
        <p>Pracujemy w oparciu o sprawdzone technologie i ręczne techniki: terapię blizn metodą MSTR, drenaż limfatyczny, masaż antycellulitowy, lipoplastykę manualną oraz głęboko relaksujący masaż misami tybetańskimi. Efekty widać, bo praca zaczyna się od diagnozy, nie od zabiegu.</p>
      </div>
      <div class="zones">
        <div class="zone">
          <div class="zone-tag">Strefa I</div>
          <div>
            <h3>Strefa treningowa</h3>
            <p>Bieżnie termoaktywne Vacutherm i automatyczne rolery do ciała — trening, który wspomaga krążenie, spalanie i efekty zabiegów modelujących.</p>
          </div>
        </div>
        <div class="zone">
          <div class="zone-tag">Strefa II</div>
          <div>
            <h3>Strefa gabinetowa</h3>
            <p>Gabinety zabiegowe, w których dobieramy technikę do celu: blizna, rozstęp, cellulit, obrzęk limfatyczny czy głęboki relaks — każdy przypadek traktujemy osobno.</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- TREATMENTS -->
  <section class="treatments" id="zabiegi">
    <div class="wrap">
      <div class="section-head">
        <div>
          <span class="kicker">Oferta</span>
          <h2>Ponad 90 zabiegów — dobranych do Twojego ciała, nie do kalendarza promocji.</h2>
        </div>
        <p>Pełna oferta z aktualnymi cenami i promocjami dostępna jest na Booksy — poniżej przegląd wg kategorii.</p>
      </div>

      <div class="treat-tabs" id="treatTabs">
        <button class="tab-btn active" data-tab="popularne">Popularne</button>
        <button class="tab-btn" data-tab="sylwetka">Modelowanie sylwetki</button>
        <button class="tab-btn" data-tab="twarz">Zabiegi na twarz</button>
        <button class="tab-btn" data-tab="masaz">Masaż</button>
        <button class="tab-btn" data-tab="depilacja">Depilacja i laser</button>
        <button class="tab-btn" data-tab="paznokcie">Paznokcie</button>
        <button class="tab-btn" data-tab="zaawansowane">Zaawansowana pielęgnacja</button>
      </div>

      <div class="treat-panels">

        <div class="treat-panel active" id="panel-popularne">
          <div class="treat-row"><span class="idx">01</span><h3>Masaż antycellulitowy</h3><p class="desc">Poprawa krążenia, ujędrnienie i redukcja cellulitu — wybrana partia lub całe ciało.</p><span class="price">od 240 zł</span></div>
          <div class="treat-row"><span class="idx">02</span><h3>Terapia blizn MSTR</h3><p class="desc">Manualna terapia tkanki bliznowatej metodą McLoughlin Scar Tissue Release.</p><span class="price">250 zł</span></div>
          <div class="treat-row"><span class="idx">03</span><h3>Autorski masaż</h3><p class="desc">Połączenie masażu antycellulitowego, limfodrenażu, Lipokiller i relaksacyjnego.</p><span class="price">350 zł</span></div>
          <div class="treat-row"><span class="idx">04</span><h3>Zabieg na twarz dedykowany</h3><p class="desc">Kompleksowa pielęgnacja twarzy dobrana indywidualnie po konsultacji.</p><span class="price">330 zł</span></div>
          <div class="treat-row"><span class="idx">05</span><h3>Endermologia</h3><p class="desc">Zabieg aparaturowy modelujący sylwetkę — pojedynczo lub w pakiecie.</p><span class="price">od 90 zł</span></div>
          <div class="treat-row"><span class="idx">06</span><h3>Pedicure</h3><p class="desc">Higieniczny, hybrydowy lub klasyczny z hybrydą.</p><span class="price">od 100 zł</span></div>
        </div>

        <div class="treat-panel" id="panel-sylwetka">
          <div class="treat-row"><span class="idx">01</span><h3>HIFU ciało i twarz<span class="promo">Promocja</span></h3><p class="desc">Skoncentrowane ultradźwięki — lifting i modelowanie bez skalpela.</p><span class="price">od 405 zł</span></div>
          <div class="treat-row"><span class="idx">02</span><h3>Terapia blizn i rozstępów</h3><p class="desc">Mikropunktura przebudowująca tkankę — blizny i rozstępy stają się płytsze.</p><span class="price">od 45 zł</span></div>
          <div class="treat-row"><span class="idx">03</span><h3>Indiba Deep Beauty</h3><p class="desc">Redukcja tkanki tłuszczowej i cellulitu, detoksykacja i drenaż.</p><span class="price">od 135 zł</span></div>
          <div class="treat-row"><span class="idx">04</span><h3>Liporadiologia Vinci</h3><p class="desc">Fale radiowe, LED i masaż podciśnieniowy — redukcja tkanki tłuszczowej.</p><span class="price">od 180 zł</span></div>
          <div class="treat-row"><span class="idx">05</span><h3>RF Infinity ciało<span class="promo">Promocja</span></h3><p class="desc">Fale radiowe pobudzające produkcję kolagenu — ujędrnienie skóry.</p><span class="price">od 180 zł</span></div>
          <div class="treat-row"><span class="idx">06</span><h3>Mezoterapia lipolityczna</h3><p class="desc">L-karnityna wspomagająca spalanie tłuszczu na opornych partiach.</p><span class="price">450 zł</span></div>
          <div class="treat-row"><span class="idx">07</span><h3>ThermoGenique Body Shape</h3><p class="desc">Wyszczuplenie, ujędrnienie i redukcja obrzęków z masażem drenującym.</p><span class="price">od 207 zł</span></div>
          <div class="treat-row"><span class="idx">08</span><h3>Terapia czaszkowo-krzyżowa</h3><p class="desc">Delikatna praca manualna redukująca napięcia i stres w całym ciele.</p><span class="price">270 zł</span></div>
        </div>

        <div class="treat-panel" id="panel-twarz">
          <div class="treat-row"><span class="idx">01</span><h3>Masaż kosmetologiczny</h3><p class="desc">Relaksujący masaż poprawiający napięcie i koloryt skóry twarzy.</p><span class="price">225 zł</span></div>
          <div class="treat-row"><span class="idx">02</span><h3>RF Infinity twarz</h3><p class="desc">Fale radiowe napinające skórę i wygładzające zmarszczki.</p><span class="price">od 252 zł</span></div>
          <div class="treat-row"><span class="idx">03</span><h3>ThermoGenique twarz</h3><p class="desc">Kontrolowane ciepło stymulujące kolagen i elastynę.</p><span class="price">135 zł</span></div>
          <div class="treat-row"><span class="idx">04</span><h3>Liporadiologia twarzy</h3><p class="desc">Lifting i odmłodzenie — gładsza, bardziej elastyczna skóra.</p><span class="price">od 180 zł</span></div>
          <div class="treat-row"><span class="idx">05</span><h3>Akupunktura kosmetyczna</h3><p class="desc">Precyzyjne igły pobudzające mikrokrążenie i produkcję kolagenu.</p><span class="price">270 zł</span></div>
          <div class="treat-row"><span class="idx">06</span><h3>Mezoterapia igłowa</h3><p class="desc">Nawilżenie i regeneracja preparatami Jalupro, Revok, Neauvia.</p><span class="price">od 270 zł</span></div>
          <div class="treat-row"><span class="idx">07</span><h3>BB Glow</h3><p class="desc">Rozświetlenie i wyrównanie kolorytu — efekt „make-up no make-up”.</p><span class="price">198 zł</span></div>
          <div class="treat-row"><span class="idx">08</span><h3>Biolifting twarzy</h3><p class="desc">Nieinwazyjny lifting igłowy stymulujący kolagen.</p><span class="price">od 495 zł</span></div>
        </div>

        <div class="treat-panel" id="panel-masaz">
          <div class="treat-row"><span class="idx">01</span><h3>Manualny drenaż limfatyczny</h3><p class="desc">Redukcja obrzęków, wsparcie regeneracji po zabiegach estetycznych.</p><span class="price">220 zł</span></div>
          <div class="treat-row"><span class="idx">02</span><h3>Masaż relaksacyjny dla kobiet</h3><p class="desc">Płynne, delikatne ruchy na indywidualnie dobranym olejku.</p><span class="price">250 zł</span></div>
          <div class="treat-row"><span class="idx">03</span><h3>Lipokiller</h3><p class="desc">Silny limfodrenaż połączony z modelowaniem sylwetki.</p><span class="price">400 zł</span></div>
          <div class="treat-row"><span class="idx">04</span><h3>Lipoplastyka manualna</h3><p class="desc">Precyzyjne modelowanie wybranej partii ciała.</p><span class="price">od 500 zł</span></div>
          <div class="treat-row"><span class="idx">05</span><h3>Masaż Kobido</h3><p class="desc">Japoński masaż liftingujący twarz, szyję i dekolt.</p><span class="price">250 zł</span></div>
          <div class="treat-row"><span class="idx">06</span><h3>Masaż misami tybetańskimi</h3><p class="desc">Głęboko relaksujący masaż dźwiękiem — wyciszenie i odprężenie ciała.</p><span class="price">250 zł</span></div>
          <div class="treat-row"><span class="idx">07</span><h3>Masaż dla kobiet w ciąży</h3><p class="desc">Delikatny masaż dostosowany do potrzeb przyszłych mam.</p><span class="price">200 zł</span></div>
          <div class="treat-row"><span class="idx">08</span><h3>Owijanie Styx Aroma Derm</h3><p class="desc">Gorące owijanie z aromaterapią — nawilżenie i ujędrnienie.</p><span class="price">250 zł</span></div>
        </div>

        <div class="treat-panel" id="panel-depilacja">
          <div class="treat-row"><span class="idx">01</span><h3>Depilacja laserowa</h3><p class="desc">Wąsik, pachy, bikini, nogi — pojedynczo lub w pakietach.</p><span class="price">od 80 zł</span></div>
          <div class="treat-row"><span class="idx">02</span><h3>Peeling węglowy</h3><p class="desc">Laserowe oczyszczenie i rozjaśnienie skóry twarzy.</p><span class="price">261 zł</span></div>
          <div class="treat-row"><span class="idx">03</span><h3>Fotoodmładzanie</h3><p class="desc">Redukcja oznak starzenia i poprawa kolorytu skóry.</p><span class="price">315 zł</span></div>
          <div class="treat-row"><span class="idx">04</span><h3>Usuwanie naczynek i rumienia</h3><p class="desc">Precyzyjna redukcja widocznych naczynek i zaczerwienień.</p><span class="price">od 225 zł</span></div>
          <div class="treat-row"><span class="idx">05</span><h3>Laser tułowy — ciało<span class="promo">Promocja</span></h3><p class="desc">Modelowanie większych partii — brzuch, twarz, szyja, dekolt.</p><span class="price">od 799 zł</span></div>
        </div>

        <div class="treat-panel" id="panel-paznokcie">
          <div class="treat-row"><span class="idx">01</span><h3>Manicure hybrydowy</h3><p class="desc">Trwały kolor z pielęgnacją paznokcia i skórek.</p><span class="price">130 zł</span></div>
          <div class="treat-row"><span class="idx">02</span><h3>Przedłużanie paznokci żelowe</h3><p class="desc">Dowolna długość, pełne modelowanie w żelu.</p><span class="price">od 180 zł</span></div>
          <div class="treat-row"><span class="idx">03</span><h3>Manicure klasyczny</h3><p class="desc">Manicure medyczny z wzmocnieniem paznokcia.</p><span class="price">80 zł</span></div>
          <div class="treat-row"><span class="idx">04</span><h3>Pedicure hybrydowy</h3><p class="desc">Klasyczny zabieg pielęgnacyjny z hybrydą na stopach.</p><span class="price">100 zł</span></div>
        </div>

        <div class="treat-panel" id="panel-zaawansowane">
          <div class="treat-row"><span class="idx">01</span><h3>Karboksyterapia CO2 (RIBESKIN)</h3><p class="desc">Dwutlenek węgla pobudzający regenerację skóry twarzy.</p><span class="price">198 zł</span></div>
          <div class="treat-row"><span class="idx">02</span><h3>Zabieg Jurgita Cosmeceuticals</h3><p class="desc">Rewitalizacja i kolagenowa regeneracja skóry.</p><span class="price">od 180 zł</span></div>
          <div class="treat-row"><span class="idx">03</span><h3>Owijanie Jurgita Tone Up</h3><p class="desc">Napięcie skóry, drenaż i redukcja cellulitu w jednym zabiegu.</p><span class="price">225 zł</span></div>
          <div class="treat-row"><span class="idx">04</span><h3>Fototerapia Celluma LED</h3><p class="desc">Trzy długości fal światła — regeneracja i redukcja stanów zapalnych.</p><span class="price">72 zł</span></div>
          <div class="treat-row"><span class="idx">05</span><h3>Elektrostymulacja BodyPro</h3><p class="desc">Pole elektromagnetyczne wzmacniające mięśnie bez ćwiczeń.</p><span class="price">od 160 zł</span></div>
        </div>

      </div>

      <div class="treat-more">
        <p>To wybrane zabiegi z każdej kategorii — pełny, zawsze aktualny cennik (90+ pozycji, w tym bieżące promocje) znajdziesz na Booksy.</p>
        <a href="https://booksy.com/pl-pl/238094_the-body-katowice_trening-i-dieta_11597_katowice" target="_blank" rel="noopener" class="btn btn-ghost-light">Zobacz pełny cennik na Booksy</a>
      </div>
    </div>
  </section>

  <!-- PROCESS -->
  <section class="process" id="proces">
    <div class="wrap">
      <div class="section-head">
        <div>
          <span class="kicker">Jak to wygląda</span>
          <h2>Cztery kroki od pierwszej wizyty do efektu.</h2>
        </div>
      </div>
      <div class="process-grid">
        <div class="step">
          <div class="num">01</div>
          <h3>Konsultacja</h3>
          <p>Rozmawiamy o celu, historii skóry i oczekiwaniach — bez zgadywania.</p>
        </div>
        <div class="step">
          <div class="num">02</div>
          <h3>Diagnoza i plan</h3>
          <p>Dobieramy zabiegi i częstotliwość sesji indywidualnie do przypadku.</p>
        </div>
        <div class="step">
          <div class="num">03</div>
          <h3>Realizacja</h3>
          <p>Seria zabiegów prowadzona przez tę samą specjalistkę, krok po kroku.</p>
        </div>
        <div class="step">
          <div class="num">04</div>
          <h3>Efekt i pielęgnacja</h3>
          <p>Zalecenia domowe i plan podtrzymujący, by efekt został z Tobą na dłużej.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- TEAM -->
  <section class="team" id="zespol">
    <div class="wrap">
      <div class="section-head">
        <div>
          <span class="kicker">Zespół</span>
          <h2>Specjalistki, które prowadzą Cię przez cały proces.</h2>
        </div>
        <p>Każda klientka pracuje z jedną specjalistką od konsultacji po ostatnią sesję.</p>
      </div>
      <div class="team-grid">
        <div class="person"><div class="avatar">OH</div><div><h4>Olena Hrynchuk</h4><span>Drenaż, masaż, lipoplastyka</span></div></div>
        <div class="person"><div class="avatar">NT</div><div><h4>Nataliia Tyshchenko</h4><span>Terapia blizn i skóry</span></div></div>
        <div class="person"><div class="avatar">L</div><div><h4>Lucyna</h4><span>Masaż antycellulitowy</span></div></div>
        <div class="person"><div class="avatar">WW</div><div><h4>Wiera Wiśniewska</h4><span>Zabiegi na twarz i ciało</span></div></div>
        <div class="person"><div class="avatar">SS</div><div><h4>Sandra Spałek</h4><span>Modelowanie sylwetki, laser</span></div></div>
        <div class="person"><div class="avatar">DL</div><div><h4>Dagmara Lewandowska</h4><span>Elektrostymulacja, lipoplastyka</span></div></div>
        <div class="person"><div class="avatar">M</div><div><h4>Martyna</h4><span>Stylizacja paznokci</span></div></div>
        <div class="person"><div class="avatar">A</div><div><h4>Anastazja</h4><span>Stylizacja paznokci</span></div></div>
        <div class="person"><div class="avatar">SP</div><div><h4>Sonia / Paulina</h4><span>Recepcja i konsultacje</span></div></div>
      </div>
    </div>
  </section>

  <!-- TESTIMONIALS -->
  <section class="testimonials" id="opinie">
    <div class="wrap testi-wrap">
      <div class="testi-rating">★★★★★ &nbsp; 5.0 na Google i Booksy</div>
      <div class="testi-quote" id="testiQuote">Po trzech sesjach terapii blizny metodą MSTR nie spodziewałam się aż takich efektów — blizna, którą miałam od dziecka, wygląda zupełnie inaczej.</div>
      <div class="testi-author" id="testiAuthor">Anna Spiridonova, Google</div>
      <div class="testi-dots" id="testiDots"></div>
    </div>
  </section>

  <!-- CTA BAND -->
  <section class="cta-band">
    <div class="wrap">
      <h2>Umów konsultację i dowiedz się, który zabieg naprawdę zadziała na Twoje ciało.</h2>
      <div class="cta-actions">
        <a href="https://booksy.com/pl-pl/238094_the-body-katowice_trening-i-dieta_11597_katowice" target="_blank" rel="noopener" class="btn btn-primary">Zarezerwuj online</a>
        <a href="tel:+48881471411" class="btn btn-ghost">Zadzwoń: 881 471 411</a>
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section class="contact" id="kontakt">
    <div class="wrap">
      <div class="contact-grid">
        <div class="contact-info">
          <h2>Odwiedź nas przy Barcelońskiej.</h2>
          <div class="info-row">
            <span class="label">Adres</span>
            <span class="value">Barcelońska 82, 40-683 Katowice</span>
          </div>
          <div class="info-row">
            <span class="label">Telefon</span>
            <span class="value"><a href="tel:+48881471411">881 471 411</a></span>
          </div>
          <div class="info-row">
            <span class="label">E-mail</span>
            <span class="value"><a href="mailto:salon@thebodykatowice.pl">salon@thebodykatowice.pl</a></span>
          </div>
          <div class="info-row">
            <span class="label">Godziny</span>
            <span class="value">Pon–Pt 8:00–20:00 · Sob od 9:00<br><a href="https://booksy.com/pl-pl/238094_the-body-katowice_trening-i-dieta_11597_katowice" target="_blank" rel="noopener">sprawdź dostępne terminy na Booksy</a></span>
          </div>
          <div class="socials">
            <a href="https://www.instagram.com/the_body_katowice/" target="_blank" rel="noopener" aria-label="Instagram">
              <svg width="17" height="17" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><rect x="3" y="3" width="18" height="18" rx="5"/><circle cx="12" cy="12" r="4"/><circle cx="17.5" cy="6.5" r="1"/></svg>
            </a>
            <a href="https://www.facebook.com/people/The-Body-Katowice/100063754171465/" target="_blank" rel="noopener" aria-label="Facebook">
              <svg width="17" height="17" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M15 8h-2a2 2 0 0 0-2 2v3H9v3h2v6h3v-6h2.5l.5-3H14v-2a1 1 0 0 1 1-1h2V8Z"/></svg>
            </a>
            <a href="tel:+48881471411" aria-label="Zadzwoń">
              <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M6.6 10.8c1.4 2.8 3.8 5.2 6.6 6.6l2.2-2.2c.3-.3.7-.4 1-.2 1.1.4 2.3.6 3.6.6.6 0 1 .4 1 1V20c0 .6-.4 1-1 1C10.6 21 3 13.4 3 4c0-.6.4-1 1-1h3.4c.6 0 1 .4 1 1 0 1.3.2 2.5.6 3.6.1.4 0 .8-.2 1L6.6 10.8Z"/></svg>
            </a>
          </div>
        </div>
        <div class="contact-map">
          <iframe loading="lazy" src="https://www.google.com/maps?q=Barcelo%C5%84ska+82,+40-683+Katowice&output=embed" title="Mapa — The Body Katowice, Barcelońska 82"></iframe>
        </div>
      </div>
    </div>
  </section>

</main>

<footer>
  <div class="wrap">
    <div class="footer-grid">
      <a href="#top" class="logo"><span class="mark">The Body</span><span class="sub">KATOWICE</span></a>
      <nav class="footer-nav">
        <a href="#o-nas">O nas</a>
        <a href="#zabiegi">Zabiegi</a>
        <a href="#zespol">Zespół</a>
        <a href="#opinie">Opinie</a>
        <a href="#kontakt">Kontakt</a>
        <a href="tel:+48881471411">881 471 411</a>
      </nav>
    </div>
    <div class="footer-bottom">
      <span>© 2026 The Body Katowice · Barcelońska 82, 40-683 Katowice</span>
      <span>Projekt strony — makieta do dalszej rozbudowy</span>
    </div>
  </div>
</footer>

<script>
  const header = document.getElementById('siteHeader');
  window.addEventListener('scroll', () => header.classList.toggle('scrolled', window.scrollY > 40));

  const burgerBtn = document.getElementById('burgerBtn');
  const closeBtn = document.getElementById('closeMobileNav');
  const mobileNav = document.getElementById('mobileNav');
  burgerBtn.addEventListener('click', () => mobileNav.classList.add('open'));
  closeBtn.addEventListener('click', () => mobileNav.classList.remove('open'));
  mobileNav.querySelectorAll('a').forEach(a => a.addEventListener('click', () => mobileNav.classList.remove('open')));

  // Treatment category tabs
  const tabBtns = document.querySelectorAll('.tab-btn');
  const panels = document.querySelectorAll('.treat-panel');
  tabBtns.forEach(btn => {
    btn.addEventListener('click', () => {
      tabBtns.forEach(b => b.classList.remove('active'));
      panels.forEach(p => p.classList.remove('active'));
      btn.classList.add('active');
      document.getElementById('panel-' + btn.dataset.tab).classList.add('active');
    });
  });

  const testimonials = [
    { quote: "Po trzech sesjach terapii blizny metodą MSTR nie spodziewałam się aż takich efektów — blizna, którą miałam od dziecka, wygląda zupełnie inaczej.", author: "Anna Spiridonova, Google" },
    { quote: "Serdecznie polecam wizyty na drenażu, masażu antycellulitowym i lipoplastyce — profesjonalizm i realne efekty od pierwszej sesji.", author: "Monika Staszewska, Google" },
    { quote: "Jedno z najlepszych miejsc na masaż limfatyczny, w jakich byłam — podejście indywidualne i uważne na każdym etapie.", author: "Anna Pint, Google" }
  ];
  let testiIndex = 0;
  const quoteEl = document.getElementById('testiQuote');
  const authorEl = document.getElementById('testiAuthor');
  const dotsEl = document.getElementById('testiDots');
  testimonials.forEach((_, i) => {
    const dot = document.createElement('button');
    if (i === 0) dot.classList.add('active');
    dot.addEventListener('click', () => showTesti(i));
    dotsEl.appendChild(dot);
  });
  function showTesti(i){
    testiIndex = i;
    quoteEl.style.opacity = 0;
    setTimeout(() => {
      quoteEl.textContent = testimonials[i].quote;
      authorEl.textContent = testimonials[i].author;
      quoteEl.style.opacity = 1;
    }, 200);
    [...dotsEl.children].forEach((d, idx) => d.classList.toggle('active', idx === i));
  }
  setInterval(() => showTesti((testiIndex + 1) % testimonials.length), 6000);
</script>

</body>
</html>
hero.jpg
