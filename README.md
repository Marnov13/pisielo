<!DOCTYPE html>
<html lang="it">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>La Fraschetta di San Paolo — Hostaria Romana</title>
<meta name="description" content="La Fraschetta di San Paolo — hostaria romana in Via Gabriello Chiabrera 128, Roma. Salumi, primi della tradizione e vino della casa, tutti i giorni a pranzo e cena.">
<link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'%3E%3Ctext y='.9em' font-size='90'%3E%F0%9F%8D%83%3C/text%3E%3C/svg%3E">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,500;0,9..144,600;0,9..144,900;1,9..144,500&family=Spectral:ital,wght@0,400;0,500;0,600;1,400&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet">
<style>
  /* ---------- Tokens ---------- */
  :root{
    --wine:      #6B1E2B;
    --wine-dark: #43121C;
    --parchment: #ECE1C8;
    --parchment-2:#E2D4B0;
    --walnut:    #2A1D14;
    --olive:     #6B7048;
    --brass:     #C9962F;
    --brass-ink: #8A5F1E;
    --cream-ink: #FBF6E9;

    --font-display: 'Fraunces', serif;
    --font-body: 'Spectral', serif;
    --font-mono: 'Space Mono', monospace;

    --container: 1120px;
    --edge: 6px;
  }

  *,*::before,*::after{ box-sizing: border-box; }
  html{ scroll-behavior: smooth; }
  body{
    margin:0;
    background: var(--parchment);
    color: var(--walnut);
    font-family: var(--font-body);
    font-size: 17px;
    line-height: 1.6;
    -webkit-font-smoothing: antialiased;
  }
  img,svg{ display:block; max-width:100%; }
  a{ color: inherit; }
  h1,h2,h3{ font-family: var(--font-display); margin: 0; font-weight: 600; letter-spacing: -0.01em; }
  p{ margin: 0 0 1em; }
  .container{ width:100%; max-width: var(--container); margin: 0 auto; padding: 0 24px; }
  section{ scroll-margin-top: 84px; }

  /* subtle paper grain, overlay across whole page */
  body::before{
    content:"";
    position: fixed; inset:0; z-index: 0; pointer-events:none;
    opacity: .5; mix-blend-mode: multiply;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='160' height='160'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='2' stitchTiles='stitch'/%3E%3CfeColorMatrix type='matrix' values='0 0 0 0 0  0 0 0 0 0  0 0 0 0 0  0 0 0 0.035 0'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");
  }

  :focus-visible{ outline: 3px solid var(--olive); outline-offset: 3px; }

  .eyebrow{
    font-family: var(--font-mono); font-size: 12.5px; letter-spacing: .18em; text-transform: uppercase;
    color: var(--brass-ink); display:flex; align-items:center; gap:10px; margin-bottom: 14px;
  }
  .eyebrow::before{ content:""; width: 22px; height:1px; background: var(--brass-ink); display:inline-block; }

  .btn{
    display:inline-flex; align-items:center; gap:8px; justify-content:center;
    font-family: var(--font-mono); font-size: 13.5px; letter-spacing:.04em; text-transform: uppercase;
    padding: 14px 24px; border-radius: 2px; text-decoration:none; border: 1.5px solid currentColor;
    transition: transform .15s ease, background .2s ease, color .2s ease;
  }
  .btn:hover{ transform: translateY(-2px); }
  .btn-solid{ background: var(--brass); border-color: var(--brass); color: var(--wine-dark); }
  .btn-solid:hover{ background: var(--cream-ink); }
  .btn-outline{ color: var(--cream-ink); border-color: rgba(251,246,233,.55); }
  .btn-outline:hover{ background: rgba(251,246,233,.1); }
  .btn-dark{ color: var(--wine-dark); border-color: var(--wine-dark); }
  .btn-dark:hover{ background: var(--wine-dark); color: var(--cream-ink); }

  /* ---------- Nav ---------- */
  header{
    position: sticky; top:0; z-index: 50;
    background: transparent;
    transition: background .35s ease, box-shadow .35s ease, padding .3s ease;
    padding: 22px 0;
  }
  header.solid{
    background: rgba(236,225,200,.94); backdrop-filter: blur(6px);
    box-shadow: 0 1px 0 rgba(42,29,20,.12); padding: 12px 0;
  }
  nav{ display:flex; align-items:center; justify-content:space-between; }
  .brand{ display:flex; align-items:center; gap:12px; text-decoration:none; color: inherit; }
  header:not(.solid) .brand{ color: var(--cream-ink); }
  .brand-mark{ width: 40px; height:40px; color: currentColor; flex-shrink:0; }
  .brand-text{ font-family: var(--font-display); font-weight:600; font-size: 17px; line-height:1.1; }
  .brand-text small{ display:block; font-family: var(--font-mono); font-size:9.5px; letter-spacing:.16em; opacity:.75; font-weight:400; text-transform:uppercase; margin-top:3px;}

  .nav-links{ display:flex; align-items:center; gap: 34px; list-style:none; margin:0; padding:0; }
  .nav-links a{ text-decoration:none; font-family: var(--font-mono); font-size: 13px; letter-spacing:.06em; text-transform:uppercase; position:relative; padding-bottom:3px; }
  header:not(.solid) .nav-links a{ color: var(--cream-ink); }
  .nav-links a::after{ content:""; position:absolute; left:0; bottom:0; width:0; height:1.5px; background: currentColor; transition: width .25s ease; }
  .nav-links a:hover::after{ width:100%; }
  .nav-cta{ display:flex; align-items:center; gap:14px; }
  .nav-toggle{ display:none; background:none; border:none; cursor:pointer; padding:8px; color:inherit; }
  header:not(.solid) .nav-toggle{ color: var(--cream-ink); }

  /* ---------- Hero ---------- */
  .hero{
    position: relative; overflow:hidden;
    background: radial-gradient(120% 140% at 15% -10%, #7c2536 0%, var(--wine) 42%, var(--wine-dark) 100%);
    color: var(--cream-ink);
    padding: 96px 0 110px;
    margin-top: -86px; /* sits behind sticky header */
  }
  .hero-grid{
    display:grid; grid-template-columns: 1.1fr .9fr; gap: 48px; align-items:center;
    padding-top: 86px;
  }
  .hero h1{ font-size: clamp(38px, 5.4vw, 62px); line-height: 1.03; margin: 6px 0 20px; }
  .hero h1 em{ font-style: italic; font-weight:500; color: var(--brass); }
  .hero p.lede{ font-size: 19px; max-width: 46ch; color: rgba(251,246,233,.88); }
  .hero-actions{ display:flex; flex-wrap:wrap; gap:14px; margin-top: 32px; }
  .hero-addr{ margin-top: 34px; font-family: var(--font-mono); font-size: 12.5px; color: rgba(251,246,233,.7); letter-spacing:.04em; }

  .stamp-wrap{ display:flex; justify-content:center; }
  .stamp{ width: min(340px, 78vw); height:auto; color: var(--brass); }
  .stamp .ink{ color: var(--cream-ink); opacity:.9; }
  @media (prefers-reduced-motion: no-preference){
    .stamp{ animation: stampPress .9s cubic-bezier(.2,.9,.25,1) both; animation-delay:.15s; }
  }
  @keyframes stampPress{
    0%{ transform: scale(1.5) rotate(-8deg); opacity:0; }
    60%{ transform: scale(.96) rotate(1deg); opacity:1; }
    100%{ transform: scale(1) rotate(0deg); opacity:1; }
  }

  /* ---------- Reveal on scroll ---------- */
  .reveal{ opacity:0; transform: translateY(18px); transition: opacity .7s ease, transform .7s ease; }
  .reveal.in{ opacity:1; transform:none; }
  @media (prefers-reduced-motion: reduce){ .reveal{ opacity:1; transform:none; transition:none; } }

  /* ---------- Storia ---------- */
  .storia{ padding: 108px 0 90px; position:relative; z-index:1; }
  .storia-grid{ display:grid; grid-template-columns: 1fr .72fr; gap: 64px; align-items:start; }
  .storia h2{ font-size: clamp(30px,3.6vw,42px); margin-bottom:22px; }
  .storia .lead{ font-size: 20px; font-style: italic; color: var(--wine-dark); font-family: var(--font-display); font-weight:500; margin-bottom:20px; }
  .storia p{ color: rgba(42,29,20,.86); }
  .frasca-rule{ width:64px; height:34px; color: var(--olive); margin-bottom: 26px; }

  .fact-card{ background: var(--cream-ink); border: 1px solid rgba(42,29,20,.12); padding: 30px 28px; box-shadow: 4px 4px 0 rgba(107,30,43,.08); }
  .fact-card dl{ margin:0; display:grid; gap:18px; }
  .fact-card dt{ font-family: var(--font-mono); font-size:11px; letter-spacing:.14em; text-transform:uppercase; color: var(--brass-ink); }
  .fact-card dd{ margin: 4px 0 0; font-family: var(--font-display); font-size: 18px; }
  .fact-card hr{ border:none; border-top:1px dashed rgba(42,29,20,.25); margin:0; }

  /* ---------- Menu ---------- */
  .menu{ background: var(--walnut); color: var(--parchment); padding: 100px 0 110px; position:relative; z-index:1; }
  .menu-head{ text-align:center; max-width: 620px; margin: 0 auto 20px; }
  .menu-head .eyebrow{ justify-content:center; color: var(--brass); }
  .menu-head .eyebrow::before,.menu-head .eyebrow::after{ content:""; width:22px; height:1px; background: var(--brass); }
  .menu-head h2{ font-size: clamp(32px,4vw,46px); color: var(--cream-ink); }

  .menu-note{
    max-width: 620px; margin: 26px auto 64px; text-align:center;
    border: 1px dashed rgba(201,150,47,.55); padding: 16px 22px; font-family: var(--font-mono); font-size: 12.5px;
    letter-spacing:.02em; color: rgba(236,225,200,.82); position:relative;
  }
  .menu-note strong{ color: var(--brass); letter-spacing:.1em; }

  .menu-grid{ display:grid; grid-template-columns: repeat(2,1fr); gap: 56px 64px; }
  .menu-section h3{
    font-family: var(--font-mono); font-size: 13px; letter-spacing:.2em; text-transform:uppercase;
    color: var(--brass); padding-bottom:10px; border-bottom: 1px solid rgba(201,150,47,.35); margin-bottom: 22px;
  }
  .dish{ display:flex; align-items:baseline; gap:10px; padding: 13px 0; border-bottom: 1px dotted rgba(236,225,200,.22); }
  .dish:last-child{ border-bottom:none; }
  .dish-name{ font-family: var(--font-display); font-size: 17px; font-weight:500; color: var(--cream-ink); }
  .dish-desc{ display:block; font-family: var(--font-body); font-style:italic; font-size: 13.5px; color: rgba(236,225,200,.6); margin-top:3px; }
  .dish-leader{ flex:1; border-bottom: 1px dotted rgba(236,225,200,.28); transform: translateY(-4px); min-width: 16px; }
  .dish-price{ font-family: var(--font-mono); font-size:14.5px; color: var(--brass); white-space:nowrap; }

  .menu-foot{ text-align:center; font-family: var(--font-mono); font-size:12px; color: rgba(236,225,200,.55); margin-top:56px; letter-spacing:.04em; }

  /* ---------- Dove siamo ---------- */
  .info{ padding: 104px 0 110px; position:relative; z-index:1; }
  .info-grid{ display:grid; grid-template-columns: .82fr 1.18fr; gap: 56px; align-items:start; }
  .info h2{ font-size: clamp(30px,3.6vw,42px); margin-bottom: 26px; }
  .hours{ width:100%; border-collapse: collapse; margin: 26px 0 30px; font-family: var(--font-mono); font-size:14px; }
  .hours td{ padding: 9px 0; border-bottom: 1px dashed rgba(42,29,20,.2); }
  .hours td:last-child{ text-align:right; color: var(--wine-dark); font-weight:700; }
  .info-line{ display:flex; gap:12px; align-items:flex-start; margin-bottom:16px; font-size:15.5px; }
  .info-line svg{ width:19px; height:19px; flex-shrink:0; margin-top:3px; color: var(--wine); }
  .info-actions{ display:flex; flex-wrap:wrap; gap:14px; margin-top: 26px; }

  .map-frame{ border: 1px solid rgba(42,29,20,.15); box-shadow: 6px 6px 0 rgba(107,30,43,.1); overflow:hidden; }
  .map-frame iframe{ width:100%; height: 420px; border:0; display:block; filter: sepia(.15) saturate(.9); }

  /* ---------- Footer ---------- */
  footer{ background: var(--wine-dark); color: rgba(236,225,200,.75); padding: 56px 0 34px; }
  .footer-grid{ display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap; gap: 26px; }
  .footer-brand{ display:flex; align-items:center; gap:14px; }
  .footer-brand .brand-mark{ width:36px; height:36px; color: var(--brass); }
  .footer-brand strong{ font-family: var(--font-display); color: var(--cream-ink); font-size:17px; display:block; }
  .footer-brand span{ font-family: var(--font-mono); font-size:11.5px; letter-spacing:.03em; }
  .footer-social{ display:flex; gap: 20px; font-family: var(--font-mono); font-size:13px; }
  .footer-social a{ text-decoration:none; border-bottom:1px solid rgba(201,150,47,.4); padding-bottom:2px; }
  .footer-social a:hover{ border-color: var(--brass); color: var(--brass); }
  .footer-bottom{ margin-top: 34px; padding-top: 24px; border-top: 1px solid rgba(236,225,200,.12); font-family: var(--font-mono); font-size: 11.5px; text-align:center; letter-spacing:.03em; }

  /* ---------- Mobile ---------- */
  @media (max-width: 880px){
    .hero-grid{ grid-template-columns: 1fr; text-align:center; }
    .hero p.lede{ margin-inline:auto; }
    .hero-actions{ justify-content:center; }
    .hero-addr{ text-align:center; }
    .stamp{ width: min(260px, 62vw); }
    .storia-grid{ grid-template-columns: 1fr; }
    .frasca-rule{ margin-inline:auto; }
    .menu-grid{ grid-template-columns: 1fr; }
    .info-grid{ grid-template-columns: 1fr; }
    .map-frame iframe{ height: 300px; }
  }
  @media (max-width: 720px){
    .nav-links, .nav-cta .btn{ display:none; }
    .nav-toggle{ display:block; }
    header.nav-open .nav-links{
      display:flex; position:absolute; top:100%; left:0; right:0; flex-direction:column; align-items:flex-start;
      background: var(--wine-dark); padding: 24px; gap: 18px; box-shadow: 0 12px 18px rgba(0,0,0,.25);
    }
    header.nav-open .nav-links a{ color: var(--cream-ink); }
  }
</style>
</head>
<body>

<header id="siteHeader">
  <div class="container">
    <nav>
      <a href="#top" class="brand">
        <svg class="brand-mark" viewBox="0 0 100 100" aria-hidden="true">
          <circle cx="50" cy="50" r="45" fill="none" stroke="currentColor" stroke-width="2.5"/>
          <path d="M50 30 L50 62 M38 62 Q50 74 62 62 M40 40 Q50 34 60 40 M40 48 Q50 43 60 48" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round"/>
          <path d="M50 30 Q44 20 34 22 Q42 30 50 30 Q58 30 66 22 Q56 20 50 30" fill="currentColor" opacity=".9"/>
        </svg>
        <span class="brand-text">La Fraschetta<br>di San Paolo<small>Hostaria Romana</small></span>
      </a>
      <ul class="nav-links">
        <li><a href="#storia">La Storia</a></li>
        <li><a href="#menu">Il Menù</a></li>
        <li><a href="#dove-siamo">Dove Siamo</a></li>
      </ul>
      <div class="nav-cta">
        <a href="tel:+390694519425" class="btn btn-dark">Prenota · 06 9451 9425</a>
      </div>
      <button class="nav-toggle" id="navToggle" aria-label="Apri il menu di navigazione" aria-expanded="false">
        <svg width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"><line x1="3" y1="6" x2="21" y2="6"/><line x1="3" y1="12" x2="21" y2="12"/><line x1="3" y1="18" x2="21" y2="18"/></svg>
      </button>
    </nav>
  </div>
</header>

<main id="top">

  <!-- HERO -->
  <section class="hero">
    <div class="container hero-grid">
      <div>
        <p class="eyebrow" style="color:var(--brass)">Hostaria Romana · dal cuore di San Paolo</p>
        <h1>La Fraschetta <em>di San Paolo</em></h1>
        <p class="lede">Salumi tagliati al momento, primi della tradizione romana e vino della casa versato senza fretta — la cucina di sempre, servita con una frasca fuori dalla porta.</p>
        <div class="hero-actions">
          <a href="#menu" class="btn btn-solid">Vedi il Menù</a>
          <a href="tel:+390694519425" class="btn btn-outline">Chiama per Prenotare</a>
          <a href="https://maps.app.goo.gl/P4DwSjSnWuqNNq27A" target="_blank" rel="noopener" class="btn btn-outline">Come Arrivare</a>
        </div>
        <p class="hero-addr">VIA GABRIELLO CHIABRERA 128 · 00145 ROMA &nbsp;—&nbsp; APERTO TUTTI I GIORNI, PRANZO E CENA</p>
      </div>
      <div class="stamp-wrap">
        <svg class="stamp" viewBox="0 0 300 300" role="img" aria-label="Timbro La Fraschetta di San Paolo, Cucina Romana">
          <defs>
            <filter id="rough" x="-20%" y="-20%" width="140%" height="140%">
              <feTurbulence type="fractalNoise" baseFrequency="0.012" numOctaves="2" seed="7" result="noise"/>
              <feDisplacementMap in="SourceGraphic" in2="noise" scale="7"/>
            </filter>
            <path id="ringTop" d="M 34,150 A 116,116 0 0 1 266,150"/>
            <path id="ringBottom" d="M 266,150 A 116,116 0 0 1 34,150"/>
          </defs>
          <g filter="url(#rough)" fill="none" stroke="currentColor">
            <circle cx="150" cy="150" r="134" stroke-width="3"/>
            <circle cx="150" cy="150" r="121" stroke-width="1.2"/>
          </g>
          <text font-family="'Space Mono',monospace" font-size="13.5" letter-spacing="3" fill="currentColor">
            <textPath href="#ringTop" startOffset="50%" text-anchor="middle">LA FRASCHETTA DI SAN PAOLO</textPath>
          </text>
          <text font-family="'Space Mono',monospace" font-size="12.5" letter-spacing="4" fill="currentColor">
            <textPath href="#ringBottom" startOffset="50%" text-anchor="middle">★ CUCINA ROMANA ★ DAL 128 ★</textPath>
          </text>
          <g class="ink" filter="url(#rough)" transform="translate(150,152)" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round">
            <path d="M-20,-42 L-20,18 Q-20,40 0,40 Q20,40 20,18 L20,-42 Z"/>
            <path d="M-20,-30 L20,-30"/>
            <path d="M0,-42 L0,-64"/>
            <path d="M0,-64 Q-16,-76 -32,-70 Q-20,-56 0,-64"/>
            <path d="M0,-64 Q16,-76 32,-70 Q20,-56 0,-64" opacity=".7"/>
            <line x1="-10" y1="52" x2="10" y2="52"/>
          </g>
        </svg>
      </div>
    </div>
  </section>

  <!-- STORIA -->
  <section class="storia" id="storia">
    <div class="container storia-grid">
      <div class="reveal">
        <p class="eyebrow">La Storia</p>
        <h2>Una frasca fuori dalla porta</h2>
        <p class="lead">Il nome "fraschetta" nasce da un'usanza contadina dei Castelli Romani.</p>
        <p>Un tempo, chi aveva del vino nuovo da vendere appendeva un ramo verde — una frasca, appunto — sopra l'ingresso della cantina: un modo semplice per far sapere al vicinato che il vino era pronto, senza bisogno di insegne. Attorno a quel vino sono nate le fraschette: tavoli comuni, salumi affettati al momento, un tagliere condiviso e la cucina povera romana che, di generazione in generazione, è diventata patrimonio di tutti.</p>
        <p>Alla Fraschetta di San Paolo, a due passi dalla Basilica, quello spirito è rimasto lo stesso: porzioni generose, un servizio informale e sincero, e la sensazione — raccontata spesso da chi ci torna — di essere seduti al tavolo di casa più che in un ristorante.</p>
      </div>
      <div class="fact-card reveal">
        <dl>
          <div><dt>Cucina</dt><dd>Romana · Hostaria · Fraschetta</dd></div>
          <hr>
          <div><dt>Zona</dt><dd>San Paolo, a 5 minuti dalla Basilica</dd></div>
          <hr>
          <div><dt>Tavoli</dt><dd>Sala interna e dehors all'aperto</dd></div>
          <hr>
          <div><dt>Aperto</dt><dd>Tutti i giorni, pranzo e cena</dd></div>
        </dl>
      </div>
    </div>
  </section>

  <!-- MENU -->
  <section class="menu" id="menu">
    <div class="container">
      <div class="menu-head reveal">
        <p class="eyebrow">Il Menù</p>
        <h2>Dalla cucina di casa</h2>
      </div>
      <p class="menu-note reveal"><strong>Anteprima</strong> — i piatti qui sotto sono una selezione dei più amati dagli ospiti, in attesa dei testi e dei prezzi definitivi della cucina. Il coperto è di € 2 a persona.</p>

      <div class="menu-grid">

        <div class="menu-section reveal">
          <h3>Antipasti</h3>
          <div class="dish"><div><span class="dish-name">Tagliere della Fraschetta</span><span class="dish-desc">salumi e formaggi locali, sott'oli della casa</span></div><span class="dish-leader"></span><span class="dish-price">€ 14</span></div>
          <div class="dish"><div><span class="dish-name">Bruschette della casa</span><span class="dish-desc">pomodoro fresco, basilico, olio extravergine</span></div><span class="dish-leader"></span><span class="dish-price">€ 7</span></div>
          <div class="dish"><div><span class="dish-name">Fiori di zucca fritti</span><span class="dish-desc">ripieni di mozzarella e alici</span></div><span class="dish-leader"></span><span class="dish-price">€ 8</span></div>
          <div class="dish"><div><span class="dish-name">Supplì al telefono</span><span class="dish-desc">riso, ragù, mozzarella filante — 2 pz</span></div><span class="dish-leader"></span><span class="dish-price">€ 6</span></div>
          <div class="dish"><div><span class="dish-name">Carciofo alla giudia</span><span class="dish-desc">quando disponibile</span></div><span class="dish-leader"></span><span class="dish-price">€ 7</span></div>
        </div>

        <div class="menu-section reveal">
          <h3>Primi</h3>
          <div class="dish"><div><span class="dish-name">Tonnarelli cacio e pepe</span><span class="dish-desc">pecorino romano, pepe macinato al momento</span></div><span class="dish-leader"></span><span class="dish-price">€ 10</span></div>
          <div class="dish"><div><span class="dish-name">Rigatoni alla carbonara</span><span class="dish-desc">guanciale, uovo, pecorino</span></div><span class="dish-leader"></span><span class="dish-price">€ 10</span></div>
          <div class="dish"><div><span class="dish-name">Bucatini all'amatriciana</span><span class="dish-desc">guanciale, pomodoro, pecorino</span></div><span class="dish-leader"></span><span class="dish-price">€ 10</span></div>
          <div class="dish"><div><span class="dish-name">Gricia</span><span class="dish-desc">guanciale e pecorino — la carbonara senza uovo</span></div><span class="dish-leader"></span><span class="dish-price">€ 10</span></div>
          <div class="dish"><div><span class="dish-name">Gnocchi al pomodoro</span><span class="dish-desc">fatti in casa, il giovedì</span></div><span class="dish-leader"></span><span class="dish-price">€ 9</span></div>
        </div>

        <div class="menu-section reveal">
          <h3>Secondi</h3>
          <div class="dish"><div><span class="dish-name">Saltimbocca alla romana</span><span class="dish-desc">vitello, prosciutto crudo, salvia, vino bianco</span></div><span class="dish-leader"></span><span class="dish-price">€ 14</span></div>
          <div class="dish"><div><span class="dish-name">Porchetta di Ariccia</span><span class="dish-desc">servita calda con il suo fondo di cottura</span></div><span class="dish-leader"></span><span class="dish-price">€ 12</span></div>
          <div class="dish"><div><span class="dish-name">Filetto di baccalà</span><span class="dish-desc">pastella leggera, fritto al momento</span></div><span class="dish-leader"></span><span class="dish-price">€ 12</span></div>
          <div class="dish"><div><span class="dish-name">Trippa alla romana</span><span class="dish-desc">pomodoro, mentuccia e pecorino</span></div><span class="dish-leader"></span><span class="dish-price">€ 11</span></div>
          <div class="dish"><div><span class="dish-name">Abbacchio a scottadito</span><span class="dish-desc">costolette di agnello alla brace</span></div><span class="dish-leader"></span><span class="dish-price">€ 16</span></div>
        </div>

        <div class="menu-section reveal">
          <h3>Contorni &amp; Bevande</h3>
          <div class="dish"><div><span class="dish-name">Patate fritte o al forno</span></div><span class="dish-leader"></span><span class="dish-price">€ 5</span></div>
          <div class="dish"><div><span class="dish-name">Puntarelle alla romana</span><span class="dish-desc">alici e aglio</span></div><span class="dish-leader"></span><span class="dish-price">€ 6</span></div>
          <div class="dish"><div><span class="dish-name">Verdure grigliate di stagione</span></div><span class="dish-leader"></span><span class="dish-price">€ 6</span></div>
          <div class="dish"><div><span class="dish-name">Vino della casa</span><span class="dish-desc">bianco o rosso — al litro</span></div><span class="dish-leader"></span><span class="dish-price">€ 10</span></div>
          <div class="dish"><div><span class="dish-name">Birra artigianale</span><span class="dish-desc">33 cl</span></div><span class="dish-leader"></span><span class="dish-price">€ 5</span></div>
        </div>

      </div>
      <p class="menu-foot">Prezzi indicativi e soggetti a conferma · Coperto € 2</p>
    </div>
  </section>

  <!-- DOVE SIAMO -->
  <section class="info" id="dove-siamo">
    <div class="container info-grid">
      <div class="reveal">
        <p class="eyebrow">Dove Siamo</p>
        <h2>Prenota il tuo tavolo</h2>

        <div class="info-line">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M12 21s-7-6.2-7-11.5A7 7 0 0 1 19 9.5C19 14.8 12 21 12 21z"/><circle cx="12" cy="9.5" r="2.5"/></svg>
          <span>Via Gabriello Chiabrera 128, 00145 Roma — 5 minuti a piedi dalla fermata Basilica San Paolo</span>
        </div>
        <div class="info-line">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M22 16.9v3a2 2 0 0 1-2.2 2 19.8 19.8 0 0 1-8.6-3.1 19.5 19.5 0 0 1-6-6 19.8 19.8 0 0 1-3.1-8.6A2 2 0 0 1 4.1 2h3a2 2 0 0 1 2 1.7c.1.9.3 1.8.6 2.7a2 2 0 0 1-.5 2.1L7.9 9.9a16 16 0 0 0 6 6l1.4-1.3a2 2 0 0 1 2.1-.5c.9.3 1.8.5 2.7.6a2 2 0 0 1 1.9 2.2z"/></svg>
          <a href="tel:+390694519425">+39 06 9451 9425</a>
        </div>
        <div class="info-line">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><rect x="3" y="4" width="18" height="17" rx="1.5"/><path d="M3 9h18M8 2v4M16 2v4"/></svg>
          <span>Consigliata la prenotazione, specialmente nel weekend</span>
        </div>

        <table class="hours">
          <tr><td>Pranzo — tutti i giorni</td><td>12:00 – 15:00</td></tr>
          <tr><td>Cena — tutti i giorni</td><td>18:00 – 23:00</td></tr>
        </table>

        <div class="info-actions">
          <a href="tel:+390694519425" class="btn btn-dark">Chiama Ora</a>
          <a href="https://maps.app.goo.gl/P4DwSjSnWuqNNq27A" target="_blank" rel="noopener" class="btn" style="border-color:var(--wine); color:var(--wine)">Apri in Google Maps</a>
        </div>
      </div>

      <div class="map-frame reveal">
        <iframe
          src="https://www.google.com/maps?q=Via+Gabriello+Chiabrera+128,+00145+Roma&output=embed"
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
          title="Mappa — La Fraschetta di San Paolo, Via Gabriello Chiabrera 128, Roma">
        </iframe>
      </div>
    </div>
  </section>

</main>

<footer>
  <div class="container">
    <div class="footer-grid">
      <div class="footer-brand">
        <svg class="brand-mark" viewBox="0 0 100 100" aria-hidden="true">
          <circle cx="50" cy="50" r="45" fill="none" stroke="currentColor" stroke-width="2.5"/>
          <path d="M50 30 L50 62 M38 62 Q50 74 62 62 M40 40 Q50 34 60 40 M40 48 Q50 43 60 48" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round"/>
        </svg>
        <div>
          <strong>La Fraschetta di San Paolo</strong>
          <span>Via Gabriello Chiabrera 128 · 00145 Roma</span>
        </div>
      </div>
      <div class="footer-social">
        <a href="https://www.facebook.com/LaFraschettadiSanPaolo/" target="_blank" rel="noopener">Facebook</a>
        <a href="https://www.instagram.com/lafraschettadisanpaolo/" target="_blank" rel="noopener">Instagram</a>
        <a href="tel:+390694519425">06 9451 9425</a>
      </div>
    </div>
    <div class="footer-bottom">© <span id="year"></span> La Fraschetta di San Paolo — Hostaria Romana</div>
  </div>
</footer>

<script>
  document.getElementById('year').textContent = new Date().getFullYear();

  // sticky header solid background on scroll
  const header = document.getElementById('siteHeader');
  const onScroll = () => header.classList.toggle('solid', window.scrollY > 40);
  onScroll();
  window.addEventListener('scroll', onScroll, { passive:true });

  // mobile nav toggle
  const navToggle = document.getElementById('navToggle');
  navToggle.addEventListener('click', () => {
    const open = header.classList.toggle('nav-open');
    navToggle.setAttribute('aria-expanded', open);
  });
  document.querySelectorAll('.nav-links a').forEach(a=>{
    a.addEventListener('click', () => { header.classList.remove('nav-open'); });
  });

  // reveal on scroll
  const io = new IntersectionObserver((entries)=>{
    entries.forEach(e=>{ if(e.isIntersecting){ e.target.classList.add('in'); io.unobserve(e.target); } });
  }, { threshold: .15 });
  document.querySelectorAll('.reveal').forEach(el=> io.observe(el));
</script>
</body>
</html>
