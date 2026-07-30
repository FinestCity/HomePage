# HomePage
Home Page for Finest City Dog Sitting
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Finest City Home &amp; Pet Sitting</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600;9..144,700&family=Public+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --navy: #14304C;
    --blue-deep: #1F4E79;
    --blue-mid: #3E7CA6;
    --blue-sky: #8FBBD9;
    --blue-mist: #EAF2F8;
    --cream: #F7F5EF;
    --gold: #C99A45;
    --ink: #1C2B36;
    --ink-soft: #4C5D6B;
    --line: #D8E3EC;
  }

  *{ box-sizing: border-box; }

  html{ scroll-behavior: smooth; }

  body{
    margin:0;
    background: var(--cream);
    color: var(--ink);
    font-family: 'Public Sans', sans-serif;
    line-height: 1.6;
  }

  h1, h2, h3{
    font-family: 'Fraunces', serif;
    color: var(--navy);
    margin: 0;
  }

  a{ color: var(--blue-deep); }

  img, svg{ display:block; max-width:100%; }

  /* ---------- Header ---------- */
  header.site{
    background: var(--navy);
    padding: 22px 24px;
    display:flex;
    align-items:center;
    justify-content:center;
    gap: 14px;
  }

  header.site .mark{ width:40px; height:40px; flex-shrink:0; }

  header.site .brand{
    color:#fff;
    font-family:'Fraunces', serif;
    font-size: 1.15rem;
    letter-spacing: 0.04em;
    text-transform: uppercase;
  }

  /* ---------- Hero ---------- */
  .hero{
    max-width: 760px;
    margin: 0 auto;
    padding: 76px 24px 48px;
    text-align:center;
  }

  .hero .eyebrow{
    display:inline-block;
    font-size: 0.78rem;
    letter-spacing: 0.16em;
    text-transform: uppercase;
    color: var(--gold);
    font-weight: 600;
    margin-bottom: 18px;
  }

  .hero h1{
    font-size: clamp(2.1rem, 4.6vw, 3.2rem);
    font-weight: 600;
    line-height: 1.15;
  }

  .hero p.lede{
    margin: 22px auto 0;
    max-width: 560px;
    font-size: 1.08rem;
    color: var(--ink-soft);
  }

  .divider{
    width: 96px;
    height: 34px;
    margin: 34px auto 0;
  }

  /* ---------- Two column section ---------- */
  .columns{
    max-width: 1120px;
    margin: 10px auto 0;
    padding: 20px 24px 80px;
    display:grid;
    grid-template-columns: 1.05fr 0.95fr;
    gap: 40px;
    align-items: start;
  }

  .panel{
    background:#fff;
    border: 1px solid var(--line);
    border-radius: 6px;
    padding: 40px 36px;
  }

  .panel .tag{
    font-size: 0.75rem;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--blue-mid);
    font-weight: 700;
    margin-bottom: 10px;
    display:block;
  }

  .panel h2{
    font-size: 1.55rem;
    font-weight: 600;
    margin-bottom: 18px;
  }

  .panel p{ color: var(--ink-soft); margin: 0 0 16px; }

  .panel p:last-of-type{ margin-bottom: 0; }

  .about-panel{
    background: linear-gradient(180deg, #ffffff 0%, var(--blue-mist) 260%);
  }

  .values-row{
    display:flex;
    gap: 16px;
    margin: 24px 0 26px;
    flex-wrap: wrap;
  }

  .value-chip{
    display:flex;
    align-items:center;
    gap: 8px;
    background: var(--blue-mist);
    border: 1px solid var(--line);
    border-radius: 30px;
    padding: 8px 14px 8px 10px;
    font-size: 0.86rem;
    color: var(--navy);
    font-weight: 600;
  }

  .value-chip svg{ width:18px; height:18px; }

  .service-levels{
    list-style:none;
    margin: 6px 0 0;
    padding:0;
    border-top: 1px solid var(--line);
  }

  .service-levels li{
    display:flex;
    gap: 12px;
    padding: 14px 0;
    border-bottom: 1px solid var(--line);
    align-items:flex-start;
  }

  .service-levels .icon{
    width: 26px;
    height: 26px;
    flex-shrink:0;
    color: var(--blue-deep);
  }

  .service-levels strong{
    display:block;
    color: var(--navy);
    font-size: 0.98rem;
  }

  .service-levels span{
    color: var(--ink-soft);
    font-size: 0.9rem;
  }

  /* ---------- Form panel ---------- */
  .form-panel{
    background: var(--navy);
    color: #fff;
    display:flex;
    flex-direction:column;
  }

  .form-panel .tag{ color: var(--blue-sky); }

  .form-panel h2{ color:#fff; }

  .form-panel p{ color: #C7D6E3; }

  .form-panel .quote-note{
    margin-top: 4px;
    display:flex;
    gap: 10px;
    align-items:flex-start;
    background: rgba(255,255,255,0.06);
    border: 1px solid rgba(255,255,255,0.14);
    border-radius: 6px;
    padding: 14px 16px;
    margin-bottom: 22px;
  }

  .form-panel .quote-note svg{ width:20px; height:20px; flex-shrink:0; color: var(--gold); margin-top:2px; }

  .form-panel .quote-note p{ margin:0; color:#E7EEF4; font-size: 0.92rem; }

  .form-frame-wrap{
    background:#fff;
    border-radius: 6px;
    overflow:hidden;
    flex:1;
  }

  .form-frame-wrap iframe{
    width:100%;
    height: 1250px;
    border:0;
    display:block;
  }

  /* ---------- Footer ---------- */
  footer{
    background: var(--navy);
    padding: 34px 24px 30px;
    text-align:center;
  }

  footer .mark{ width:30px; height:30px; margin:0 auto 12px; opacity:0.85; }

  footer p{
    margin:0;
    color: #A9BFD1;
    font-size: 0.84rem;
    letter-spacing: 0.02em;
  }

  /* ---------- Responsive ---------- */
  @media (max-width: 860px){
    .columns{ grid-template-columns: 1fr; }
    .panel{ padding: 32px 26px; }
  }

  @media (prefers-reduced-motion: reduce){
    html{ scroll-behavior:auto; }
  }
</style>
</head>
<body>

<header class="site">
  <svg class="mark" viewBox="0 0 64 64" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
    <path d="M8 30L32 10L56 30" stroke="#C99A45" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
    <path d="M14 26V52C14 53.1 14.9 54 16 54H48C49.1 54 50 53.1 50 52V26" stroke="#EAF2F8" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
    <path d="M26 54V40C26 38.9 26.9 38 28 38H36C37.1 38 38 38.9 38 40V54" stroke="#EAF2F8" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
    <circle cx="32" cy="27" r="2.6" fill="#8FBBD9"/>
    <path d="M27.5 30.5c0-1.6 2-2.8 4.5-2.8s4.5 1.2 4.5 2.8" stroke="#8FBBD9" stroke-width="2" stroke-linecap="round"/>
  </svg>
  <span class="brand">Finest City Home &amp; Pet Sitting</span>
</header>

<section class="hero">
  <span class="eyebrow">Trusted &middot; Local &middot; Animal-Loving</span>
  <h1>Caring for your home and pets like they're our own</h1>
  <p class="lede">We've been fortunate to help many happy clients feel at ease while they're away &mdash; and we look forward to getting to know you and your pets so we can build a plan that fits your family's individual needs.</p>
  <svg class="divider" viewBox="0 0 96 34" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
    <line x1="0" y1="17" x2="30" y2="17" stroke="#D8E3EC" stroke-width="1.5"/>
    <line x1="66" y1="17" x2="96" y2="17" stroke="#D8E3EC" stroke-width="1.5"/>
    <path d="M40 22c0-5 8-9 8-9s8 4 8 9c0 3-3 5-8 5s-8-2-8-5z" fill="#EAF2F8" stroke="#3E7CA6" stroke-width="1.4"/>
    <circle cx="44.5" cy="19" r="1" fill="#1F4E79"/>
    <circle cx="51.5" cy="19" r="1" fill="#1F4E79"/>
  </svg>
</section>

<section class="columns">

  <div class="panel about-panel">
    <span class="tag">About Us</span>
    <h2>Our background &amp; values</h2>
    <p>Finest City Home &amp; Pet Sitting has helped many families across the area care for the parts of life they treasure most &mdash; their homes and their pets. We know that leaving them in someone else's hands takes trust, and we work hard to earn it every visit.</p>
    <p>Great customer service and clear communication are at the heart of everything we do, alongside a genuine love of animals of every shape, size, and species. If you live outside our usual service area, we're happy to travel to meet your needs &mdash; just ask.</p>

    <div class="values-row">
      <span class="value-chip">
        <svg viewBox="0 0 24 24" fill="none"><path d="M12 20s-7-4.35-9.5-8.5C.9 8.1 2.6 4.5 6 4.5c2 0 3.4 1.2 4.5 2.6C11.6 5.7 13 4.5 15 4.5c3.4 0 5.1 3.6 3.5 7C16 15.65 12 20 12 20z" stroke="#1F4E79" stroke-width="1.6" stroke-linejoin="round"/></svg>
        Animal-loving
      </span>
      <span class="value-chip">
        <svg viewBox="0 0 24 24" fill="none"><path d="M4 12l1.5-1.5M20 12l-1.5-1.5M12 4v2M6.5 6.5L8 8M17.5 6.5L16 8M8 20h8M9 16h6" stroke="#1F4E79" stroke-width="1.6" stroke-linecap="round"/><circle cx="12" cy="12" r="4" stroke="#1F4E79" stroke-width="1.6"/></svg>
        Clear communication
      </span>
      <span class="value-chip">
        <svg viewBox="0 0 24 24" fill="none"><path d="M3 12l9-8 9 8M6 10v9a1 1 0 001 1h10a1 1 0 001-1v-9" stroke="#1F4E79" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"/></svg>
        Home &amp; pet care
      </span>
      <span class="value-chip">
        <svg viewBox="0 0 24 24" fill="none"><path d="M12 21s-6-4.35-9-8.5C0.5 8 2.5 4 6.5 4c2 0 3.6 1.4 5.5 3.6C13.9 5.4 15.5 4 17.5 4c4 0 6 4 3.5 8.5-3 4.15-9 8.5-9 8.5z" stroke="#1F4E79" stroke-width="1.6"/></svg>
        Will travel to you
      </span>
    </div>

    <p>We're full service and glad to cover it all &mdash; but we also offer flexible levels of care, so you only pay for what you actually need:</p>

    <ul class="service-levels">
      <li>
        <svg class="icon" viewBox="0 0 24 24" fill="none"><path d="M12 21s-7-4.4-9-9c-1.4-3.3.5-6.8 4-6.8 2 0 3.6 1.3 5 3.3 1.4-2 3-3.3 5-3.3 3.5 0 5.4 3.5 4 6.8-2 4.6-9 9-9 9z" stroke="currentColor" stroke-width="1.5"/></svg>
        <div><strong>Drop-in visits</strong><span>A quick, friendly check-in to feed, refresh water, and give some love.</span></div>
      </li>
      <li>
        <svg class="icon" viewBox="0 0 24 24" fill="none"><path d="M4 19c3-1 5-3 5-6M10 13c2 0 4-2 4-5M4 19l6-6M14 8l6-6M18 4l2 2-4 4" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
        <div><strong>Walks &amp; feeding</strong><span>Regular walks paired with reliable feeding on your pet's own schedule.</span></div>
      </li>
      <li>
        <svg class="icon" viewBox="0 0 24 24" fill="none"><path d="M21 12.8A9 9 0 1111.2 3a7 7 0 009.8 9.8z" stroke="currentColor" stroke-width="1.5" stroke-linejoin="round"/></svg>
        <div><strong>Overnight stays</strong><span>Full overnight care in your home, so pets keep their normal routine.</span></div>
      </li>
    </ul>
  </div>

  <div class="panel form-panel">
    <span class="tag">Get Started</span>
    <h2>Interested in working with us?</h2>
    <p>Please complete the form below and we'll reach out about your request as soon as possible, price quote included.</p>

    <div class="quote-note">
      <svg viewBox="0 0 24 24" fill="none"><path d="M12 8v5M12 16h.01" stroke="currentColor" stroke-width="1.8" stroke-linecap="round"/><circle cx="12" cy="12" r="9" stroke="currentColor" stroke-width="1.6"/></svg>
      <p>Tell us a bit about your home, your pets, and the dates you need &mdash; we'll follow up with a personalized quote.</p>
    </div>

    <div class="form-frame-wrap">
      <iframe src="https://docs.google.com/forms/d/e/1FAIpQLSfia2F5rLv3LVewZrP3mLKf1y4nZosVl1c1Z0Zo-WYzMNF2NA/viewform?embedded=true" title="Finest City Home & Pet Sitting request form">Loading form&hellip;</iframe>
    </div>
  </div>

</section>

<footer>
  <svg class="mark" viewBox="0 0 64 64" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
    <path d="M8 30L32 10L56 30" stroke="#C99A45" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
    <path d="M14 26V52C14 53.1 14.9 54 16 54H48C49.1 54 50 53.1 50 52V26" stroke="#EAF2F8" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
  </svg>
  <p>Finest City Home &amp; Pet Sitting &mdash; caring for your home and your best friends.</p>
</footer>

</body>
</html>
