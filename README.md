<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>João Santana Advogados Associados | Advocacia Especializada</title>
<meta name="description" content="Escritório de advocacia com atuação em Direito Imobiliário, Empresarial, Sucessões, Cível e Consumidor. Atendimento personalizado em Belo Horizonte - MG.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;0,700;1,300;1,400&family=Outfit:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --gold: #E8A020;
    --gold-light: #F0B84A;
    --gold-pale: #FBF0DC;
    --dark: #1A1A1A;
    --gray: #6B6B6B;
    --light: #F8F6F2;
    --white: #FFFFFF;
    --border: rgba(232,160,32,0.2);
  }
  * { margin: 0; padding: 0; box-sizing: border-box; }
  html { scroll-behavior: smooth; }
  body { font-family: 'Outfit', sans-serif; background: var(--white); color: var(--dark); overflow-x: hidden; }

  /* NAV */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 1000;
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 5vw; height: 72px;
    background: rgba(255,255,255,0.98);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
    transition: box-shadow .3s;
  }
  nav.scrolled { box-shadow: 0 4px 32px rgba(0,0,0,0.08); }
  .nav-logo { display: flex; align-items: center; gap: 14px; text-decoration: none; }
  .nav-logo-icon {
    width: 48px; height: 48px; background: var(--gold); border-radius: 10px;
    display: flex; align-items: center; justify-content: center;
    font-family: 'Cormorant Garamond', serif; font-size: 22px; font-weight: 700;
    color: white; letter-spacing: -1px; flex-shrink: 0;
  }
  .nav-logo-name { font-weight: 600; font-size: 15px; color: var(--dark); letter-spacing: 0.5px; line-height: 1.2; }
  .nav-logo-sub { font-size: 10px; font-weight: 400; color: var(--gold); letter-spacing: 2px; text-transform: uppercase; }
  .nav-links { display: flex; gap: 36px; list-style: none; }
  .nav-links a { text-decoration: none; font-size: 13px; font-weight: 500; color: var(--gray); letter-spacing: 0.5px; transition: color .2s; }
  .nav-links a:hover { color: var(--gold); }
  .nav-cta {
    background: var(--gold); color: white; padding: 10px 24px; border-radius: 6px;
    font-size: 13px; font-weight: 600; text-decoration: none; letter-spacing: 0.5px;
    transition: background .2s, transform .15s; white-space: nowrap;
  }
  .nav-cta:hover { background: #c8891a; transform: translateY(-1px); }

  /* HAMBURGER */
  .hamburger {
    display: none; flex-direction: column; justify-content: center;
    gap: 6px; cursor: pointer; padding: 8px; background: none; border: none;
    width: 40px; height: 40px;
  }
  .hamburger span {
    display: block; width: 24px; height: 2px;
    background: var(--dark); border-radius: 2px;
    transition: transform .3s, opacity .3s;
    transform-origin: center;
  }
  .hamburger.open span:nth-child(1) { transform: translateY(8px) rotate(45deg); }
  .hamburger.open span:nth-child(2) { opacity: 0; transform: scaleX(0); }
  .hamburger.open span:nth-child(3) { transform: translateY(-8px) rotate(-45deg); }

  /* MOBILE MENU */
  .mobile-menu {
    display: none; position: fixed; top: 72px; left: 0; right: 0;
    background: #1A1A1A; z-index: 999;
    flex-direction: column; padding: 24px 6vw 32px;
    gap: 0; border-top: 1px solid rgba(232,160,32,0.2);
    box-shadow: 0 20px 40px rgba(0,0,0,0.4);
  }
  .mobile-menu.open { display: flex; }
  .mobile-menu a {
    text-decoration: none; font-size: 16px; font-weight: 400;
    color: rgba(255,255,255,0.8); padding: 14px 0;
    border-bottom: 1px solid rgba(255,255,255,0.08);
    transition: color .2s;
  }
  .mobile-menu a:hover { color: var(--gold); }
  .mobile-menu a.mobile-cta {
    margin-top: 20px; background: var(--gold); color: white;
    padding: 14px 24px; border-radius: 8px; text-align: center;
    font-weight: 600; border: none;
  }

  /* HERO */
  .hero {
    min-height: 100vh; background: var(--dark);
    display: grid; grid-template-columns: 1fr 1fr;
    position: relative; overflow: hidden; padding-top: 72px;
  }
  .hero-bg-pattern {
    position: absolute; inset: 0; pointer-events: none;
    background-image:
      radial-gradient(circle at 70% 30%, rgba(232,160,32,0.12) 0%, transparent 50%),
      radial-gradient(circle at 20% 80%, rgba(232,160,32,0.06) 0%, transparent 40%);
  }
  .hero-lines {
    position: absolute; inset: 0; pointer-events: none;
    background-image: repeating-linear-gradient(90deg, rgba(255,255,255,0.02) 0px, rgba(255,255,255,0.02) 1px, transparent 1px, transparent 80px);
  }
  .hero-content {
    display: flex; flex-direction: column; justify-content: center;
    padding: 80px 5vw 80px 8vw; position: relative; z-index: 2;
  }
  .hero-badge {
    display: inline-flex; align-items: center; gap: 8px;
    background: rgba(232,160,32,0.15); border: 1px solid rgba(232,160,32,0.3);
    color: var(--gold-light); padding: 6px 16px; border-radius: 40px;
    font-size: 11px; font-weight: 600; letter-spacing: 2px;
    text-transform: uppercase; margin-bottom: 32px; width: fit-content;
  }
  .hero-badge::before { content: ''; width: 6px; height: 6px; background: var(--gold); border-radius: 50%; }
  .hero-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(38px, 4.5vw, 64px); font-weight: 300;
    line-height: 1.15; color: white; margin-bottom: 24px;
  }
  .hero-title em { font-style: italic; color: var(--gold-light); }
  .hero-title strong { font-weight: 700; }
  .hero-desc {
    font-size: 15px; font-weight: 300; color: rgba(255,255,255,0.65);
    line-height: 1.8; max-width: 480px; margin-bottom: 48px;
  }
  .hero-actions { display: flex; gap: 16px; flex-wrap: wrap; }
  .btn-ghost {
    border: 1px solid rgba(255,255,255,0.2); color: rgba(255,255,255,0.8);
    padding: 15px 32px; border-radius: 8px; font-size: 14px; font-weight: 400;
    text-decoration: none; letter-spacing: 0.5px; transition: border-color .2s, color .2s;
  }
  .btn-ghost:hover { border-color: var(--gold); color: var(--gold-light); }
  .hero-stats {
    display: flex; gap: 40px; margin-top: 64px;
    padding-top: 40px; border-top: 1px solid rgba(255,255,255,0.1);
  }
  .stat-num { font-family: 'Cormorant Garamond', serif; font-size: 40px; font-weight: 700; color: var(--gold); line-height: 1; }
  .stat-label { font-size: 12px; color: rgba(255,255,255,0.5); letter-spacing: 1px; text-transform: uppercase; margin-top: 4px; }
  .hero-image { position: relative; overflow: hidden; }
  .hero-image::before {
    content: ''; position: absolute; left: 0; top: 0; bottom: 0; width: 60px;
    background: linear-gradient(90deg, var(--dark), transparent); z-index: 2;
  }
  .hero-image img { width: 100%; height: 100%; object-fit: cover; object-position: center top; }
  .hero-image-overlay { position: absolute; inset: 0; background: linear-gradient(135deg, rgba(26,26,26,0.3) 0%, transparent 60%); z-index: 1; }

  /* SECTION BASE */
  section { padding: 100px 8vw; }
  .section-tag { font-size: 11px; font-weight: 600; letter-spacing: 3px; text-transform: uppercase; color: var(--gold); margin-bottom: 16px; }
  .section-title { font-family: 'Cormorant Garamond', serif; font-size: clamp(30px, 3.5vw, 50px); font-weight: 400; line-height: 1.2; color: var(--dark); margin-bottom: 20px; }
  .section-title em { font-style: italic; color: var(--gold); }

  /* AREAS */
  .areas { background: var(--light); }
  .areas-header { max-width: 640px; margin-bottom: 64px; }
  .areas-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 2px; }
  .areas-grid .area-card:first-child { grid-column: span 2; }
  .area-card {
    background: white; padding: 48px 40px; position: relative; overflow: hidden;
    cursor: default; transition: background .3s;
  }
  .area-card:hover { background: var(--dark); }
  .area-card:hover .area-icon { background: rgba(232,160,32,0.15); color: var(--gold); }
  .area-card:hover .area-name { color: white; }
  .area-card:hover .area-desc { color: rgba(255,255,255,0.6); }
  .area-card:hover .area-line { background: var(--gold); }
  .area-number { font-family: 'Cormorant Garamond', serif; font-size: 11px; color: var(--gold); letter-spacing: 2px; margin-bottom: 24px; }
  .area-icon { width: 48px; height: 48px; background: var(--gold-pale); border-radius: 10px; display: flex; align-items: center; justify-content: center; font-size: 22px; margin-bottom: 24px; transition: .3s; }
  .area-name { font-family: 'Cormorant Garamond', serif; font-size: 26px; font-weight: 600; color: var(--dark); line-height: 1.2; margin-bottom: 16px; transition: color .3s; }
  .area-line { width: 32px; height: 2px; background: var(--gold); margin-bottom: 20px; transition: .3s; }
  .area-desc { font-size: 14px; font-weight: 300; color: var(--gray); line-height: 1.75; transition: color .3s; }

  /* ABOUT */
  .about { display: grid; grid-template-columns: 1fr 1fr; gap: 80px; align-items: center; padding: 100px 8vw; }
  .about-image-wrap { position: relative; }
  .about-img { width: 100%; aspect-ratio: 4/5; object-fit: cover; object-position: center top; border-radius: 4px; }
  .about-accent { position: absolute; bottom: -24px; right: -24px; width: 200px; height: 200px; border: 2px solid var(--gold); border-radius: 4px; z-index: -1; }
  .about-tag-block {
    position: absolute; top: 32px; left: -32px;
    background: var(--gold); padding: 20px 24px; border-radius: 4px;
    color: white; text-align: center; box-shadow: 0 8px 32px rgba(232,160,32,0.4);
  }
  .about-tag-num { font-family: 'Cormorant Garamond', serif; font-size: 42px; font-weight: 700; line-height: 1; }
  .about-tag-text { font-size: 11px; letter-spacing: 1px; opacity: 0.85; }
  .about-text { font-size: 15px; font-weight: 300; color: var(--gray); line-height: 1.9; margin-bottom: 40px; }
  .about-pillars { display: flex; flex-direction: column; gap: 20px; }
  .pillar { display: flex; gap: 16px; align-items: flex-start; padding: 16px 20px; background: var(--light); border-radius: 8px; border-left: 3px solid var(--gold); }
  .pillar-icon { font-size: 20px; flex-shrink: 0; }
  .pillar-title { font-weight: 600; font-size: 14px; color: var(--dark); }
  .pillar-text { font-size: 13px; color: var(--gray); margin-top: 2px; font-weight: 300; }

  /* TESTIMONIALS */
  .testimonials { background: var(--dark); color: white; }
  .testimonials .section-title { color: white; }
  .testimonials-header { display: flex; justify-content: space-between; align-items: flex-end; margin-bottom: 32px; flex-wrap: wrap; gap: 24px; }
  .review-avg { font-family: 'Cormorant Garamond', serif; font-size: 52px; font-weight: 700; color: var(--gold); line-height: 1; }
  .review-label { font-size: 12px; color: rgba(255,255,255,0.4); margin-top: 4px; }
  .stars { color: var(--gold); font-size: 18px; letter-spacing: 2px; }
  .google-badge {
    display: flex; align-items: center; gap: 20px; margin-bottom: 36px;
    padding: 16px 24px; background: rgba(255,255,255,0.05);
    border: 1px solid rgba(255,255,255,0.08); border-radius: 10px; flex-wrap: wrap;
  }
  .testimonials-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px; }
  .tcard {
    background: rgba(255,255,255,0.05); border: 1px solid rgba(255,255,255,0.08);
    border-radius: 12px; padding: 32px 28px; transition: border-color .3s, background .3s;
  }
  .tcard:hover { border-color: rgba(232,160,32,0.4); background: rgba(232,160,32,0.05); }
  .tcard-quote { font-family: 'Cormorant Garamond', serif; font-size: 48px; line-height: 1; color: var(--gold); margin-bottom: 16px; font-style: italic; }
  .tcard-text { font-size: 14px; font-weight: 300; color: rgba(255,255,255,0.75); line-height: 1.75; margin-bottom: 24px; }
  .tcard-author { display: flex; align-items: center; gap: 12px; }
  .tcard-avatar { width: 40px; height: 40px; border-radius: 50%; background: linear-gradient(135deg, var(--gold), #c8891a); display: flex; align-items: center; justify-content: center; font-family: 'Cormorant Garamond', serif; font-size: 16px; font-weight: 700; color: white; flex-shrink: 0; }
  .tcard-name { font-size: 14px; font-weight: 500; color: white; }
  .tcard-date { font-size: 12px; color: rgba(255,255,255,0.35); margin-top: 2px; }

  /* IMAGE BANNER */
  .img-banner { height: 340px; overflow: hidden; position: relative; }
  .img-banner img { width: 100%; height: 100%; object-fit: cover; object-position: center 40%; filter: brightness(0.45) grayscale(20%); }
  .img-banner-overlay { position: absolute; inset: 0; display: flex; flex-direction: column; align-items: center; justify-content: center; text-align: center; padding: 0 20px; }
  .img-banner-quote { font-family: 'Cormorant Garamond', serif; font-size: clamp(22px,3.5vw,44px); color: white; font-weight: 300; line-height: 1.4; max-width: 760px; }
  .img-banner-quote em { color: var(--gold-light); font-style: italic; }
  .img-banner-btn { margin-top: 32px; background: var(--gold); color: white; padding: 14px 36px; border-radius: 8px; font-size: 14px; font-weight: 600; text-decoration: none; letter-spacing: .5px; box-shadow: 0 4px 20px rgba(232,160,32,0.5); transition: background .2s, transform .15s; }
  .img-banner-btn:hover { background: #c8891a; transform: translateY(-2px); }

  /* CONTACT */
  .contact { background: var(--light); }
  .contact-inner { display: grid; grid-template-columns: 1fr 1fr; gap: 80px; align-items: start; }
  .contact-block { margin-bottom: 36px; }
  .contact-block-label { font-size: 11px; letter-spacing: 2px; text-transform: uppercase; color: var(--gold); font-weight: 600; margin-bottom: 8px; }
  .contact-block-value { font-size: 15px; color: var(--dark); font-weight: 400; line-height: 1.6; }
  .contact-block-value a { color: var(--dark); text-decoration: none; transition: color .2s; }
  .contact-block-value a:hover { color: var(--gold); }
  .contact-cta-box { background: var(--dark); border-radius: 16px; padding: 48px 40px; color: white; }
  .contact-cta-title { font-family: 'Cormorant Garamond', serif; font-size: 32px; font-weight: 400; margin-bottom: 16px; line-height: 1.3; }
  .contact-cta-title em { color: var(--gold); font-style: italic; }
  .contact-cta-text { font-size: 14px; color: rgba(255,255,255,0.6); margin-bottom: 32px; font-weight: 300; line-height: 1.7; }
  .whatsapp-btn { display: inline-flex; align-items: center; gap: 10px; background: #25D366; color: white; padding: 14px 28px; border-radius: 8px; font-size: 15px; font-weight: 600; text-decoration: none; transition: background .2s, transform .15s; box-shadow: 0 4px 20px rgba(37,211,102,0.3); }
  .whatsapp-btn:hover { background: #1db954; transform: translateY(-2px); }
  .map-placeholder { margin-top: 32px; border-radius: 12px; overflow: hidden; height: 220px; background: #e5e5e5; }
  .map-placeholder iframe { width: 100%; height: 100%; border: none; }

  /* FOOTER */
  footer { background: var(--dark); color: rgba(255,255,255,0.4); padding: 28px 8vw; display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 16px; border-top: 1px solid rgba(255,255,255,0.06); }
  footer p { font-size: 12px; }
  .footer-logo-text { font-family: 'Cormorant Garamond', serif; font-size: 16px; font-weight: 600; color: rgba(255,255,255,0.6); }

  /* ANIMATIONS */
  @keyframes fadeUp { from { opacity: 0; transform: translateY(30px); } to { opacity: 1; transform: translateY(0); } }

  /* RESPONSIVE */
  @media (max-width: 1024px) {
    .areas-grid { grid-template-columns: 1fr 1fr; }
    .areas-grid .area-card:first-child { grid-column: span 1; }
    .testimonials-grid { grid-template-columns: 1fr 1fr; }
  }
  @media (max-width: 768px) {
    .nav-links, .nav-cta { display: none; }
    .hamburger { display: flex; }
    .hero { grid-template-columns: 1fr; min-height: auto; }
    .hero-image { display: none; }
    .hero-content { padding: 60px 6vw; }
    .hero-stats { gap: 24px; }
    .about { grid-template-columns: 1fr; gap: 40px; padding: 60px 6vw; }
    .about-accent { display: none; }
    .about-tag-block { left: 16px; top: 16px; }
    .areas { padding: 60px 6vw; }
    .areas-grid { grid-template-columns: 1fr; }
    .area-card { padding: 36px 28px; }
    .testimonials-grid { grid-template-columns: 1fr; }
    section { padding: 60px 6vw; }
    .contact-inner { grid-template-columns: 1fr; gap: 40px; }
    footer { flex-direction: column; text-align: center; }
    .img-banner { height: 280px; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav id="nav">
  <a href="#" class="nav-logo">
    <div class="nav-logo-icon">JS</div>
    <div>
      <div class="nav-logo-name">João Santana</div>
      <div class="nav-logo-sub">Advogados Associados</div>
    </div>
  </a>

  <ul class="nav-links">
    <li><a href="#areas">Áreas</a></li>
    <li><a href="#sobre">Sobre</a></li>
    <li><a href="#depoimentos">Depoimentos</a></li>
    <li><a href="#contato">Contato</a></li>
  </ul>

  <a href="https://wa.me/5531997177002" class="nav-cta" target="_blank" rel="noopener noreferrer">Fale Conosco</a>

  <button class="hamburger" id="hamburger" aria-label="Menu" onclick="toggleMenu()">
    <span></span>
    <span></span>
    <span></span>
  </button>
</nav>

<!-- MOBILE MENU -->
<div class="mobile-menu" id="mobileMenu">
  <a href="#areas" onclick="closeMenu()">Áreas de Atuação</a>
  <a href="#sobre" onclick="closeMenu()">Sobre Nós</a>
  <a href="#depoimentos" onclick="closeMenu()">Depoimentos</a>
  <a href="#contato" onclick="closeMenu()">Contato</a>
  <a href="https://wa.me/5531997177002" class="mobile-cta" target="_blank" rel="noopener noreferrer">💬 Falar pelo WhatsApp</a>
</div>

<!-- HERO -->
<section class="hero">
  <div class="hero-bg-pattern"></div>
  <div class="hero-lines"></div>
  <div class="hero-content">
    <div class="hero-badge">Escritório de Advocacia</div>
    <h1 class="hero-title">
      Protegendo Seus <em>Direitos,</em><br>
      <strong>Construindo Seu Futuro.</strong>
    </h1>
    <p class="hero-desc">
      Com um time de advogados especializados e mais de 8 anos de experiência, nosso escritório lidera com excelência em Direito Imobiliário, Cível, Consumidor, Empresarial e Sucessões. Estamos aqui para defender seus direitos e interesses.
    </p>
    <div class="hero-actions">
      <a href="#areas" class="btn-ghost">Nossas Áreas</a>
    </div>
    <div class="hero-stats">
      <div>
        <div class="stat-num">8+</div>
        <div class="stat-label">Anos de Experiência</div>
      </div>
      <div>
        <div class="stat-num">5</div>
        <div class="stat-label">Áreas de Atuação</div>
      </div>
      <div>
        <div class="stat-num">5★</div>
        <div class="stat-label">Avaliação Google</div>
      </div>
    </div>
  </div>
  <div class="hero-image">
    <div class="hero-image-overlay"></div>
    <img
      src="https://images.pexels.com/photos/5668858/pexels-photo-5668858.jpeg?auto=compress&cs=tinysrgb&w=900"
      alt="Escritório de Advocacia João Santana"
      loading="eager"
      onerror="this.src='https://images.pexels.com/photos/159832/justice-law-case-hearing-159832.jpeg?auto=compress&cs=tinysrgb&w=900'">
  </div>
</section>

<!-- ÁREAS DE ATUAÇÃO -->
<section class="areas" id="areas">
  <div class="areas-header">
    <div class="section-tag">Nossas Especialidades</div>
    <h2 class="section-title">Soluções Jurídicas Abrangentes para Atender às Suas <em>Necessidades.</em></h2>
  </div>
  <div class="areas-grid">
    <div class="area-card">
      <div class="area-number">01</div>
      <div class="area-icon">🏠</div>
      <div class="area-name">Direito Imobiliário</div>
      <div class="area-line"></div>
      <p class="area-desc">Da negociação de contratos à resolução de litígios, nosso conhecimento profundo do mercado imobiliário assegura a proteção e o sucesso de nossos clientes.</p>
    </div>
    <div class="area-card">
      <div class="area-number">02</div>
      <div class="area-icon">🏛️</div>
      <div class="area-name">Direito Empresarial</div>
      <div class="area-line"></div>
      <p class="area-desc">Consultoria e suporte jurídico para empresas, cobrindo desde a formação até a consultoria em operações diárias e questões complexas.</p>
    </div>
    <div class="area-card">
      <div class="area-number">03</div>
      <div class="area-icon">⚖️</div>
      <div class="area-name">Direito de Sucessões</div>
      <div class="area-line"></div>
      <p class="area-desc">Assistência em planejamento sucessório e litígios, garantindo a proteção do patrimônio e a transmissão de legados de acordo com a vontade de nossos clientes.</p>
    </div>
    <div class="area-card">
      <div class="area-number">04</div>
      <div class="area-icon">📋</div>
      <div class="area-name">Direito Cível</div>
      <div class="area-line"></div>
      <p class="area-desc">Representação legal excepcional em disputas cíveis, incluindo questões contratuais, responsabilidade civil e direitos de propriedade, assegurando a defesa eficaz dos seus direitos.</p>
    </div>
    <div class="area-card">
      <div class="area-number">05</div>
      <div class="area-icon">🛡️</div>
      <div class="area-name">Direito do Consumidor</div>
      <div class="area-line"></div>
      <p class="area-desc">Defendemos os direitos dos consumidores, lidando com práticas injustas e litígios de consumo, buscando justiça e compensações adequadas.</p>
    </div>
  </div>
</section>

<!-- SOBRE NÓS -->
<section class="about" id="sobre">
  <div class="about-image-wrap">
    <img
      class="about-img"
      src="https://images.pexels.com/photos/5669619/pexels-photo-5669619.jpeg?auto=compress&cs=tinysrgb&w=700"
      alt="Equipe de advogados João Santana"
      onerror="this.src='https://images.pexels.com/photos/4427611/pexels-photo-4427611.jpeg?auto=compress&cs=tinysrgb&w=700'">
    <div class="about-accent"></div>
    <div class="about-tag-block">
      <div class="about-tag-num">2016</div>
      <div class="about-tag-text">Fundado em</div>
    </div>
  </div>
  <div>
    <div class="section-tag">Sobre Nós</div>
    <h2 class="section-title">João Santana Junior<br><em>Sociedade de Advogados</em></h2>
    <p class="about-text">
      Somos uma equipe de advogados dedicados e apaixonados por justiça e excelência no atendimento jurídico. Fundado em 2016, nosso escritório tem se destacado pela abordagem personalizada e pelo comprometimento em oferecer soluções jurídicas eficientes e inovadoras em diversas áreas do Direito.
      <br><br>
      Com forte ênfase em Direito Imobiliário, Cível, do Consumidor, Empresarial e de Sucessões, nossa missão é simplificar o complexo mundo jurídico para nossos clientes, protegendo seus interesses e contribuindo para o seu sucesso. Cada membro da nossa equipe traz uma riqueza de conhecimento e experiência, garantindo uma representação legal de alta qualidade e estratégias vencedoras.
    </p>
    <div class="about-pillars">
      <div class="pillar">
        <div class="pillar-icon">🎯</div>
        <div>
          <div class="pillar-title">Abordagem Personalizada</div>
          <div class="pillar-text">Cada cliente recebe atenção individualizada e estratégias sob medida para o seu caso.</div>
        </div>
      </div>
      <div class="pillar">
        <div class="pillar-icon">💡</div>
        <div>
          <div class="pillar-title">Soluções Inovadoras</div>
          <div class="pillar-text">Unimos experiência jurídica sólida com métodos modernos e eficientes.</div>
        </div>
      </div>
      <div class="pillar">
        <div class="pillar-icon">🤝</div>
        <div>
          <div class="pillar-title">Compromisso com Resultados</div>
          <div class="pillar-text">Trabalhamos incansavelmente para proteger seus direitos e alcançar o melhor desfecho.</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- DEPOIMENTOS -->
<section class="testimonials" id="depoimentos">
  <div class="testimonials-header">
    <div>
      <div class="section-tag">Depoimentos</div>
      <h2 class="section-title">O que nossos clientes<br><em>dizem sobre nós</em></h2>
    </div>
    <div style="text-align:right">
      <div class="review-avg">5,0</div>
      <div class="stars">★★★★★</div>
      <div class="review-label">Avaliação no Google</div>
      <a href="https://www.google.com/search?q=jo%C3%A3o+santana+junior+advocacia+belo+horizonte" target="_blank" rel="noopener noreferrer"
        style="display:inline-flex;align-items:center;gap:8px;margin-top:12px;border:1px solid rgba(232,160,32,0.35);color:#F0B84A;padding:7px 16px;border-radius:6px;font-size:11px;font-weight:500;text-decoration:none;letter-spacing:1px;text-transform:uppercase;">
        Ver no Google
      </a>
    </div>
  </div>

  <div class="google-badge">
    <svg width="60" height="20" viewBox="0 0 272 92" xmlns="http://www.w3.org/2000/svg">
      <path d="M115.75 47.18c0 12.77-9.99 22.18-22.25 22.18s-22.25-9.41-22.25-22.18C71.25 34.32 81.24 25 93.5 25s22.25 9.32 22.25 22.18zm-9.74 0c0-7.98-5.79-13.44-12.51-13.44S80.99 39.2 80.99 47.18c0 7.9 5.79 13.44 12.51 13.44s12.51-5.55 12.51-13.44z" fill="rgba(255,255,255,0.6)"/>
      <path d="M163.75 47.18c0 12.77-9.99 22.18-22.25 22.18s-22.25-9.41-22.25-22.18c0-12.85 9.99-22.18 22.25-22.18s22.25 9.32 22.25 22.18zm-9.74 0c0-7.98-5.79-13.44-12.51-13.44s-12.51 5.46-12.51 13.44c0 7.9 5.79 13.44 12.51 13.44s12.51-5.55 12.51-13.44z" fill="rgba(255,255,255,0.6)"/>
      <path d="M225 3v65h-9.5V3h9.5z" fill="rgba(255,255,255,0.6)"/>
      <path d="M35.29 41.41V32H67c.31 1.64.47 3.58.47 5.68 0 7.06-1.93 15.79-8.15 22.01-6.05 6.3-13.78 9.66-24.02 9.66C16.32 69.35.36 53.89.36 34.91.36 15.93 16.32.47 35.3.47c10.5 0 17.98 4.12 23.6 9.49l-6.64 6.64c-4.03-3.78-9.49-6.72-16.97-6.72-13.86 0-24.7 11.17-24.7 25.03 0 13.86 10.84 25.03 24.7 25.03 8.99 0 14.11-3.61 17.39-6.89 2.66-2.66 4.41-6.46 5.1-11.65l-22.49.01z" fill="rgba(255,255,255,0.6)"/>
    </svg>
    <div style="width:1px;height:28px;background:rgba(255,255,255,0.1)"></div>
    <span style="color:#E8A020;font-size:20px;letter-spacing:2px;">★★★★★</span>
    <span style="font-family:'Cormorant Garamond',serif;font-size:26px;font-weight:700;color:#E8A020;">5,0</span>
    <span style="font-size:13px;color:rgba(255,255,255,0.4);">· 7 avaliações verificadas</span>
  </div>

  <div class="testimonials-grid">
    <div class="tcard">
      <div class="tcard-quote">"</div>
      <p class="tcard-text">Profissionais muito atenciosos e esclarecem as dúvidas com rapidez. Recomendo a todos.</p>
      <div class="tcard-author">
        <div class="tcard-avatar">D</div>
        <div><div class="tcard-name">Desiree Moura da Silva</div><div class="tcard-date">01/04/2024</div></div>
      </div>
    </div>
    <div class="tcard">
      <div class="tcard-quote">"</div>
      <p class="tcard-text">Ótimo advogado!!!</p>
      <div class="tcard-author">
        <div class="tcard-avatar">I</div>
        <div><div class="tcard-name">Isis Tande</div><div class="tcard-date">26/03/2024</div></div>
      </div>
    </div>
    <div class="tcard">
      <div class="tcard-quote">"</div>
      <p class="tcard-text">Excelente atendimento, pessoas extremamente capacitadas! Super satisfeita!</p>
      <div class="tcard-author">
        <div class="tcard-avatar">D</div>
        <div><div class="tcard-name">Danielle Soares dos Santos</div><div class="tcard-date">19/03/2024</div></div>
      </div>
    </div>
    <div class="tcard">
      <div class="tcard-quote">"</div>
      <p class="tcard-text">Ótimo profissional! Explica tudo muito certo, esclarece todas as dúvidas.</p>
      <div class="tcard-author">
        <div class="tcard-avatar">M</div>
        <div><div class="tcard-name">Mauricio Bettone</div><div class="tcard-date">08/03/2024</div></div>
      </div>
    </div>
    <div class="tcard">
      <div class="tcard-quote">"</div>
      <p class="tcard-text">Excelente profissional esclareceu todas as minhas dúvidas e muito atuante, eu indico com certeza.</p>
      <div class="tcard-author">
        <div class="tcard-avatar">F</div>
        <div><div class="tcard-name">Fernando Rocha</div><div class="tcard-date">06/03/2024</div></div>
      </div>
    </div>
    <div class="tcard">
      <div class="tcard-quote">"</div>
      <p class="tcard-text">O fato de ser atencioso e com profundo conhecimento jurídico nos traz maior tranquilidade para concluir as negociações.</p>
      <div class="tcard-author">
        <div class="tcard-avatar">L</div>
        <div><div class="tcard-name">Luiz Schumann</div><div class="tcard-date">05/03/2024</div></div>
      </div>
    </div>
    <div class="tcard">
      <div class="tcard-quote">"</div>
      <p class="tcard-text">Excelente profissional, tirou todas as minhas dúvidas, está atuando bem presente no meu caso.</p>
      <div class="tcard-author">
        <div class="tcard-avatar">M</div>
        <div><div class="tcard-name">Maria Luiza</div><div class="tcard-date">05/03/2024</div></div>
      </div>
    </div>
  </div>
</section>

<!-- IMAGE BANNER -->
<div class="img-banner">
  <img
    src="https://images.pexels.com/photos/5668772/pexels-photo-5668772.jpeg?auto=compress&cs=tinysrgb&w=1600"
    alt="Compromisso com a justiça"
    loading="lazy"
    onerror="this.src='https://images.pexels.com/photos/159832/justice-law-case-hearing-159832.jpeg?auto=compress&cs=tinysrgb&w=1600'">
  <div class="img-banner-overlay">
    <p class="img-banner-quote">
      <em>Justiça</em> não é apenas uma palavra —<br>é o compromisso que assumimos com cada cliente.
    </p>
    <a href="https://wa.me/5531997177002" target="_blank" rel="noopener noreferrer" class="img-banner-btn">Agende sua Consulta</a>
  </div>
</div>

<!-- CONTATO -->
<section class="contact" id="contato">
  <div class="section-tag">Entre em Contato</div>
  <h2 class="section-title" style="margin-bottom:60px">Estamos prontos para <em>atender você</em></h2>
  <div class="contact-inner">
    <div>
      <div class="contact-block">
        <div class="contact-block-label">Telefone / WhatsApp</div>
        <div class="contact-block-value">
          <a href="https://wa.me/5531997177002" target="_blank" rel="noopener noreferrer">(31) 99717-7002</a>
        </div>
      </div>
      <div class="contact-block">
        <div class="contact-block-label">Endereço</div>
        <div class="contact-block-value">
          Av. Raja Gabáglia, 2000 - Sala 311, Torre 1<br>
          Estoril, Belo Horizonte - MG<br>
          CEP: 30494-170
        </div>
      </div>
      <div class="contact-block">
        <div class="contact-block-label">Horário de Atendimento</div>
        <div class="contact-block-value">Segunda a Sexta: 9h às 18h</div>
      </div>
      <div class="map-placeholder">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3751.3773316413!2d-43.9886!3d-19.9474!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0xa6917c2ffd9b70f%3A0xa14e5fcafd45977e!2sAv.%20Raja%20Gab%C3%A1glia%2C%202000%20-%20Estoril%2C%20Belo%20Horizonte%20-%20MG%2C%2030494-170!5e0!3m2!1spt-BR!2sbr!4v1647899999999!5m2!1spt-BR!2sbr"
          allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade">
        </iframe>
      </div>
    </div>
    <div class="contact-cta-box">
      <h3 class="contact-cta-title">Agende sua<br><em>Consulta Hoje</em></h3>
      <p class="contact-cta-text">
        Nossa equipe está pronta para ouvir você e encontrar a melhor solução jurídica para o seu caso. Entre em contato agora mesmo pelo WhatsApp.
      </p>
      <a href="https://wa.me/5531997177002?text=Ol%C3%A1%2C%20gostaria%20de%20agendar%20uma%20consulta." class="whatsapp-btn" target="_blank" rel="noopener noreferrer">
        <span>💬</span> Falar pelo WhatsApp
      </a>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo-text">João Santana Junior Advocacia</div>
  <p>Todos os direitos reservados. João Santana Junior Advocacia © 2025</p>
</footer>

<script>
  // Nav scroll shadow
  window.addEventListener('scroll', () => {
    const nav = document.getElementById('nav');
    if (nav) nav.classList.toggle('scrolled', window.scrollY > 20);
  });

  // Hamburger toggle
  function toggleMenu() {
    const btn = document.getElementById('hamburger');
    const menu = document.getElementById('mobileMenu');
    if (!btn || !menu) return;
    const isOpen = menu.classList.contains('open');
    if (isOpen) {
      menu.classList.remove('open');
      btn.classList.remove('open');
    } else {
      menu.classList.add('open');
      btn.classList.add('open');
    }
  }

  function closeMenu() {
    const menu = document.getElementById('mobileMenu');
    const btn = document.getElementById('hamburger');
    if (menu) menu.classList.remove('open');
    if (btn) btn.classList.remove('open');
  }

  // Close menu on outside click
  document.addEventListener('click', function(e) {
    const menu = document.getElementById('mobileMenu');
    const btn = document.getElementById('hamburger');
    if (menu && menu.classList.contains('open') && !menu.contains(e.target) && btn && !btn.contains(e.target)) {
      closeMenu();
    }
  });

  // Scroll animations for cards
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.style.opacity = '1';
        entry.target.style.transform = 'translateY(0)';
      }
    });
  }, { threshold: 0.1, rootMargin: '0px 0px -20px 0px' });

  document.querySelectorAll('.area-card, .tcard, .pillar').forEach(el => {
    el.style.opacity = '0';
    el.style.transform = 'translateY(20px)';
    el.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
    observer.observe(el);
  });
</script>
</body>
</html>
