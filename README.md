Si te doy mi código HTML css js me puedes crear un enlace para tener un visualización de navegador “<!DOCTYPE html>
<html lang="es" class="scroll-smooth">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="NexaCore Studio — Agencia de desarrollo web premium. Creamos experiencias digitales de clase mundial: Landing Pages, E-Commerce, Apps Web, SEO y más." />
  <meta name="keywords" content="desarrollo web, agencia digital, diseño web, e-commerce, SEO, aplicaciones web, NexaCore" />
  <meta name="author" content="NexaCore Studio" />
  <meta name="robots" content="index, follow" />
  <!-- Open Graph -->
  <meta property="og:title" content="NexaCore Studio — Desarrollo Web Premium" />
  <meta property="og:description" content="Transformamos ideas en experiencias digitales de clase mundial." />
  <meta property="og:type" content="website" />
  <meta property="og:url" content="https://nexacore.studio" />
  <meta property="og:image" content="https://nexacore.studio/og-image.jpg" />
  <!-- Twitter Card -->
  <meta name="twitter:card" content="summary_large_image" />
  <meta name="twitter:title" content="NexaCore Studio" />
  <meta name="twitter:description" content="Desarrollo web premium de clase mundial." />
  <!-- Security Headers via meta (supplemental) -->
  <meta http-equiv="X-Content-Type-Options" content="nosniff" />
  <meta http-equiv="Referrer-Policy" content="strict-origin-when-cross-origin" />
  <!-- Structured Data -->
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "Organization",
    "name": "NexaCore Studio",
    "url": "https://nexacore.studio",
    "logo": "https://nexacore.studio/logo.png",
    "contactPoint": {"@type":"ContactPoint","telephone":"+1-555-000-0000","contactType":"customer service"},
    "sameAs": ["https://linkedin.com/company/nexacore","https://github.com/nexacore"]
  }
  </script>
  <title>NexaCore Studio — Desarrollo Web Premium</title>
  <!-- Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;1,9..40,300&display=swap" rel="stylesheet" />
  <!-- Tailwind CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- AOS -->
  <link href="https://unpkg.com/aos@2.3.4/dist/aos.css" rel="stylesheet" />
  <!-- Lucide Icons -->
  <script src="https://unpkg.com/lucide@latest/dist/umd/lucide.js"></script>

  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: { display: ['Syne','sans-serif'], body: ['DM Sans','sans-serif'] },
          colors: {
            nexa: { 50:'#f0fdf9', 100:'#ccfbee', 200:'#99f5dd', 300:'#5de8c5', 400:'#2dd4b0', 500:'#10b897', 600:'#0a9179', 700:'#0b7663', 800:'#0d5f50', 900:'#0d4f43', 950:'#052e27' },
            acid: { 400:'#a3ff57', 500:'#84f030' },
            void: { 900:'#050810', 800:'#090d18', 700:'#0d1220', 600:'#141926', 500:'#1a2133' }
          },
          animation: {
            'float':'float 6s ease-in-out infinite',
            'pulse-slow':'pulse 4s ease-in-out infinite',
            'spin-slow':'spin 20s linear infinite',
            'marquee':'marquee 30s linear infinite',
            'marquee2':'marquee2 30s linear infinite',
            'fade-in-up':'fadeInUp 0.6s ease forwards',
            'counter':'counter 2s ease-out forwards',
          },
          keyframes: {
            float:{'0%,100%':{transform:'translateY(0px)'},'50%':{transform:'translateY(-20px)'}},
            marquee:{'0%':{transform:'translateX(0%)'},'100%':{transform:'translateX(-50%)'}},
            marquee2:{'0%':{transform:'translateX(50%)'},'100%':{transform:'translateX(0%)'}},
            fadeInUp:{'0%':{opacity:'0',transform:'translateY(30px)'},'100%':{opacity:'1',transform:'translateY(0)'}},
          }
        }
      }
    }
  </script>

  <style>
    /* ===== BASE ===== */
    *,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
    html{scroll-behavior:smooth}
    body{font-family:'DM Sans',sans-serif;background:#050810;color:#e2e8f0;overflow-x:hidden;cursor:none}

    /* ===== CUSTOM CURSOR ===== */
    #cursor{position:fixed;width:12px;height:12px;background:#10b897;border-radius:50%;pointer-events:none;z-index:99999;transform:translate(-50%,-50%);transition:transform .1s,background .2s;mix-blend-mode:difference}
    #cursor-ring{position:fixed;width:36px;height:36px;border:1.5px solid rgba(16,184,151,.5);border-radius:50%;pointer-events:none;z-index:99998;transform:translate(-50%,-50%);transition:all .15s ease;mix-blend-mode:difference}
    body:hover #cursor{opacity:1}

    /* ===== LOADING SCREEN ===== */
    #loader{position:fixed;inset:0;background:#050810;z-index:99997;display:flex;align-items:center;justify-content:center;flex-direction:column;gap:1.5rem;transition:opacity .6s ease,visibility .6s}
    #loader.hidden{opacity:0;visibility:hidden;pointer-events:none}
    .loader-logo{font-family:'Syne',sans-serif;font-size:2rem;font-weight:800;color:#10b897;letter-spacing:-.02em}
    .loader-bar-wrap{width:200px;height:2px;background:rgba(255,255,255,.08);border-radius:2px;overflow:hidden}
    .loader-bar{height:100%;background:linear-gradient(90deg,#10b897,#a3ff57);width:0%;transition:width 2s ease;border-radius:2px}

    /* ===== NOISE OVERLAY ===== */
    body::before{content:'';position:fixed;inset:0;background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='1'/%3E%3C/svg%3E");opacity:.03;pointer-events:none;z-index:0}

    /* ===== GLOW ORBS ===== */
    .orb{position:absolute;border-radius:50%;filter:blur(80px);opacity:.15;pointer-events:none}
    .orb-1{width:600px;height:600px;background:#10b897;top:-200px;right:-100px}
    .orb-2{width:400px;height:400px;background:#0d4f43;bottom:0;left:-100px}
    .orb-3{width:300px;height:300px;background:#a3ff57;top:50%;left:50%}

    /* ===== GLASS CARD ===== */
    .glass{background:rgba(255,255,255,.03);backdrop-filter:blur(20px);-webkit-backdrop-filter:blur(20px);border:1px solid rgba(255,255,255,.06);border-radius:1.25rem}
    .glass-hover{transition:all .3s ease}
    .glass-hover:hover{background:rgba(255,255,255,.06);border-color:rgba(16,184,151,.3);transform:translateY(-4px);box-shadow:0 24px 60px rgba(16,184,151,.1)}

    /* ===== GRADIENT TEXT ===== */
    .grad-text{background:linear-gradient(135deg,#10b897 0%,#a3ff57 100%);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text}
    .grad-text-2{background:linear-gradient(135deg,#fff 30%,rgba(255,255,255,.5));-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text}

    /* ===== SECTION ===== */
    .section{padding:7rem 0;position:relative;overflow:hidden}
    .container{max-width:1280px;margin:0 auto;padding:0 1.5rem}
    .section-label{font-family:'Syne',sans-serif;font-size:.75rem;font-weight:700;letter-spacing:.2em;text-transform:uppercase;color:#10b897;margin-bottom:1rem}
    .section-title{font-family:'Syne',sans-serif;font-size:clamp(2rem,5vw,3.5rem);font-weight:800;line-height:1.1;letter-spacing:-.03em;margin-bottom:1.5rem}

    /* ===== BUTTONS ===== */
    .btn-primary{display:inline-flex;align-items:center;gap:.5rem;background:linear-gradient(135deg,#10b897,#0a9179);color:#fff;font-family:'Syne',sans-serif;font-weight:700;font-size:.9rem;padding:.85rem 2rem;border-radius:100px;border:none;cursor:pointer;transition:all .3s ease;position:relative;overflow:hidden;letter-spacing:.01em}
    .btn-primary::before{content:'';position:absolute;inset:0;background:linear-gradient(135deg,#a3ff57,#10b897);opacity:0;transition:opacity .3s}
    .btn-primary:hover::before{opacity:1}
    .btn-primary:hover{transform:translateY(-2px);box-shadow:0 16px 40px rgba(16,184,151,.4)}
    .btn-primary span{position:relative;z-index:1}
    .btn-secondary{display:inline-flex;align-items:center;gap:.5rem;background:transparent;color:#e2e8f0;font-family:'Syne',sans-serif;font-weight:600;font-size:.9rem;padding:.85rem 2rem;border-radius:100px;border:1px solid rgba(255,255,255,.15);cursor:pointer;transition:all .3s ease}
    .btn-secondary:hover{border-color:#10b897;color:#10b897;background:rgba(16,184,151,.05)}

    /* ===== NAV ===== */
    nav{position:fixed;top:0;left:0;right:0;z-index:1000;padding:1.25rem 0;transition:all .4s ease}
    nav.scrolled{background:rgba(5,8,16,.85);backdrop-filter:blur(24px);-webkit-backdrop-filter:blur(24px);border-bottom:1px solid rgba(255,255,255,.06);padding:.85rem 0}
    .nav-logo{font-family:'Syne',sans-serif;font-weight:800;font-size:1.4rem;color:#fff;text-decoration:none;letter-spacing:-.03em}
    .nav-logo span{color:#10b897}
    .nav-link{font-family:'Syne',sans-serif;font-size:.85rem;font-weight:600;color:rgba(255,255,255,.7);text-decoration:none;transition:color .2s;letter-spacing:.01em}
    .nav-link:hover{color:#10b897}

    /* ===== HERO ===== */
    #hero{min-height:100vh;display:flex;align-items:center;padding-top:5rem;position:relative;overflow:hidden}
    .hero-grid{background-image:linear-gradient(rgba(16,184,151,.08) 1px,transparent 1px),linear-gradient(90deg,rgba(16,184,151,.08) 1px,transparent 1px);background-size:60px 60px;position:absolute;inset:0;mask-image:radial-gradient(ellipse 80% 50% at 50% 0%,black,transparent)}
    .stat-card{background:rgba(255,255,255,.03);border:1px solid rgba(255,255,255,.08);border-radius:1rem;padding:1.25rem 1.5rem;text-align:center;transition:all .3s}
    .stat-card:hover{border-color:rgba(16,184,151,.4);background:rgba(16,184,151,.05)}
    .stat-num{font-family:'Syne',sans-serif;font-size:2rem;font-weight:800;color:#10b897;line-height:1}
    .stat-label{font-size:.8rem;color:rgba(255,255,255,.5);margin-top:.25rem}

    /* ===== FLOATING TECH BADGE ===== */
    .tech-badge{position:absolute;background:rgba(255,255,255,.04);backdrop-filter:blur(12px);border:1px solid rgba(255,255,255,.1);border-radius:.75rem;padding:.6rem 1rem;font-family:'Syne',sans-serif;font-size:.8rem;font-weight:700;color:rgba(255,255,255,.8);white-space:nowrap}

    /* ===== TEAM CARDS ===== */
    .team-card{position:relative;overflow:hidden;border-radius:1.5rem;background:rgba(255,255,255,.03);border:1px solid rgba(255,255,255,.07);transition:all .4s ease}
    .team-card:hover{border-color:rgba(16,184,151,.4);transform:translateY(-6px)}
    .team-card::before{content:'';position:absolute;inset:0;background:linear-gradient(to top,rgba(16,184,151,.15),transparent);opacity:0;transition:opacity .4s}
    .team-card:hover::before{opacity:1}
    .team-avatar{width:100%;aspect-ratio:1;object-fit:cover;display:block}

    /* ===== SERVICE CARDS ===== */
    .service-card{background:rgba(255,255,255,.02);border:1px solid rgba(255,255,255,.07);border-radius:1.25rem;padding:2rem;transition:all .3s ease;position:relative;overflow:hidden;group:true}
    .service-card::after{content:'';position:absolute;inset:0;background:radial-gradient(circle at 80% 20%,rgba(16,184,151,.08),transparent 60%);opacity:0;transition:opacity .4s}
    .service-card:hover::after{opacity:1}
    .service-card:hover{border-color:rgba(16,184,151,.35);transform:translateY(-4px);box-shadow:0 20px 50px rgba(0,0,0,.4)}
    .service-icon{width:52px;height:52px;background:linear-gradient(135deg,rgba(16,184,151,.2),rgba(163,255,87,.1));border:1px solid rgba(16,184,151,.3);border-radius:.875rem;display:flex;align-items:center;justify-content:center;margin-bottom:1.25rem;color:#10b897}

    /* ===== PROGRESS BARS ===== */
    .prog-bar{height:4px;background:rgba(255,255,255,.06);border-radius:4px;overflow:hidden;position:relative}
    .prog-fill{height:100%;background:linear-gradient(90deg,#10b897,#a3ff57);border-radius:4px;width:0%;transition:width 1.5s cubic-bezier(.4,0,.2,1)}
    .prog-fill.animated{width:var(--prog)}

    /* ===== PORTFOLIO FILTER ===== */
    .filter-btn{font-family:'Syne',sans-serif;font-size:.8rem;font-weight:700;padding:.5rem 1.25rem;border-radius:100px;border:1px solid rgba(255,255,255,.12);background:transparent;color:rgba(255,255,255,.6);cursor:pointer;transition:all .25s;letter-spacing:.05em}
    .filter-btn.active,.filter-btn:hover{background:rgba(16,184,151,.15);border-color:#10b897;color:#10b897}

    /* ===== PORTFOLIO CARD ===== */
    .portfolio-card{border-radius:1.25rem;overflow:hidden;position:relative;cursor:pointer;aspect-ratio:16/10;background:#090d18;border:1px solid rgba(255,255,255,.07);transition:all .4s}
    .portfolio-card:hover{transform:scale(1.02);border-color:rgba(16,184,151,.4)}
    .portfolio-overlay{position:absolute;inset:0;background:linear-gradient(to top,rgba(5,8,16,.95) 0%,rgba(5,8,16,.4) 50%,transparent 100%);opacity:0;transition:opacity .4s;display:flex;flex-direction:column;justify-content:flex-end;padding:1.5rem}
    .portfolio-card:hover .portfolio-overlay{opacity:1}

    /* ===== TESTIMONIALS ===== */
    .testimonial-slider{display:flex;gap:1.5rem;transition:transform .5s ease}
    .testimonial-card{min-width:380px;background:rgba(255,255,255,.03);border:1px solid rgba(255,255,255,.07);border-radius:1.5rem;padding:2rem;flex-shrink:0}

    /* ===== MARQUEE ===== */
    .marquee-wrapper{overflow:hidden;position:relative}
    .marquee-wrapper::before,.marquee-wrapper::after{content:'';position:absolute;top:0;bottom:0;width:120px;z-index:2}
    .marquee-wrapper::before{left:0;background:linear-gradient(90deg,#050810,transparent)}
    .marquee-wrapper::after{right:0;background:linear-gradient(-90deg,#050810,transparent)}
    .marquee-track{display:flex;width:max-content;animation:marquee 30s linear infinite}
    .marquee-track:hover{animation-play-state:paused}

    /* ===== FAQ ACCORDION ===== */
    .faq-item{border:1px solid rgba(255,255,255,.07);border-radius:1rem;overflow:hidden;transition:border-color .3s}
    .faq-item.open{border-color:rgba(16,184,151,.35)}
    .faq-btn{width:100%;display:flex;align-items:center;justify-content:space-between;padding:1.25rem 1.5rem;background:rgba(255,255,255,.02);color:#e2e8f0;font-family:'Syne',sans-serif;font-weight:600;font-size:.95rem;cursor:pointer;border:none;text-align:left;transition:background .3s;gap:1rem}
    .faq-btn:hover{background:rgba(255,255,255,.04)}
    .faq-icon{flex-shrink:0;width:22px;height:22px;border:1px solid rgba(255,255,255,.2);border-radius:50%;display:flex;align-items:center;justify-content:center;transition:all .3s;color:#10b897}
    .faq-item.open .faq-icon{background:#10b897;border-color:#10b897;color:#050810;transform:rotate(45deg)}
    .faq-body{max-height:0;overflow:hidden;transition:max-height .4s ease,padding .3s}
    .faq-body.open{max-height:300px;padding:0 1.5rem 1.5rem}
    .faq-body p{color:rgba(255,255,255,.55);font-size:.9rem;line-height:1.8}

    /* ===== CONTACT FORM ===== */
    .form-group{display:flex;flex-direction:column;gap:.4rem}
    .form-label{font-family:'Syne',sans-serif;font-size:.8rem;font-weight:700;color:rgba(255,255,255,.5);letter-spacing:.05em;text-transform:uppercase}
    .form-input{background:rgba(255,255,255,.04);border:1px solid rgba(255,255,255,.1);border-radius:.75rem;padding:.85rem 1.1rem;color:#e2e8f0;font-family:'DM Sans',sans-serif;font-size:.9rem;outline:none;transition:all .3s;width:100%}
    .form-input:focus{border-color:#10b897;background:rgba(16,184,151,.05);box-shadow:0 0 0 3px rgba(16,184,151,.1)}
    .form-input.error{border-color:#ef4444}
    .form-error{font-size:.78rem;color:#ef4444;margin-top:.25rem;display:none}
    .form-error.show{display:block}
    select.form-input option{background:#090d18}

    /* ===== WHATSAPP FLOAT ===== */
    #wa-btn{position:fixed;bottom:2rem;right:2rem;z-index:999;background:linear-gradient(135deg,#25d366,#128c7e);width:62px;height:62px;border-radius:50%;display:flex;align-items:center;justify-content:center;box-shadow:0 8px 32px rgba(37,211,102,.4);cursor:pointer;transition:all .3s;text-decoration:none;border:none}
    #wa-btn::before{content:'';position:absolute;inset:-4px;border-radius:50%;background:rgba(37,211,102,.3);animation:pulse 2.5s ease-in-out infinite}
    #wa-btn:hover{transform:scale(1.1) translateY(-3px)}
    #wa-tooltip{position:absolute;right:74px;top:50%;transform:translateY(-50%);background:#090d18;border:1px solid rgba(255,255,255,.1);border-radius:.75rem;padding:.5rem 1rem;font-family:'Syne',sans-serif;font-size:.8rem;font-weight:700;white-space:nowrap;opacity:0;pointer-events:none;transition:opacity .3s}
    #wa-btn:hover #wa-tooltip{opacity:1}

    /* ===== FOOTER ===== */
    footer{background:#090d18;border-top:1px solid rgba(255,255,255,.06)}
    .footer-link{font-size:.88rem;color:rgba(255,255,255,.45);text-decoration:none;transition:color .2s;display:block;margin-bottom:.6rem}
    .footer-link:hover{color:#10b897}
    .social-icon{width:38px;height:38px;background:rgba(255,255,255,.05);border:1px solid rgba(255,255,255,.1);border-radius:.625rem;display:flex;align-items:center;justify-content:center;color:rgba(255,255,255,.6);cursor:pointer;transition:all .25s;text-decoration:none}
    .social-icon:hover{background:rgba(16,184,151,.15);border-color:#10b897;color:#10b897;transform:translateY(-2px)}

    /* ===== MODAL ===== */
    #modal{position:fixed;inset:0;z-index:9999;display:none;align-items:center;justify-content:center;padding:1.5rem}
    #modal.open{display:flex}
    #modal-bg{position:absolute;inset:0;background:rgba(5,8,16,.9);backdrop-filter:blur(12px)}
    #modal-box{position:relative;z-index:1;background:#090d18;border:1px solid rgba(255,255,255,.1);border-radius:1.5rem;max-width:680px;width:100%;max-height:85vh;overflow-y:auto;padding:2.5rem}

    /* ===== TIMELINE ===== */
    .timeline-line{position:absolute;left:50%;top:0;bottom:0;width:1px;background:linear-gradient(to bottom,transparent,rgba(16,184,151,.4),transparent);transform:translateX(-50%)}
    .timeline-dot{width:12px;height:12px;background:#10b897;border-radius:50%;box-shadow:0 0 0 4px rgba(16,184,151,.2)}

    /* ===== SCROLLBAR ===== */
    ::-webkit-scrollbar{width:4px}
    ::-webkit-scrollbar-track{background:#050810}
    ::-webkit-scrollbar-thumb{background:#10b897;border-radius:4px}

    /* ===== RESPONSIVE ===== */
    @media(max-width:768px){
      .section{padding:4rem 0}
      .section-title{font-size:2rem}
      .testimonial-card{min-width:300px}
      #cursor,#cursor-ring{display:none}
      body{cursor:auto}
    }
    @media(max-width:640px){
      .tech-badge{display:none}
    }

    /* ===== AOS OVERRIDE ===== */
    [data-aos]{pointer-events:none}
    [data-aos].aos-animate{pointer-events:auto}
  </style>
</head>
<body>

<!-- ===== LOADER ===== -->
<div id="loader">
  <div class="loader-logo">Nexa<span style="color:#a3ff57">Core</span></div>
  <div class="loader-bar-wrap"><div class="loader-bar" id="loader-bar"></div></div>
  <p style="font-size:.78rem;color:rgba(255,255,255,.3);font-family:'Syne',sans-serif;letter-spacing:.15em">INICIALIZANDO</p>
</div>

<!-- ===== CUSTOM CURSOR ===== -->
<div id="cursor"></div>
<div id="cursor-ring"></div>

<!-- ===== NAVIGATION ===== -->
<nav id="navbar">
  <div class="container">
    <div style="display:flex;align-items:center;justify-content:space-between;gap:2rem">
      <a href="#hero" class="nav-logo">Nexa<span>Core</span></a>
      <!-- Desktop -->
      <div class="hidden md:flex items-center gap-8">
        <a href="#about" class="nav-link">Nosotros</a>
        <a href="#services" class="nav-link">Servicios</a>
        <a href="#portfolio" class="nav-link">Portafolio</a>
        <a href="#team" class="nav-link">Equipo</a>
        <a href="#contact" class="nav-link">Contacto</a>
      </div>
      <div class="flex items-center gap-3">
        <a href="#contact" class="btn-primary hidden sm:inline-flex"><span>Cotizar Proyecto</span></a>
        <!-- Mobile hamburger -->
        <button id="menu-btn" class="md:hidden text-white p-2" aria-label="Abrir menú">
          <svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M3 12h18M3 6h18M3 18h18"/></svg>
        </button>
      </div>
    </div>
  </div>
  <!-- Mobile Menu -->
  <div id="mobile-menu" style="display:none;background:rgba(9,13,24,.98);border-top:1px solid rgba(255,255,255,.06);padding:1.5rem">
    <div style="display:flex;flex-direction:column;gap:1.2rem">
      <a href="#about" class="nav-link text-base" onclick="closeMobileMenu()">Nosotros</a>
      <a href="#services" class="nav-link text-base" onclick="closeMobileMenu()">Servicios</a>
      <a href="#portfolio" class="nav-link text-base" onclick="closeMobileMenu()">Portafolio</a>
      <a href="#team" class="nav-link text-base" onclick="closeMobileMenu()">Equipo</a>
      <a href="#contact" class="nav-link text-base" onclick="closeMobileMenu()">Contacto</a>
      <a href="#contact" class="btn-primary text-center justify-center" onclick="closeMobileMenu()"><span>Cotizar Proyecto</span></a>
    </div>
  </div>
</nav>

<!-- ===== HERO ===== -->
<section id="hero">
  <div class="hero-grid"></div>
  <div class="orb orb-1"></div>
  <div class="orb orb-2"></div>
  <div class="container" style="position:relative;z-index:1;width:100%">
    <div style="display:grid;grid-template-columns:1fr 1fr;gap:4rem;align-items:center" class="hero-grid-layout">

      <!-- Left -->
      <div>
        <div style="display:inline-flex;align-items:center;gap:.5rem;background:rgba(16,184,151,.1);border:1px solid rgba(16,184,151,.25);border-radius:100px;padding:.4rem 1rem;margin-bottom:1.5rem" data-aos="fade-down">
          <span style="width:6px;height:6px;background:#a3ff57;border-radius:50%;animation:pulse 2s infinite"></span>
          <span style="font-family:'Syne',sans-serif;font-size:.78rem;font-weight:700;color:#10b897;letter-spacing:.1em">DISPONIBLES PARA NUEVOS PROYECTOS</span>
        </div>

        <h1 style="font-family:'Syne',sans-serif;font-weight:800;font-size:clamp(2.5rem,6vw,4.5rem);line-height:1.05;letter-spacing:-.04em;margin-bottom:1.5rem" data-aos="fade-up" data-aos-delay="100">
          <span class="grad-text-2">Construimos el</span><br/>
          <span class="grad-text">futuro digital</span><br/>
          <span class="grad-text-2">de tu empresa.</span>
        </h1>

        <p style="font-size:1.05rem;color:rgba(255,255,255,.55);line-height:1.8;max-width:480px;margin-bottom:2.5rem" data-aos="fade-up" data-aos-delay="200">
          Somos <strong style="color:rgba(255,255,255,.8)">NexaCore Studio</strong>, una agencia de desarrollo web premium que transforma ideas en experiencias digitales de clase mundial — rápidas, seguras y diseñadas para convertir.
        </p>

        <div style="display:flex;flex-wrap:wrap;gap:1rem;margin-bottom:3.5rem" data-aos="fade-up" data-aos-delay="300">
          <a href="#contact" class="btn-primary"><span>Solicitar Cotización</span><svg width="16" height="16" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><path d="M5 12h14m-7-7 7 7-7 7"/></svg></a>
          <a href="#portfolio" class="btn-secondary">Ver Portafolio <svg width="16" height="16" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M5 12h14m-7-7 7 7-7 7"/></svg></a>
        </div>

        <!-- Stats -->
        <div style="display:grid;grid-template-columns:repeat(4,1fr);gap:1rem" data-aos="fade-up" data-aos-delay="400">
          <div class="stat-card"><div class="stat-num" data-count="200">0</div><div class="stat-label">Clientes<br/>Satisfechos</div></div>
          <div class="stat-card"><div class="stat-num" data-count="340">0</div><div class="stat-label">Proyectos<br/>Completados</div></div>
          <div class="stat-card"><div class="stat-num" data-count="8">0</div><div class="stat-label">Años de<br/>Experiencia</div></div>
          <div class="stat-card"><div class="stat-num" data-count="30">0</div><div class="stat-label">Tecnologías<br/>Dominadas</div></div>
        </div>
      </div>

      <!-- Right — visual -->
      <div style="position:relative;display:flex;align-items:center;justify-content:center;min-height:500px" data-aos="fade-left" data-aos-delay="200">
        <!-- Central glow orb -->
        <div style="position:absolute;width:300px;height:300px;background:radial-gradient(circle,rgba(16,184,151,.2),transparent 70%);border-radius:50%"></div>
        <!-- Main card -->
        <div class="glass" style="padding:2rem;width:320px;position:relative;z-index:2;animation:float 6s ease-in-out infinite">
          <div style="display:flex;align-items:center;gap:.75rem;margin-bottom:1.5rem">
            <div style="width:36px;height:36px;background:linear-gradient(135deg,#10b897,#a3ff57);border-radius:.6rem;display:flex;align-items:center;justify-content:center">
              <svg width="18" height="18" fill="none" stroke="#050810" stroke-width="2.5" viewBox="0 0 24 24"><path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"/></svg>
            </div>
            <div>
              <p style="font-family:'Syne',sans-serif;font-weight:700;font-size:.9rem">NexaShop E-Commerce</p>
              <p style="font-size:.75rem;color:rgba(255,255,255,.4)">Lanzado hace 2 horas</p>
            </div>
          </div>
          <!-- Mini chart -->
          <div style="display:flex;align-items:flex-end;gap:.3rem;height:60px;margin-bottom:1rem">
            <div style="flex:1;background:rgba(16,184,151,.2);border-radius:.25rem;height:40%"></div>
            <div style="flex:1;background:rgba(16,184,151,.3);border-radius:.25rem;height:65%"></div>
            <div style="flex:1;background:rgba(16,184,151,.4);border-radius:.25rem;height:45%"></div>
            <div style="flex:1;background:rgba(16,184,151,.5);border-radius:.25rem;height:80%"></div>
            <div style="flex:1;background:rgba(16,184,151,.6);border-radius:.25rem;height:55%"></div>
            <div style="flex:1;background:rgba(163,255,87,.6);border-radius:.25rem;height:90%"></div>
            <div style="flex:1;background:rgba(163,255,87,.8);border-radius:.25rem;height:70%"></div>
          </div>
          <div style="display:flex;align-items:center;justify-content:space-between">
            <div>
              <p style="font-family:'Syne',sans-serif;font-size:1.5rem;font-weight:800;color:#a3ff57">+247%</p>
              <p style="font-size:.75rem;color:rgba(255,255,255,.4)">Conversiones este mes</p>
            </div>
            <div style="width:42px;height:42px;background:rgba(163,255,87,.1);border:1px solid rgba(163,255,87,.3);border-radius:50%;display:flex;align-items:center;justify-content:center">
              <svg width="18" height="18" fill="none" stroke="#a3ff57" stroke-width="2.5" viewBox="0 0 24 24"><path d="M7 17L17 7M17 7H7M17 7v10"/></svg>
            </div>
          </div>
        </div>

        <!-- Floating badges -->
        <div class="tech-badge" style="top:10%;left:0;animation:float 5s ease-in-out infinite .5s">⚡ Next.js 14</div>
        <div class="tech-badge" style="bottom:20%;left:5%;animation:float 5.5s ease-in-out infinite 1s">🎨 Figma</div>
        <div class="tech-badge" style="top:25%;right:0;animation:float 6s ease-in-out infinite .2s">🛡️ 99.9% Uptime</div>
        <div class="tech-badge" style="bottom:10%;right:5%;animation:float 4.5s ease-in-out infinite .8s">🚀 Lighthouse 100</div>
      </div>
    </div>
  </div>
</section>

<!-- ===== SPONSORS MARQUEE ===== -->
<section style="padding:3rem 0;border-top:1px solid rgba(255,255,255,.05);border-bottom:1px solid rgba(255,255,255,.05);background:rgba(9,13,24,.5);overflow:hidden">
  <p style="text-align:center;font-family:'Syne',sans-serif;font-size:.72rem;font-weight:700;letter-spacing:.2em;color:rgba(255,255,255,.25);margin-bottom:2rem">EMPRESAS QUE CONFÍAN EN NOSOTROS</p>
  <div class="marquee-wrapper">
    <div class="marquee-track">
      <!-- logos (text-based for demo) -->
      <span style="margin:0 3rem;font-family:'Syne',sans-serif;font-size:1.1rem;font-weight:800;color:rgba(255,255,255,.2);letter-spacing:-.03em">TechCorp</span>
      <span style="margin:0 3rem;font-family:'Syne',sans-serif;font-size:1.1rem;font-weight:800;color:rgba(255,255,255,.2);letter-spacing:-.03em">Nexabit</span>
      <span style="margin:0 3rem;font-family:'Syne',sans-serif;font-size:1.1rem;font-weight:800;color:rgba(255,255,255,.2);letter-spacing:-.03em">AeroStore</span>
      <span style="margin:0 3rem;font-family:'Syne',sans-serif;font-size:1.1rem;font-weight:800;color:rgba(255,255,255,.2);letter-spacing:-.03em">FintraX</span>
      <span style="margin:0 3rem;font-family:'Syne',sans-serif;font-size:1.1rem;font-weight:800;color:rgba(255,255,255,.2);letter-spacing:-.03em">HealthHub</span>
      <span style="margin:0 3rem;font-family:'Syne',sans-serif;font-size:1.1rem;font-weight:800;color:rgba(255,255,255,.2);letter-spacing:-.03em">PropiaMedia</span>
      <span style="margin:0 3rem;font-family:'Syne',sans-serif;font-size:1.1rem;font-weight:800;color:rgba(255,255,255,.2);letter-spacing:-.03em">Cloudify</span>
      <span style="margin:0 3rem;font-family:'Syne',sans-serif;font-size:1.1rem;font-weight:800;color:rgba(255,255,255,.2);letter-spacing:-.03em">Orbis AI</span>
      <!-- duplicate for seamless loop -->
      <span style="margin:0 3rem;font-family:'Syne',sans-serif;font-size:1.1rem;font-weight:800;color:rgba(255,255,255,.2);letter-spacing:-.03em">TechCorp</span>
      <span style="margin:0 3rem;font-family:'Syne',sans-serif;font-size:1.1rem;font-weight:800;color:rgba(255,255,255,.2);letter-spacing:-.03em">Nexabit</span>
      <span style="margin:0 3rem;font-family:'Syne',sans-serif;font-size:1.1rem;font-weight:800;color:rgba(255,255,255,.2);letter-spacing:-.03em">AeroStore</span>
      <span style="margin:0 3rem;font-family:'Syne',sans-serif;font-size:1.1rem;font-weight:800;color:rgba(255,255,255,.2);letter-spacing:-.03em">FintraX</span>
      <span style="margin:0 3rem;font-family:'Syne',sans-serif;font-size:1.1rem;font-weight:800;color:rgba(255,255,255,.2);letter-spacing:-.03em">HealthHub</span>
      <span style="margin:0 3rem;font-family:'Syne',sans-serif;font-size:1.1rem;font-weight:800;color:rgba(255,255,255,.2);letter-spacing:-.03em">PropiaMedia</span>
      <span style="margin:0 3rem;font-family:'Syne',sans-serif;font-size:1.1rem;font-weight:800;color:rgba(255,255,255,.2);letter-spacing:-.03em">Cloudify</span>
      <span style="margin:0 3rem;font-family:'Syne',sans-serif;font-size:1.1rem;font-weight:800;color:rgba(255,255,255,.2);letter-spacing:-.03em">Orbis AI</span>
    </div>
  </div>
</section>

<!-- ===== ABOUT ===== -->
<section id="about" class="section">
  <div class="orb" style="width:400px;height:400px;background:#0a9179;top:0;right:0;opacity:.1"></div>
  <div class="container" style="position:relative;z-index:1">
    <div style="display:grid;grid-template-columns:1fr 1fr;gap:5rem;align-items:center">
      <!-- Left visual -->
      <div data-aos="fade-right">
        <div style="position:relative">
          <div style="background:linear-gradient(135deg,rgba(16,184,151,.15),rgba(163,255,87,.05));border:1px solid rgba(16,184,151,.2);border-radius:2rem;padding:2.5rem;position:relative;z-index:1">
            <!-- Mission Vis Cards -->
            <div style="display:grid;gap:1rem">
              <div class="glass" style="padding:1.25rem;border-radius:1rem;display:flex;gap:1rem;align-items:flex-start">
                <div style="width:40px;height:40px;background:rgba(16,184,151,.15);border-radius:.75rem;display:flex;align-items:center;justify-content:center;flex-shrink:0"><svg width="20" height="20" fill="none" stroke="#10b897" stroke-width="2" viewBox="0 0 24 24"><circle cx="12" cy="12" r="10"/><path d="M12 8v4l3 3"/></svg></div>
                <div><p style="font-family:'Syne',sans-serif;font-weight:700;font-size:.9rem;margin-bottom:.25rem">Misión</p><p style="font-size:.82rem;color:rgba(255,255,255,.5);line-height:1.6">Potenciar negocios con soluciones digitales de alto impacto que generan resultados medibles.</p></div>
              </div>
              <div class="glass" style="padding:1.25rem;border-radius:1rem;display:flex;gap:1rem;align-items:flex-start">
                <div style="width:40px;height:40px;background:rgba(163,255,87,.1);border-radius:.75rem;display:flex;align-items:center;justify-content:center;flex-shrink:0"><svg width="20" height="20" fill="none" stroke="#a3ff57" stroke-width="2" viewBox="0 0 24 24"><path d="M2 12s3-7 10-7 10 7 10 7-3 7-10 7-10-7-10-7z"/><circle cx="12" cy="12" r="3"/></svg></div>
                <div><p style="font-family:'Syne',sans-serif;font-weight:700;font-size:.9rem;margin-bottom:.25rem">Visión</p><p style="font-size:.82rem;color:rgba(255,255,255,.5);line-height:1.6">Ser la agencia digital más reconocida de Latinoamérica, referente en innovación y excelencia.</p></div>
              </div>
              <div class="glass" style="padding:1.25rem;border-radius:1rem;display:flex;gap:1rem;align-items:flex-start">
                <div style="width:40px;height:40px;background:rgba(16,184,151,.1);border-radius:.75rem;display:flex;align-items:center;justify-content:center;flex-shrink:0"><svg width="20" height="20" fill="none" stroke="#10b897" stroke-width="2" viewBox="0 0 24 24"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg></div>
                <div><p style="font-family:'Syne',sans-serif;font-weight:700;font-size:.9rem;margin-bottom:.25rem">Valores</p><p style="font-size:.82rem;color:rgba(255,255,255,.5);line-height:1.6">Innovación · Transparencia · Compromiso · Calidad · Orientación al cliente</p></div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Right text -->
      <div data-aos="fade-left" data-aos-delay="100">
        <p class="section-label">Sobre Nosotros</p>
        <h2 class="section-title"><span class="grad-text-2">Una agencia con</span><br/><span class="grad-text">ADN tecnológico.</span></h2>
        <p style="color:rgba(255,255,255,.55);line-height:1.8;margin-bottom:1.5rem">Fundada en 2016, <strong style="color:rgba(255,255,255,.8)">NexaCore Studio</strong> nació con la convicción de que cada negocio merece una presencia digital extraordinaria. Comenzamos como un equipo de 3 apasionados del código; hoy somos un estudio de 20+ profesionales especializados en crear experiencias que convierten visitantes en clientes.</p>
        <p style="color:rgba(255,255,255,.55);line-height:1.8;margin-bottom:2rem">Trabajamos con startups innovadoras, pymes en crecimiento y corporativos globales. Nuestro proceso es transparente, ágil y enfocado en resultados — no en horas de trabajo.</p>

        <!-- Timeline -->
        <div style="position:relative;padding-left:1.5rem;border-left:1px solid rgba(16,184,151,.25)">
          <div style="margin-bottom:1.25rem;position:relative">
            <div style="position:absolute;left:-1.75rem;top:.2rem;width:10px;height:10px;background:#10b897;border-radius:50%"></div>
            <p style="font-family:'Syne',sans-serif;font-weight:700;font-size:.88rem;color:#10b897">2016 — Fundación</p>
            <p style="font-size:.82rem;color:rgba(255,255,255,.45);margin-top:.2rem">Primer proyecto: tienda online que generó $200k en su primer año</p>
          </div>
          <div style="margin-bottom:1.25rem;position:relative">
            <div style="position:absolute;left:-1.75rem;top:.2rem;width:10px;height:10px;background:#10b897;border-radius:50%"></div>
            <p style="font-family:'Syne',sans-serif;font-weight:700;font-size:.88rem;color:#10b897">2019 — Expansión</p>
            <p style="font-size:.82rem;color:rgba(255,255,255,.45);margin-top:.2rem">Apertura de oficina en Miami y alcance de 100 clientes internacionales</p>
          </div>
          <div style="margin-bottom:1.25rem;position:relative">
            <div style="position:absolute;left:-1.75rem;top:.2rem;width:10px;height:10px;background:#10b897;border-radius:50%"></div>
            <p style="font-family:'Syne',sans-serif;font-weight:700;font-size:.88rem;color:#10b897">2022 — Escala</p>
            <p style="font-size:.82rem;color:rgba(255,255,255,.45);margin-top:.2rem">Premio a Mejor Agencia Digital LatAm. 200+ proyectos entregados</p>
          </div>
          <div style="position:relative">
            <div style="position:absolute;left:-1.75rem;top:.2rem;width:10px;height:10px;background:#a3ff57;border-radius:50%;box-shadow:0 0 10px rgba(163,255,87,.5)"></div>
            <p style="font-family:'Syne',sans-serif;font-weight:700;font-size:.88rem;color:#a3ff57">2024 — Presente</p>
            <p style="font-size:.82rem;color:rgba(255,255,255,.45);margin-top:.2rem">Pioneros en IA aplicada al desarrollo web. 340+ proyectos y creciendo</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ===== SERVICES ===== -->
<section id="services" class="section" style="background:rgba(9,13,24,.6)">
  <div class="container">
    <div style="text-align:center;max-width:600px;margin:0 auto 4rem" data-aos="fade-up">
      <p class="section-label">Nuestros Servicios</p>
      <h2 class="section-title"><span class="grad-text-2">Todo lo que tu</span><br/><span class="grad-text">negocio necesita.</span></h2>
      <p style="color:rgba(255,255,255,.45);line-height:1.8">Soluciones digitales integrales diseñadas para impulsar el crecimiento de tu empresa desde el día uno.</p>
    </div>

    <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:1.5rem">

      <!-- Service Card Template -->
      <div class="service-card" data-aos="fade-up" data-aos-delay="0">
        <div class="service-icon"><svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><rect x="3" y="3" width="18" height="18" rx="2"/><path d="M3 9h18"/><path d="M9 21V9"/></svg></div>
        <h3 style="font-family:'Syne',sans-serif;font-weight:700;font-size:1.05rem;margin-bottom:.625rem">Landing Pages</h3>
        <p style="font-size:.85rem;color:rgba(255,255,255,.45);line-height:1.7;margin-bottom:1.25rem">Páginas diseñadas para convertir visitantes en clientes. CRO aplicado desde el diseño.</p>
        <ul style="font-size:.8rem;color:rgba(255,255,255,.4);list-style:none;display:flex;flex-direction:column;gap:.4rem;margin-bottom:1.5rem">
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> A/B Testing incluido</li>
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Optimizada para móviles</li>
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Carga ultra rápida</li>
        </ul>
        <button onclick="scrollToContact()" class="btn-secondary" style="width:100%;justify-content:center;font-size:.82rem">Solicitar →</button>
      </div>

      <div class="service-card" data-aos="fade-up" data-aos-delay="50">
        <div class="service-icon"><svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><circle cx="12" cy="12" r="10"/><path d="M2 12h20M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></svg></div>
        <h3 style="font-family:'Syne',sans-serif;font-weight:700;font-size:1.05rem;margin-bottom:.625rem">Sitios Corporativos</h3>
        <p style="font-size:.85rem;color:rgba(255,255,255,.45);line-height:1.7;margin-bottom:1.25rem">Presencia profesional que refleja la excelencia de tu marca y genera confianza institucional.</p>
        <ul style="font-size:.8rem;color:rgba(255,255,255,.4);list-style:none;display:flex;flex-direction:column;gap:.4rem;margin-bottom:1.5rem">
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Diseño premium personalizado</li>
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> CMS integrado</li>
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Multi-idioma disponible</li>
        </ul>
        <button onclick="scrollToContact()" class="btn-secondary" style="width:100%;justify-content:center;font-size:.82rem">Solicitar →</button>
      </div>

      <div class="service-card" data-aos="fade-up" data-aos-delay="100">
        <div class="service-icon"><svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M6 2L3 6v14a2 2 0 002 2h14a2 2 0 002-2V6l-3-4z"/><line x1="3" y1="6" x2="21" y2="6"/><path d="M16 10a4 4 0 01-8 0"/></svg></div>
        <h3 style="font-family:'Syne',sans-serif;font-weight:700;font-size:1.05rem;margin-bottom:.625rem">E-Commerce</h3>
        <p style="font-size:.85rem;color:rgba(255,255,255,.45);line-height:1.7;margin-bottom:1.25rem">Tiendas online de alto rendimiento integradas con pasarelas de pago y logística.</p>
        <ul style="font-size:.8rem;color:rgba(255,255,255,.4);list-style:none;display:flex;flex-direction:column;gap:.4rem;margin-bottom:1.5rem">
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Stripe / PayPal / MercadoPago</li>
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Panel de administración</li>
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Reportes y analytics</li>
        </ul>
        <button onclick="scrollToContact()" class="btn-secondary" style="width:100%;justify-content:center;font-size:.82rem">Solicitar →</button>
      </div>

      <div class="service-card" data-aos="fade-up" data-aos-delay="150">
        <div class="service-icon"><svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><rect x="5" y="2" width="14" height="20" rx="2"/><line x1="12" y1="18" x2="12.01" y2="18"/></svg></div>
        <h3 style="font-family:'Syne',sans-serif;font-weight:700;font-size:1.05rem;margin-bottom:.625rem">Aplicaciones Web</h3>
        <p style="font-size:.85rem;color:rgba(255,255,255,.45);line-height:1.7;margin-bottom:1.25rem">Aplicaciones escalables con arquitecturas modernas: React, Next.js, Node.js y microservicios.</p>
        <ul style="font-size:.8rem;color:rgba(255,255,255,.4);list-style:none;display:flex;flex-direction:column;gap:.4rem;margin-bottom:1.5rem">
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Arquitectura escalable</li>
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> API REST / GraphQL</li>
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> CI/CD pipelines</li>
        </ul>
        <button onclick="scrollToContact()" class="btn-secondary" style="width:100%;justify-content:center;font-size:.82rem">Solicitar →</button>
      </div>

      <div class="service-card" data-aos="fade-up" data-aos-delay="200">
        <div class="service-icon"><svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg></div>
        <h3 style="font-family:'Syne',sans-serif;font-weight:700;font-size:1.05rem;margin-bottom:.625rem">Sistemas Empresariales</h3>
        <p style="font-size:.85rem;color:rgba(255,255,255,.45);line-height:1.7;margin-bottom:1.25rem">ERP, CRM y sistemas a medida que automatizan y optimizan procesos críticos de negocio.</p>
        <ul style="font-size:.8rem;color:rgba(255,255,255,.4);list-style:none;display:flex;flex-direction:column;gap:.4rem;margin-bottom:1.5rem">
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Módulos personalizados</li>
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Reportes en tiempo real</li>
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Seguridad enterprise</li>
        </ul>
        <button onclick="scrollToContact()" class="btn-secondary" style="width:100%;justify-content:center;font-size:.82rem">Solicitar →</button>
      </div>

      <div class="service-card" data-aos="fade-up" data-aos-delay="250">
        <div class="service-icon"><svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><circle cx="12" cy="12" r="3"/><path d="M19.07 4.93l-1.41 1.41M6.34 17.66l-1.41 1.41M20 12h-2M6 12H4M17.66 17.66l-1.41-1.41M6.34 6.34L4.93 4.93"/></svg></div>
        <h3 style="font-family:'Syne',sans-serif;font-weight:700;font-size:1.05rem;margin-bottom:.625rem">Diseño UI/UX</h3>
        <p style="font-size:.85rem;color:rgba(255,255,255,.45);line-height:1.7;margin-bottom:1.25rem">Interfaces centradas en el usuario que combinan belleza visual con usabilidad excepcional.</p>
        <ul style="font-size:.8rem;color:rgba(255,255,255,.4);list-style:none;display:flex;flex-direction:column;gap:.4rem;margin-bottom:1.5rem">
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Research + wireframes</li>
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Prototipos interactivos</li>
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Design systems</li>
        </ul>
        <button onclick="scrollToContact()" class="btn-secondary" style="width:100%;justify-content:center;font-size:.82rem">Solicitar →</button>
      </div>

      <div class="service-card" data-aos="fade-up" data-aos-delay="300">
        <div class="service-icon"><svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M21 21l-6-6m2-5a7 7 0 1 1-14 0 7 7 0 0 1 14 0z"/></svg></div>
        <h3 style="font-family:'Syne',sans-serif;font-weight:700;font-size:1.05rem;margin-bottom:.625rem">SEO &amp; Marketing Digital</h3>
        <p style="font-size:.85rem;color:rgba(255,255,255,.45);line-height:1.7;margin-bottom:1.25rem">Posicionamiento orgánico y estrategia de contenidos para dominar los motores de búsqueda.</p>
        <ul style="font-size:.8rem;color:rgba(255,255,255,.4);list-style:none;display:flex;flex-direction:column;gap:.4rem;margin-bottom:1.5rem">
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Auditoría SEO técnico</li>
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Link building</li>
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Reportes mensuales</li>
        </ul>
        <button onclick="scrollToContact()" class="btn-secondary" style="width:100%;justify-content:center;font-size:.82rem">Solicitar →</button>
      </div>

      <div class="service-card" data-aos="fade-up" data-aos-delay="350">
        <div class="service-icon"><svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M18 20V10M12 20V4M6 20v-6"/></svg></div>
        <h3 style="font-family:'Syne',sans-serif;font-weight:700;font-size:1.05rem;margin-bottom:.625rem">Optimización de Rendimiento</h3>
        <p style="font-size:.85rem;color:rgba(255,255,255,.45);line-height:1.7;margin-bottom:1.25rem">Auditoría completa y optimización de Core Web Vitals. Lighthouse 90+ garantizado.</p>
        <ul style="font-size:.8rem;color:rgba(255,255,255,.4);list-style:none;display:flex;flex-direction:column;gap:.4rem;margin-bottom:1.5rem">
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Core Web Vitals</li>
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> CDN configuration</li>
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Caching avanzado</li>
        </ul>
        <button onclick="scrollToContact()" class="btn-secondary" style="width:100%;justify-content:center;font-size:.82rem">Solicitar →</button>
      </div>

      <div class="service-card" data-aos="fade-up" data-aos-delay="400">
        <div class="service-icon"><svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z"/></svg></div>
        <h3 style="font-family:'Syne',sans-serif;font-weight:700;font-size:1.05rem;margin-bottom:.625rem">Hosting &amp; Dominio</h3>
        <p style="font-size:.85rem;color:rgba(255,255,255,.45);line-height:1.7;margin-bottom:1.25rem">Infraestructura cloud de alta disponibilidad en AWS/Azure con SLA 99.9% uptime.</p>
        <ul style="font-size:.8rem;color:rgba(255,255,255,.4);list-style:none;display:flex;flex-direction:column;gap:.4rem;margin-bottom:1.5rem">
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> SSL gratuito</li>
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Backups diarios</li>
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Monitoreo 24/7</li>
        </ul>
        <button onclick="scrollToContact()" class="btn-secondary" style="width:100%;justify-content:center;font-size:.82rem">Solicitar →</button>
      </div>

      <div class="service-card" data-aos="fade-up" data-aos-delay="450">
        <div class="service-icon"><svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M8 6h13M8 12h13M8 18h13M3 6h.01M3 12h.01M3 18h.01"/></svg></div>
        <h3 style="font-family:'Syne',sans-serif;font-weight:700;font-size:1.05rem;margin-bottom:.625rem">Integración de APIs</h3>
        <p style="font-size:.85rem;color:rgba(255,255,255,.45);line-height:1.7;margin-bottom:1.25rem">Conecta tu plataforma con cualquier servicio externo: pagos, CRM, ERPs, redes sociales y más.</p>
        <ul style="font-size:.8rem;color:rgba(255,255,255,.4);list-style:none;display:flex;flex-direction:column;gap:.4rem;margin-bottom:1.5rem">
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> REST & GraphQL</li>
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> OAuth 2.0</li>
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Webhooks</li>
        </ul>
        <button onclick="scrollToContact()" class="btn-secondary" style="width:100%;justify-content:center;font-size:.82rem">Solicitar →</button>
      </div>

      <div class="service-card" data-aos="fade-up" data-aos-delay="500">
        <div class="service-icon"><svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M14.7 6.3a1 1 0 0 0 0 1.4l1.6 1.6a1 1 0 0 0 1.4 0l3.77-3.77a6 6 0 0 1-7.94 7.94l-6.91 6.91a2.12 2.12 0 0 1-3-3l6.91-6.91a6 6 0 0 1 7.94-7.94l-3.76 3.76z"/></svg></div>
        <h3 style="font-family:'Syne',sans-serif;font-weight:700;font-size:1.05rem;margin-bottom:.625rem">Mantenimiento Web</h3>
        <p style="font-size:.85rem;color:rgba(255,255,255,.45);line-height:1.7;margin-bottom:1.25rem">Planes de mantenimiento mensual para que tu sitio esté siempre actualizado, seguro y veloz.</p>
        <ul style="font-size:.8rem;color:rgba(255,255,255,.4);list-style:none;display:flex;flex-direction:column;gap:.4rem;margin-bottom:1.5rem">
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Actualizaciones de seguridad</li>
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Soporte prioritario</li>
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Reportes de rendimiento</li>
        </ul>
        <button onclick="scrollToContact()" class="btn-secondary" style="width:100%;justify-content:center;font-size:.82rem">Solicitar →</button>
      </div>

      <div class="service-card" data-aos="fade-up" data-aos-delay="550">
        <div class="service-icon"><svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M9 3H5a2 2 0 00-2 2v4m6-6h10a2 2 0 012 2v4M9 3v18m0 0h10a2 2 0 002-2V9M9 21H5a2 2 0 01-2-2V9m0 0h18"/></svg></div>
        <h3 style="font-family:'Syne',sans-serif;font-weight:700;font-size:1.05rem;margin-bottom:.625rem">Consultoría Tecnológica</h3>
        <p style="font-size:.85rem;color:rgba(255,255,255,.45);line-height:1.7;margin-bottom:1.25rem">Estrategia digital, auditoría tecnológica y hoja de ruta para la transformación digital de tu empresa.</p>
        <ul style="font-size:.8rem;color:rgba(255,255,255,.4);list-style:none;display:flex;flex-direction:column;gap:.4rem;margin-bottom:1.5rem">
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Tech stack advisory</li>
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Roadmap digital</li>
          <li style="display:flex;gap:.5rem;align-items:center"><span style="color:#10b897">✓</span> Due diligence tecnológico</li>
        </ul>
        <button onclick="scrollToContact()" class="btn-secondary" style="width:100%;justify-content:center;font-size:.82rem">Solicitar →</button>
      </div>
    </div>
  </div>
</section>

<!-- ===== TECHNOLOGIES ===== -->
<section id="technologies" class="section">
  <div class="container">
    <div style="text-align:center;max-width:600px;margin:0 auto 4rem" data-aos="fade-up">
      <p class="section-label">Stack Tecnológico</p>
      <h2 class="section-title"><span class="grad-text-2">Dominamos el</span><br/><span class="grad-text">ecosistema digital.</span></h2>
    </div>

    <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:2rem">

      <!-- Frontend -->
      <div class="glass" style="padding:2rem;border-radius:1.5rem" data-aos="fade-up">
        <h3 style="font-family:'Syne',sans-serif;font-weight:700;margin-bottom:1.5rem;display:flex;align-items:center;gap:.5rem"><span style="color:#10b897">⬡</span> Frontend</h3>
        <div id="tech-frontend" style="display:flex;flex-direction:column;gap:1rem"></div>
      </div>

      <!-- Backend -->
      <div class="glass" style="padding:2rem;border-radius:1.5rem" data-aos="fade-up" data-aos-delay="100">
        <h3 style="font-family:'Syne',sans-serif;font-weight:700;margin-bottom:1.5rem;display:flex;align-items:center;gap:.5rem"><span style="color:#a3ff57">⬡</span> Backend</h3>
        <div id="tech-backend" style="display:flex;flex-direction:column;gap:1rem"></div>
      </div>

      <!-- DB & Cloud -->
      <div style="display:flex;flex-direction:column;gap:2rem">
        <div class="glass" style="padding:2rem;border-radius:1.5rem" data-aos="fade-up" data-aos-delay="200">
          <h3 style="font-family:'Syne',sans-serif;font-weight:700;margin-bottom:1.5rem;display:flex;align-items:center;gap:.5rem"><span style="color:#10b897">⬡</span> Bases de Datos</h3>
          <div id="tech-db" style="display:flex;flex-direction:column;gap:1rem"></div>
        </div>
        <div class="glass" style="padding:2rem;border-radius:1.5rem" data-aos="fade-up" data-aos-delay="250">
          <h3 style="font-family:'Syne',sans-serif;font-weight:700;margin-bottom:1.5rem;display:flex;align-items:center;gap:.5rem"><span style="color:#a3ff57">⬡</span> Cloud &amp; Tools</h3>
          <div id="tech-cloud" style="display:flex;flex-direction:column;gap:1rem"></div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ===== PORTFOLIO ===== -->
<section id="portfolio" class="section" style="background:rgba(9,13,24,.6)">
  <div class="container">
    <div style="text-align:center;max-width:600px;margin:0 auto 3rem" data-aos="fade-up">
      <p class="section-label">Portafolio</p>
      <h2 class="section-title"><span class="grad-text-2">Trabajo que</span><br/><span class="grad-text">habla por sí solo.</span></h2>
    </div>

    <!-- Filters -->
    <div style="display:flex;flex-wrap:wrap;gap:.75rem;justify-content:center;margin-bottom:2.5rem" data-aos="fade-up" data-aos-delay="100">
      <button class="filter-btn active" data-filter="all">Todos</button>
      <button class="filter-btn" data-filter="ecommerce">E-Commerce</button>
      <button class="filter-btn" data-filter="corporate">Corporativo</button>
      <button class="filter-btn" data-filter="app">Aplicaciones</button>
      <button class="filter-btn" data-filter="landing">Landing Pages</button>
    </div>

    <!-- Grid -->
    <div id="portfolio-grid" style="display:grid;grid-template-columns:repeat(auto-fit,minmax(320px,1fr));gap:1.5rem"></div>

    <div style="text-align:center;margin-top:3rem" data-aos="fade-up">
      <button class="btn-secondary" onclick="scrollToContact()">Ver más proyectos →</button>
    </div>
  </div>
</section>

<!-- ===== TEAM ===== -->
<section id="team" class="section">
  <div class="container">
    <div style="text-align:center;max-width:600px;margin:0 auto 4rem" data-aos="fade-up">
      <p class="section-label">Nuestro Equipo</p>
      <h2 class="section-title"><span class="grad-text-2">Las mentes detrás</span><br/><span class="grad-text">de la magia.</span></h2>
      <p style="color:rgba(255,255,255,.45);line-height:1.8">Un equipo multidisciplinario de apasionados del diseño, el código y la estrategia digital.</p>
    </div>

    <div id="team-grid" style="display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:1.5rem"></div>
  </div>
</section>

<!-- ===== TESTIMONIALS ===== -->
<section id="testimonials" class="section" style="background:rgba(9,13,24,.6)">
  <div class="container">
    <div style="text-align:center;max-width:600px;margin:0 auto 4rem" data-aos="fade-up">
      <p class="section-label">Testimonios</p>
      <h2 class="section-title"><span class="grad-text-2">Lo que dicen</span><br/><span class="grad-text">nuestros clientes.</span></h2>
    </div>

    <div style="position:relative;overflow:hidden" data-aos="fade-up" data-aos-delay="100">
      <div id="testimonial-track" style="display:flex;gap:1.5rem;transition:transform .5s cubic-bezier(.4,0,.2,1)"></div>
    </div>

    <!-- Dots -->
    <div id="testimonial-dots" style="display:flex;justify-content:center;gap:.5rem;margin-top:2rem"></div>
  </div>
</section>

<!-- ===== FAQ ===== -->
<section id="faq" class="section">
  <div class="container">
    <div style="text-align:center;max-width:600px;margin:0 auto 4rem" data-aos="fade-up">
      <p class="section-label">FAQ</p>
      <h2 class="section-title"><span class="grad-text-2">Preguntas</span><br/><span class="grad-text">frecuentes.</span></h2>
    </div>

    <div style="max-width:760px;margin:0 auto;display:flex;flex-direction:column;gap:1rem" id="faq-container" data-aos="fade-up" data-aos-delay="100"></div>
  </div>
</section>

<!-- ===== CONTACT ===== -->
<section id="contact" class="section" style="background:rgba(9,13,24,.6)">
  <div class="orb" style="width:500px;height:500px;background:#10b897;bottom:-200px;right:-100px;opacity:.08"></div>
  <div class="container" style="position:relative;z-index:1">
    <div style="display:grid;grid-template-columns:1fr 1.5fr;gap:5rem;align-items:start">

      <!-- Left -->
      <div data-aos="fade-right">
        <p class="section-label">Contacto</p>
        <h2 class="section-title"><span class="grad-text-2">Hablemos de</span><br/><span class="grad-text">tu proyecto.</span></h2>
        <p style="color:rgba(255,255,255,.5);line-height:1.8;margin-bottom:2.5rem">Cuéntanos sobre tu idea y en menos de 24 horas recibirás una propuesta personalizada con costo, tiempos y roadmap.</p>

        <div style="display:flex;flex-direction:column;gap:1.5rem">
          <div style="display:flex;align-items:center;gap:1rem">
            <div style="width:44px;height:44px;background:rgba(16,184,151,.1);border:1px solid rgba(16,184,151,.2);border-radius:.75rem;display:flex;align-items:center;justify-content:center;flex-shrink:0"><svg width="20" height="20" fill="none" stroke="#10b897" stroke-width="2" viewBox="0 0 24 24"><path d="M22 16.92v3a2 2 0 01-2.18 2 19.79 19.79 0 01-8.63-3.07A19.5 19.5 0 013 5.86 2 2 0 015 3.68h3a2 2 0 012 1.72c.127.96.361 1.903.7 2.81a2 2 0 01-.45 2.11L9.09 11.53a16 16 0 006.29 6.29l1.23-1.23a2 2 0 012.11-.45c.907.339 1.85.573 2.81.7A2 2 0 0122 16.92z"/></svg></div>
            <div><p style="font-family:'Syne',sans-serif;font-weight:700;font-size:.88rem">Teléfono / WhatsApp</p><p style="font-size:.85rem;color:rgba(255,255,255,.45)">+1 (555) 000-0000</p></div>
          </div>
          <div style="display:flex;align-items:center;gap:1rem">
            <div style="width:44px;height:44px;background:rgba(16,184,151,.1);border:1px solid rgba(16,184,151,.2);border-radius:.75rem;display:flex;align-items:center;justify-content:center;flex-shrink:0"><svg width="20" height="20" fill="none" stroke="#10b897" stroke-width="2" viewBox="0 0 24 24"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg></div>
            <div><p style="font-family:'Syne',sans-serif;font-weight:700;font-size:.88rem">Email</p><p style="font-size:.85rem;color:rgba(255,255,255,.45)">hola@nexacore.studio</p></div>
          </div>
          <div style="display:flex;align-items:center;gap:1rem">
            <div style="width:44px;height:44px;background:rgba(16,184,151,.1);border:1px solid rgba(16,184,151,.2);border-radius:.75rem;display:flex;align-items:center;justify-content:center;flex-shrink:0"><svg width="20" height="20" fill="none" stroke="#10b897" stroke-width="2" viewBox="0 0 24 24"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"/><circle cx="12" cy="10" r="3"/></svg></div>
            <div><p style="font-family:'Syne',sans-serif;font-weight:700;font-size:.88rem">Dirección</p><p style="font-size:.85rem;color:rgba(255,255,255,.45)">1234 Innovation Drive, Suite 500<br/>Miami, FL 33101</p></div>
          </div>
        </div>

        <!-- Social -->
        <div style="margin-top:2.5rem">
          <p style="font-family:'Syne',sans-serif;font-size:.8rem;font-weight:700;color:rgba(255,255,255,.3);letter-spacing:.1em;text-transform:uppercase;margin-bottom:1rem">Síguenos</p>
          <div style="display:flex;gap:.75rem;flex-wrap:wrap">
            <a href="#" class="social-icon" title="Instagram" aria-label="Instagram"><svg width="18" height="18" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><rect x="2" y="2" width="20" height="20" rx="5"/><path d="M16 11.37A4 4 0 1112.63 8 4 4 0 0116 11.37z"/><line x1="17.5" y1="6.5" x2="17.51" y2="6.5"/></svg></a>
            <a href="#" class="social-icon" title="LinkedIn" aria-label="LinkedIn"><svg width="18" height="18" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M16 8a6 6 0 016 6v7h-4v-7a2 2 0 00-2-2 2 2 0 00-2 2v7h-4v-7a6 6 0 016-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg></a>
            <a href="#" class="social-icon" title="X / Twitter" aria-label="Twitter"><svg width="18" height="18" fill="currentColor" viewBox="0 0 24 24"><path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"/></svg></a>
            <a href="#" class="social-icon" title="Facebook" aria-label="Facebook"><svg width="18" height="18" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M18 2h-3a5 5 0 00-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 011-1h3z"/></svg></a>
            <a href="#" class="social-icon" title="YouTube" aria-label="YouTube"><svg width="18" height="18" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M22.54 6.42a2.78 2.78 0 00-1.95-1.96C18.88 4 12 4 12 4s-6.88 0-8.59.46a2.78 2.78 0 00-1.95 1.96A29 29 0 001 12a29 29 0 00.46 5.58A2.78 2.78 0 003.41 19.58C5.12 20 12 20 12 20s6.88 0 8.59-.46a2.78 2.78 0 001.95-1.95A29 29 0 0023 12a29 29 0 00-.46-5.58z"/><polygon points="9.75 15.02 15.5 12 9.75 8.98 9.75 15.02"/></svg></a>
            <a href="#" class="social-icon" title="GitHub" aria-label="GitHub"><svg width="18" height="18" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 00-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0020 4.77 5.07 5.07 0 0019.91 1S18.73.65 16 2.48a13.38 13.38 0 00-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 005 4.77a5.44 5.44 0 00-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 009 18.13V22"/></svg></a>
          </div>
        </div>

        <!-- Map -->
        <div style="margin-top:2rem;border-radius:1rem;overflow:hidden;border:1px solid rgba(255,255,255,.08)">
          <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d114967.23424082706!2d-80.3298!3d25.7617!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x88d9b0a20ec8c111%3A0xff96f271ddad4f65!2sMiami%2C%20FL!5e0!3m2!1sen!2sus!4v1234567890" width="100%" height="200" style="border:0;filter:grayscale(80%) invert(90%) hue-rotate(180deg)" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade" title="Ubicación NexaCore Studio"></iframe>
        </div>
      </div>

      <!-- Right: Form -->
      <div class="glass" style="padding:2.5rem;border-radius:1.5rem" data-aos="fade-left" data-aos-delay="100">
        <h3 style="font-family:'Syne',sans-serif;font-weight:700;font-size:1.3rem;margin-bottom:.5rem">Solicitar Cotización</h3>
        <p style="font-size:.85rem;color:rgba(255,255,255,.4);margin-bottom:2rem">Respuesta garantizada en menos de 24 horas hábiles.</p>

        <!-- Honeypot anti-spam field (hidden) -->
        <form id="contact-form" novalidate style="display:flex;flex-direction:column;gap:1.25rem">
          <input type="text" name="website_url" id="honeypot" style="display:none;visibility:hidden;position:absolute;left:-9999px" tabindex="-1" autocomplete="off" aria-hidden="true"/>

          <div style="display:grid;grid-template-columns:1fr 1fr;gap:1rem">
            <div class="form-group">
              <label class="form-label" for="fname">Nombre *</label>
              <input class="form-input" type="text" id="fname" name="fname" placeholder="Tu nombre" autocomplete="given-name" required maxlength="50"/>
              <span class="form-error" id="fname-err">Campo requerido</span>
            </div>
            <div class="form-group">
              <label class="form-label" for="lname">Apellido *</label>
              <input class="form-input" type="text" id="lname" name="lname" placeholder="Tu apellido" autocomplete="family-name" required maxlength="50"/>
              <span class="form-error" id="lname-err">Campo requerido</span>
            </div>
          </div>

          <div class="form-group">
            <label class="form-label" for="company">Empresa</label>
            <input class="form-input" type="text" id="company" name="company" placeholder="Nombre de tu empresa" maxlength="100"/>
          </div>

          <div style="display:grid;grid-template-columns:1fr 1fr;gap:1rem">
            <div class="form-group">
              <label class="form-label" for="email">Email *</label>
              <input class="form-input" type="email" id="email" name="email" placeholder="tu@email.com" autocomplete="email" required maxlength="100"/>
              <span class="form-error" id="email-err">Email inválido</span>
            </div>
            <div class="form-group">
              <label class="form-label" for="phone">Teléfono</label>
              <input class="form-input" type="tel" id="phone" name="phone" placeholder="+1 555 000 0000" autocomplete="tel" maxlength="20"/>
            </div>
          </div>

          <div class="form-group">
            <label class="form-label" for="service">Servicio Requerido *</label>
            <select class="form-input" id="service" name="service" required>
              <option value="">Selecciona un servicio...</option>
              <option>Landing Page</option>
              <option>Sitio Web Corporativo</option>
              <option>E-Commerce</option>
              <option>Aplicación Web</option>
              <option>Sistema Empresarial</option>
              <option>Diseño UI/UX</option>
              <option>SEO</option>
              <option>Mantenimiento Web</option>
              <option>Integración de APIs</option>
              <option>Hosting &amp; Dominio</option>
              <option>Consultoría Tecnológica</option>
              <option>Otro</option>
            </select>
            <span class="form-error" id="service-err">Selecciona un servicio</span>
          </div>

          <div class="form-group">
            <label class="form-label" for="budget">Presupuesto Estimado</label>
            <select class="form-input" id="budget" name="budget">
              <option value="">Selecciona tu presupuesto...</option>
              <option>Menos de $1,000</option>
              <option>$1,000 - $3,000</option>
              <option>$3,000 - $7,000</option>
              <option>$7,000 - $15,000</option>
              <option>$15,000 - $30,000</option>
              <option>Más de $30,000</option>
            </select>
          </div>

          <div class="form-group">
            <label class="form-label" for="message">Mensaje *</label>
            <textarea class="form-input" id="message" name="message" placeholder="Cuéntanos sobre tu proyecto, objetivos y cualquier detalle relevante..." rows="4" required maxlength="1000" style="resize:vertical"></textarea>
            <span class="form-error" id="message-err">El mensaje es requerido</span>
          </div>

          <button type="submit" class="btn-primary" style="justify-content:center;padding:1rem" id="submit-btn">
            <span id="submit-text">Enviar Solicitud</span>
            <svg id="submit-arrow" width="16" height="16" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><path d="M5 12h14m-7-7 7 7-7 7"/></svg>
          </button>

          <p style="font-size:.75rem;color:rgba(255,255,255,.3);text-align:center;line-height:1.6">🔒 Tu información es confidencial y nunca será compartida con terceros.</p>

          <!-- Success / Error messages -->
          <div id="form-success" style="display:none;background:rgba(16,184,151,.1);border:1px solid rgba(16,184,151,.3);border-radius:.75rem;padding:1rem;text-align:center">
            <p style="color:#10b897;font-family:'Syne',sans-serif;font-weight:700">✅ ¡Mensaje enviado!</p>
            <p style="font-size:.82rem;color:rgba(255,255,255,.5);margin-top:.25rem">Te contactaremos en menos de 24 horas.</p>
          </div>
          <div id="form-error-msg" style="display:none;background:rgba(239,68,68,.1);border:1px solid rgba(239,68,68,.3);border-radius:.75rem;padding:1rem;text-align:center">
            <p style="color:#ef4444;font-family:'Syne',sans-serif;font-weight:700">❌ Error al enviar</p>
            <p style="font-size:.82rem;color:rgba(255,255,255,.5);margin-top:.25rem">Por favor intenta nuevamente o escríbenos por WhatsApp.</p>
          </div>
        </form>
      </div>
    </div>
  </div>
</section>

<!-- ===== FOOTER ===== -->
<footer style="padding:5rem 0 2rem">
  <div class="container">
    <div style="display:grid;grid-template-columns:2fr 1fr 1fr 1fr;gap:3rem;margin-bottom:3rem" class="footer-grid">

      <!-- Brand -->
      <div>
        <a href="#hero" class="nav-logo" style="font-size:1.6rem;display:block;margin-bottom:1rem">Nexa<span>Core</span></a>
        <p style="font-size:.88rem;color:rgba(255,255,255,.4);line-height:1.8;max-width:300px;margin-bottom:1.5rem">Agencia de desarrollo web premium. Transformamos ideas en experiencias digitales de clase mundial que impulsan el crecimiento de tu negocio.</p>
        <div style="display:flex;gap:.75rem;flex-wrap:wrap">
          <a href="#" class="social-icon" aria-label="Instagram"><svg width="16" height="16" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><rect x="2" y="2" width="20" height="20" rx="5"/><path d="M16 11.37A4 4 0 1112.63 8 4 4 0 0116 11.37z"/><line x1="17.5" y1="6.5" x2="17.51" y2="6.5"/></svg></a>
          <a href="#" class="social-icon" aria-label="LinkedIn"><svg width="16" height="16" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M16 8a6 6 0 016 6v7h-4v-7a2 2 0 00-2-2 2 2 0 00-2 2v7h-4v-7a6 6 0 016-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg></a>
          <a href="#" class="social-icon" aria-label="GitHub"><svg width="16" height="16" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 00-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0020 4.77 5.07 5.07 0 0019.91 1S18.73.65 16 2.48a13.38 13.38 0 00-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 005 4.77a5.44 5.44 0 00-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 009 18.13V22"/></svg></a>
        </div>
      </div>

      <!-- Links -->
      <div>
        <p style="font-family:'Syne',sans-serif;font-weight:700;font-size:.88rem;margin-bottom:1.25rem;color:rgba(255,255,255,.8)">Empresa</p>
        <a href="#about" class="footer-link">Sobre Nosotros</a>
        <a href="#team" class="footer-link">Equipo</a>
        <a href="#portfolio" class="footer-link">Portafolio</a>
        <a href="#testimonials" class="footer-link">Testimonios</a>
        <a href="#" class="footer-link">Blog</a>
        <a href="#contact" class="footer-link">Contacto</a>
      </div>

      <div>
        <p style="font-family:'Syne',sans-serif;font-weight:700;font-size:.88rem;margin-bottom:1.25rem;color:rgba(255,255,255,.8)">Servicios</p>
        <a href="#services" class="footer-link">Landing Pages</a>
        <a href="#services" class="footer-link">Sitios Corporativos</a>
        <a href="#services" class="footer-link">E-Commerce</a>
        <a href="#services" class="footer-link">Apps Web</a>
        <a href="#services" class="footer-link">SEO</a>
        <a href="#services" class="footer-link">UI/UX Design</a>
      </div>

      <div>
        <p style="font-family:'Syne',sans-serif;font-weight:700;font-size:.88rem;margin-bottom:1.25rem;color:rgba(255,255,255,.8)">Contacto</p>
        <p class="footer-link" style="pointer-events:none">📧 hola@nexacore.studio</p>
        <p class="footer-link" style="pointer-events:none">📞 +1 (555) 000-0000</p>
        <p class="footer-link" style="pointer-events:none">📍 Miami, FL 33101</p>
        <div style="margin-top:1rem;padding:.75rem 1rem;background:rgba(16,184,151,.08);border:1px solid rgba(16,184,151,.2);border-radius:.75rem">
          <p style="font-family:'Syne',sans-serif;font-size:.75rem;font-weight:700;color:#10b897;margin-bottom:.25rem">🟢 Disponibles ahora</p>
          <p style="font-size:.75rem;color:rgba(255,255,255,.35)">Lun–Vie 9AM–6PM (EST)</p>
        </div>
      </div>
    </div>

    <!-- Divider -->
    <div style="border-top:1px solid rgba(255,255,255,.06);padding-top:2rem;display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:1rem">
      <p style="font-size:.8rem;color:rgba(255,255,255,.25)">© 2024 NexaCore Studio. Todos los derechos reservados.</p>
      <div style="display:flex;gap:1.5rem;flex-wrap:wrap">
        <a href="#" style="font-size:.8rem;color:rgba(255,255,255,.25);text-decoration:none;transition:color .2s" onmouseover="this.style.color='#10b897'" onmouseout="this.style.color='rgba(255,255,255,.25)'">Política de Privacidad</a>
        <a href="#" style="font-size:.8rem;color:rgba(255,255,255,.25);text-decoration:none;transition:color .2s" onmouseover="this.style.color='#10b897'" onmouseout="this.style.color='rgba(255,255,255,.25)'">Términos de Uso</a>
        <a href="#" style="font-size:.8rem;color:rgba(255,255,255,.25);text-decoration:none;transition:color .2s" onmouseover="this.style.color='#10b897'" onmouseout="this.style.color='rgba(255,255,255,.25)'">Cookies</a>
      </div>
    </div>
  </div>
</footer>

<!-- ===== WHATSAPP FLOAT ===== -->
<a id="wa-btn" href="https://wa.me/15550000000?text=Hola%2C%20me%20interesa%20cotizar%20un%20proyecto%20web." target="_blank" rel="noopener noreferrer" aria-label="Chatear por WhatsApp">
  <div id="wa-tooltip">💬 Chatea con nosotros</div>
  <svg width="28" height="28" viewBox="0 0 24 24" fill="white"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12 2C6.477 2 2 6.484 2 12.017c0 1.99.531 3.861 1.457 5.473L2 22l4.625-1.434C8.034 21.417 9.985 22 12 22c5.523 0 10-4.477 10-10S17.523 2 12 2zm0 18c-1.86 0-3.593-.516-5.064-1.41l-.36-.214-3.735 1.157 1.18-3.624-.235-.375A7.933 7.933 0 014 12c0-4.418 3.582-8 8-8s8 3.582 8 8-3.582 8-8 8z"/></svg>
</a>

<!-- ===== MODAL ===== -->
<div id="modal" role="dialog" aria-modal="true" aria-labelledby="modal-title">
  <div id="modal-bg" onclick="closeModal()"></div>
  <div id="modal-box">
    <div style="display:flex;justify-content:space-between;align-items:flex-start;margin-bottom:1.5rem">
      <h2 id="modal-title" style="font-family:'Syne',sans-serif;font-weight:800;font-size:1.5rem"></h2>
      <button onclick="closeModal()" style="background:rgba(255,255,255,.1);border:none;border-radius:.5rem;width:36px;height:36px;display:flex;align-items:center;justify-content:center;cursor:pointer;color:#fff;flex-shrink:0;margin-left:1rem">
        <svg width="16" height="16" fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><path d="M18 6L6 18M6 6l12 12"/></svg>
      </button>
    </div>
    <div id="modal-content"></div>
  </div>
</div>

<!-- ===== AOS ===== -->
<script src="https://unpkg.com/aos@2.3.4/dist/aos.js"></script>

<script>
// ========================
// SECURITY: Sanitize helper
// ========================
function sanitizeHTML(str) {
  const div = document.createElement('div');
  div.appendChild(document.createTextNode(String(str || '')));
  return div.innerHTML;
}

// ========================
// LOADER
// ========================
const loaderBar = document.getElementById('loader-bar');
const loader = document.getElementById('loader');
loaderBar.style.width = '100%';
setTimeout(() => { loader.classList.add('hidden'); }, 2200);

// ========================
// CUSTOM CURSOR
// ========================
const cursor = document.getElementById('cursor');
const cursorRing = document.getElementById('cursor-ring');
let cx = 0, cy = 0, rx = 0, ry = 0;
document.addEventListener('mousemove', e => {
  cx = e.clientX; cy = e.clientY;
  cursor.style.left = cx + 'px'; cursor.style.top = cy + 'px';
  cursorRing.style.left = cx + 'px'; cursorRing.style.top = cy + 'px';
});
document.querySelectorAll('a,button,.service-card,.team-card,.portfolio-card').forEach(el => {
  el.addEventListener('mouseenter', () => { cursor.style.transform = 'translate(-50%,-50%) scale(2)'; cursorRing.style.transform = 'translate(-50%,-50%) scale(1.5)'; });
  el.addEventListener('mouseleave', () => { cursor.style.transform = 'translate(-50%,-50%) scale(1)'; cursorRing.style.transform = 'translate(-50%,-50%) scale(1)'; });
});

// ========================
// NAVBAR SCROLL
// ========================
const navbar = document.getElementById('navbar');
window.addEventListener('scroll', () => {
  navbar.classList.toggle('scrolled', window.scrollY > 60);
}, { passive: true });

// ========================
// MOBILE MENU
// ========================
const menuBtn = document.getElementById('menu-btn');
const mobileMenu = document.getElementById('mobile-menu');
menuBtn.addEventListener('click', () => {
  mobileMenu.style.display = mobileMenu.style.display === 'none' ? 'block' : 'none';
});
function closeMobileMenu() { mobileMenu.style.display = 'none'; }

// ========================
// ANIMATED COUNTERS
// ========================
function animateCounter(el, target, suffix = '') {
  let start = 0;
  const duration = 2000;
  const step = target / (duration / 16);
  const timer = setInterval(() => {
    start = Math.min(start + step, target);
    el.textContent = Math.floor(start) + suffix;
    if (start >= target) clearInterval(timer);
  }, 16);
}
const counters = document.querySelectorAll('[data-count]');
const counterObs = new IntersectionObserver((entries) => {
  entries.forEach(e => {
    if (e.isIntersecting) {
      animateCounter(e.target, parseInt(e.target.dataset.count), e.target.dataset.suffix || '+');
      counterObs.unobserve(e.target);
    }
  });
}, { threshold: .5 });
counters.forEach(c => counterObs.observe(c));

// ========================
// TECHNOLOGIES DATA
// ========================
const techData = {
  frontend: [
    { name: 'React / Next.js', pct: 96 },
    { name: 'TypeScript', pct: 94 },
    { name: 'Vue.js / Nuxt', pct: 88 },
    { name: 'Tailwind CSS', pct: 97 },
    { name: 'Angular', pct: 82 },
  ],
  backend: [
    { name: 'Node.js / Express', pct: 95 },
    { name: 'Python / Django', pct: 88 },
    { name: 'PHP / Laravel', pct: 85 },
    { name: 'ASP.NET Core', pct: 80 },
  ],
  db: [
    { name: 'PostgreSQL / MySQL', pct: 93 },
    { name: 'MongoDB', pct: 90 },
    { name: 'SQL Server', pct: 82 },
  ],
  cloud: [
    { name: 'AWS / Azure', pct: 88 },
    { name: 'Docker / CI-CD', pct: 92 },
    { name: 'Figma', pct: 95 },
  ]
};

function renderTechSection(containerId, items) {
  const el = document.getElementById(containerId);
  if (!el) return;
  el.innerHTML = items.map(({ name, pct }) => `
    <div>
      <div style="display:flex;justify-content:space-between;margin-bottom:.4rem">
        <span style="font-family:'Syne',sans-serif;font-size:.82rem;font-weight:600;color:rgba(255,255,255,.75)">${sanitizeHTML(name)}</span>
        <span style="font-family:'Syne',sans-serif;font-size:.78rem;font-weight:700;color:#10b897">${sanitizeHTML(String(pct))}%</span>
      </div>
      <div class="prog-bar"><div class="prog-fill" style="--prog:${pct}%"></div></div>
    </div>
  `).join('');
}

renderTechSection('tech-frontend', techData.frontend);
renderTechSection('tech-backend', techData.backend);
renderTechSection('tech-db', techData.db);
renderTechSection('tech-cloud', techData.cloud);

// Animate progress bars on scroll
const progObs = new IntersectionObserver((entries) => {
  entries.forEach(e => {
    if (e.isIntersecting) {
      e.target.querySelectorAll('.prog-fill').forEach(b => b.classList.add('animated'));
      progObs.unobserve(e.target);
    }
  });
}, { threshold: .3 });
document.getElementById('technologies') && progObs.observe(document.getElementById('technologies'));

// ========================
// PORTFOLIO DATA
// ========================
const portfolioItems = [
  { title: 'NexaShop Commerce', cat: 'ecommerce', tags: ['Next.js', 'Stripe', 'Tailwind'], color: '#10b897', desc: 'Tienda online de moda premium con más de 500 SKUs, pasarela de pago integrada y panel de administración completo.', result: '+340% ventas en 6 meses' },
  { title: 'TechCorp Corporate', cat: 'corporate', tags: ['React', 'Node.js', 'AWS'], color: '#6366f1', desc: 'Sitio corporativo para empresa tecnológica de 300 empleados con sistema de careers y blog multiidioma.', result: '+180% leads orgánicos' },
  { title: 'FintraX Dashboard', cat: 'app', tags: ['Vue.js', 'D3.js', 'PostgreSQL'], color: '#f59e0b', desc: 'Plataforma de analítica financiera con dashboards en tiempo real y reportes exportables.', result: '50K usuarios activos' },
  { title: 'AeroLanding SaaS', cat: 'landing', tags: ['Next.js', 'Framer', 'Tailwind'], color: '#a3ff57', desc: 'Landing page de conversión para SaaS de gestión aeroportuaria con animaciones avanzadas.', result: '12% conversion rate' },
  { title: 'HealthHub App', cat: 'app', tags: ['React', 'Django', 'MongoDB'], color: '#ec4899', desc: 'Aplicación de telemedicina con videollamadas integradas, historial clínico y agenda médica.', result: '20K pacientes registrados' },
  { title: 'PropiaMedia E-Store', cat: 'ecommerce', tags: ['WooCommerce', 'PHP', 'MySQL'], color: '#14b8a6', desc: 'Marketplace de medios digitales con sistema de licencias y descarga automática.', result: '$1.2M en ventas año 1' },
];

function renderPortfolio(filter = 'all') {
  const grid = document.getElementById('portfolio-grid');
  const items = filter === 'all' ? portfolioItems : portfolioItems.filter(i => i.cat === filter);
  grid.innerHTML = items.map((item, i) => `
    <div class="portfolio-card" onclick="openModal('${sanitizeHTML(item.title)}', '${sanitizeHTML(item.desc)}', '${sanitizeHTML(item.result)}', '${sanitizeHTML(item.tags.join(','))}')"
         style="animation-delay:${i * 80}ms" data-aos="fade-up">
      <!-- Placeholder visual -->
      <div style="position:absolute;inset:0;background:linear-gradient(135deg,${sanitizeHTML(item.color)}15,rgba(9,13,24,.8));display:flex;align-items:center;justify-content:center">
        <div style="text-align:center;padding:2rem">
          <div style="width:60px;height:60px;background:${sanitizeHTML(item.color)}20;border:1px solid ${sanitizeHTML(item.color)}40;border-radius:1rem;display:flex;align-items:center;justify-content:center;margin:0 auto 1rem">
            <svg width="28" height="28" fill="none" stroke="${sanitizeHTML(item.color)}" stroke-width="1.5" viewBox="0 0 24 24"><rect x="3" y="3" width="18" height="18" rx="2"/><path d="M3 9h18"/><path d="M9 21V9"/></svg>
          </div>
          <p style="font-family:'Syne',sans-serif;font-weight:800;font-size:1.1rem;color:rgba(255,255,255,.9)">${sanitizeHTML(item.title)}</p>
          <p style="font-size:.75rem;margin-top:.5rem;color:${sanitizeHTML(item.color)};font-weight:700">${sanitizeHTML(item.result)}</p>
        </div>
      </div>
      <!-- Overlay -->
      <div class="portfolio-overlay">
        <div style="display:flex;flex-wrap:wrap;gap:.4rem;margin-bottom:.75rem">
          ${item.tags.map(t => `<span style="font-family:'Syne',sans-serif;font-size:.7rem;font-weight:700;padding:.2rem .6rem;background:rgba(255,255,255,.1);border-radius:100px;color:rgba(255,255,255,.7)">${sanitizeHTML(t)}</span>`).join('')}
        </div>
        <p style="font-family:'Syne',sans-serif;font-weight:700;font-size:1rem;margin-bottom:.25rem">${sanitizeHTML(item.title)}</p>
        <p style="font-size:.78rem;color:rgba(255,255,255,.55)">Ver detalles →</p>
      </div>
    </div>
  `).join('');
}

renderPortfolio();

// Filter buttons
document.querySelectorAll('.filter-btn').forEach(btn => {
  btn.addEventListener('click', function() {
    document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
    this.classList.add('active');
    renderPortfolio(this.dataset.filter);
  });
});

// ========================
// MODAL
// ========================
function openModal(title, desc, result, tagsStr) {
  const modal = document.getElementById('modal');
  document.getElementById('modal-title').textContent = title;
  const tags = tagsStr.split(',').map(t => `<span style="font-family:'Syne',sans-serif;font-size:.75rem;font-weight:700;padding:.3rem .75rem;background:rgba(16,184,151,.1);border:1px solid rgba(16,184,151,.25);border-radius:100px;color:#10b897">${sanitizeHTML(t)}</span>`).join('');
  document.getElementById('modal-content').innerHTML = `
    <p style="color:rgba(255,255,255,.6);line-height:1.8;margin-bottom:1.5rem">${sanitizeHTML(desc)}</p>
    <div style="background:rgba(16,184,151,.08);border:1px solid rgba(16,184,151,.2);border-radius:.75rem;padding:1rem;margin-bottom:1.5rem">
      <p style="font-family:'Syne',sans-serif;font-weight:700;font-size:.8rem;color:#10b897;margin-bottom:.25rem">RESULTADO</p>
      <p style="font-size:1.1rem;font-weight:700">${sanitizeHTML(result)}</p>
    </div>
    <div style="display:flex;flex-wrap:wrap;gap:.5rem;margin-bottom:2rem">${tags}</div>
    <button onclick="scrollToContact();closeModal();" class="btn-primary" style="justify-content:center;width:100%"><span>Quiero un proyecto similar</span></button>
  `;
  modal.classList.add('open');
  document.body.style.overflow = 'hidden';
}
function closeModal() {
  document.getElementById('modal').classList.remove('open');
  document.body.style.overflow = '';
}
document.addEventListener('keydown', e => { if (e.key === 'Escape') closeModal(); });

// ========================
// TEAM DATA
// ========================
const team = [
  { name: 'Alejandro Reyes', role: 'Fundador & CEO', exp: '15+ años', initials: 'AR', color: '#10b897', desc: 'Estratega digital y líder visionario. Especialista en arquitecturas web escalables y growth hacking.' },
  { name: 'María González', role: 'Co-Fundadora & COO', exp: '12+ años', initials: 'MG', color: '#6366f1', desc: 'Experta en operaciones y gestión de proyectos ágiles. Garante de la excelencia en cada entrega.' },
  { name: 'Carlos Mendoza', role: 'CTO', exp: '14+ años', initials: 'CM', color: '#f59e0b', desc: 'Arquitecto de software y cloud. Expert en AWS, microservicios y performance engineering.' },
  { name: 'Sofía Ramírez', role: 'Lead UI/UX Designer', exp: '10+ años', initials: 'SR', color: '#ec4899', desc: 'Diseñadora de experiencias centrada en el usuario. Egresada de RISD, ex-Google Design.' },
  { name: 'Daniel Torres', role: 'Senior Frontend Dev', exp: '8+ años', initials: 'DT', color: '#a3ff57', desc: 'Especialista en React/Next.js y animaciones avanzadas. Contributor de proyectos open source.' },
  { name: 'Ana Flores', role: 'Senior Backend Dev', exp: '9+ años', initials: 'AF', color: '#14b8a6', desc: 'Arquitecta de APIs REST y GraphQL. Experta en seguridad web y bases de datos distribuidas.' },
  { name: 'Roberto Silva', role: 'SEO Specialist', exp: '7+ años', initials: 'RS', color: '#f97316', desc: 'Estratega SEO certificado por Google. Especialista en Core Web Vitals y marketing de contenidos.' },
  { name: 'Valentina Cruz', role: 'UI/UX Designer', exp: '6+ años', initials: 'VC', color: '#8b5cf6', desc: 'Diseñadora de interfaces con enfoque en conversión y accesibilidad WCAG. Figma expert.' },
];

const teamGrid = document.getElementById('team-grid');
teamGrid.innerHTML = team.map((m, i) => `
  <div class="team-card" data-aos="fade-up" data-aos-delay="${i * 60}">
    <!-- Avatar placeholder with initials -->
    <div style="aspect-ratio:1;display:flex;align-items:center;justify-content:center;background:linear-gradient(135deg,${sanitizeHTML(m.color)}20,${sanitizeHTML(m.color)}08);border-bottom:1px solid rgba(255,255,255,.06)">
      <div style="width:90px;height:90px;background:${sanitizeHTML(m.color)}18;border:2px solid ${sanitizeHTML(m.color)}40;border-radius:50%;display:flex;align-items:center;justify-content:center;font-family:'Syne',sans-serif;font-weight:800;font-size:1.8rem;color:${sanitizeHTML(m.color)}">${sanitizeHTML(m.initials)}</div>
    </div>
    <div style="padding:1.5rem">
      <p style="font-family:'Syne',sans-serif;font-weight:700;font-size:1rem;margin-bottom:.2rem">${sanitizeHTML(m.name)}</p>
      <p style="font-size:.8rem;color:${sanitizeHTML(m.color)};font-weight:600;margin-bottom:.75rem">${sanitizeHTML(m.role)}</p>
      <p style="font-size:.8rem;color:rgba(255,255,255,.4);line-height:1.6;margin-bottom:1rem">${sanitizeHTML(m.desc)}</p>
      <div style="display:flex;align-items:center;justify-content:space-between">
        <span style="font-family:'Syne',sans-serif;font-size:.75rem;font-weight:700;padding:.25rem .75rem;background:rgba(255,255,255,.05);border-radius:100px;color:rgba(255,255,255,.4)">⏱ ${sanitizeHTML(m.exp)}</span>
        <div style="display:flex;gap:.5rem">
          <a href="#" class="social-icon" style="width:30px;height:30px;border-radius:.5rem" aria-label="LinkedIn de ${sanitizeHTML(m.name)}"><svg width="14" height="14" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M16 8a6 6 0 016 6v7h-4v-7a2 2 0 00-2-2 2 2 0 00-2 2v7h-4v-7a6 6 0 016-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg></a>
          <a href="#" class="social-icon" style="width:30px;height:30px;border-radius:.5rem" aria-label="Twitter de ${sanitizeHTML(m.name)}"><svg width="14" height="14" fill="currentColor" viewBox="0 0 24 24"><path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"/></svg></a>
        </div>
      </div>
    </div>
  </div>
`).join('');

// ========================
// TESTIMONIALS DATA
// ========================
const testimonials = [
  { name: 'Carlos Méndez', company: 'TechCorp CEO', initials: 'CM', color: '#10b897', rating: 5, text: 'NexaCore transformó completamente nuestra presencia digital. El sitio web que desarrollaron superó todas nuestras expectativas en diseño y rendimiento. Nuestras conversiones aumentaron un 340% en los primeros 3 meses.' },
  { name: 'Laura Jiménez', company: 'AeroStore CMO', initials: 'LJ', color: '#6366f1', rating: 5, text: 'El equipo de NexaCore es absolutamente excepcional. Entregaron nuestro e-commerce en tiempo récord, con una calidad de código impecable y un diseño que enamoró a todos nuestros clientes.' },
  { name: 'Andrés Morales', company: 'FintraX Founder', initials: 'AM', color: '#f59e0b', rating: 5, text: 'Trabajar con NexaCore fue una experiencia increíble. Son profesionales, transparentes y realmente saben lo que hacen. El dashboard que construyeron maneja millones de transacciones sin problemas.' },
  { name: 'Isabella Santos', company: 'PropiaMedia CEO', initials: 'IS', color: '#ec4899', rating: 5, text: 'Llevamos 3 proyectos con NexaCore y cada uno mejor que el anterior. Su atención al detalle y comprensión del negocio es única. Los recomiendo sin dudarlo.' },
  { name: 'Ricardo Vargas', company: 'HealthHub CTO', initials: 'RV', color: '#14b8a6', rating: 5, text: 'La app de telemedicina que desarrollaron para nosotros es robusta, segura y hermosa. El código es limpio y escalable. Pasamos de 0 a 20,000 usuarios en 6 meses.' },
  { name: 'Natalia Perez', company: 'Cloudify Startup', initials: 'NP', color: '#a3ff57', rating: 5, text: 'Como startup, necesitábamos una landing page que convirtiera desde el día uno. NexaCore la entregó en 10 días y alcanzamos 12% de conversion rate. Absolutamente extraordinario.' },
  { name: 'Fernando López', company: 'Orbis AI Director', initials: 'FL', color: '#8b5cf6', rating: 5, text: 'El nivel técnico y creativo del equipo es de clase mundial. Construyeron nuestro sistema de IA en tiempo récord y con la arquitectura perfecta. Son nuestros socios tecnológicos de confianza.' },
  { name: 'Camila Rojas', company: 'Nexabit CMO', initials: 'CR', color: '#f97316', rating: 5, text: 'El SEO que implementaron disparó nuestro tráfico orgánico un 280% en 4 meses. Pero más allá de los números, la calidad de su trabajo y atención al cliente es inigualable. Son los mejores.' },
];

const track = document.getElementById('testimonial-track');
const dotsEl = document.getElementById('testimonial-dots');
let tIdx = 0;

track.innerHTML = testimonials.map((t, i) => `
  <div class="testimonial-card" style="min-width:min(380px, 85vw)">
    <div style="display:flex;gap:.75rem;align-items:center;margin-bottom:1.25rem">
      <div style="width:48px;height:48px;background:${sanitizeHTML(t.color)}18;border:2px solid ${sanitizeHTML(t.color)}40;border-radius:50%;display:flex;align-items:center;justify-content:center;font-family:'Syne',sans-serif;font-weight:800;font-size:1rem;color:${sanitizeHTML(t.color)};flex-shrink:0">${sanitizeHTML(t.initials)}</div>
      <div>
        <p style="font-family:'Syne',sans-serif;font-weight:700;font-size:.9rem">${sanitizeHTML(t.name)}</p>
        <p style="font-size:.78rem;color:rgba(255,255,255,.4)">${sanitizeHTML(t.company)}</p>
      </div>
      <div style="margin-left:auto;color:#f59e0b;font-size:.9rem">★★★★★</div>
    </div>
    <p style="font-size:.88rem;color:rgba(255,255,255,.55);line-height:1.8">"${sanitizeHTML(t.text)}"</p>
  </div>
`).join('');

// Dots
dotsEl.innerHTML = testimonials.slice(0, Math.ceil(testimonials.length / 2)).map((_, i) => `
  <button onclick="goToTestimonial(${i})" style="width:8px;height:8px;border-radius:50%;border:none;cursor:pointer;transition:all .3s;background:${i === 0 ? '#10b897' : 'rgba(255,255,255,.15)'}" id="tdot-${i}" aria-label="Ir a testimonio ${i + 1}"></button>
`).join('');

function goToTestimonial(idx) {
  tIdx = idx;
  const cardW = 380 + 24; // width + gap
  track.style.transform = `translateX(-${tIdx * cardW}px)`;
  document.querySelectorAll('[id^=tdot-]').forEach((d, i) => {
    d.style.background = i === tIdx ? '#10b897' : 'rgba(255,255,255,.15)';
    d.style.width = i === tIdx ? '24px' : '8px';
    d.style.borderRadius = '4px';
  });
}

setInterval(() => {
  tIdx = (tIdx + 1) % Math.ceil(testimonials.length / 2);
  goToTestimonial(tIdx);
}, 4500);

// ========================
// FAQ DATA
// ========================
const faqs = [
  { q: '¿Cuánto cuesta una página web?', a: 'Los precios varían según la complejidad del proyecto. Una landing page de alta conversión puede comenzar desde $800. Un sitio corporativo completo oscila entre $3,000 y $12,000. Un e-commerce o aplicación web personalizada puede ir de $8,000 en adelante. Te enviamos una propuesta detallada y sin compromisos en menos de 24 horas.' },
  { q: '¿Cuánto tarda el desarrollo?', a: 'El tiempo depende del alcance. Una landing page puede estar lista en 5-7 días hábiles. Un sitio corporativo toma entre 3 y 6 semanas. Un e-commerce completo entre 4 y 10 semanas. Trabajamos con metodologías ágiles y te mantenemos informado con updates semanales a través de nuestra plataforma de gestión.' },
  { q: '¿Incluyen hosting y dominio?', a: 'Sí. Ofrecemos planes de hosting en servidores AWS o Azure de alta disponibilidad con SLA del 99.9%. También incluimos gestión de dominios, certificado SSL, backups diarios automáticos y monitoreo 24/7. Puedes optar por nuestros planes de hosting o usar tu proveedor preferido.' },
  { q: '¿Ofrecen soporte post-lanzamiento?', a: 'Absolutamente. Todos nuestros proyectos incluyen 30 días de soporte gratuito post-lanzamiento. Además, contamos con planes de mantenimiento mensual que incluyen actualizaciones de seguridad, optimizaciones de rendimiento, pequeñas modificaciones y soporte técnico prioritario vía WhatsApp y email.' },
  { q: '¿Trabajan con clientes internacionales?', a: 'Sí, trabajamos con clientes en toda Latinoamérica, Estados Unidos, España y Europa. Manejamos proyectos completamente en remoto con procesos transparentes y reuniones virtuales periódicas. Aceptamos pagos en USD, EUR y monedas locales.' },
  { q: '¿Aceptan pagos fraccionados?', a: 'Sí. Nuestro esquema de pago estándar es 50% al inicio del proyecto y 50% al lanzamiento. Para proyectos mayores a $5,000, ofrecemos planes de pago en 3 o 4 cuotas. Aceptamos transferencia bancaria, tarjetas de crédito, PayPal y criptomonedas.' },
  { q: '¿Incluyen optimización SEO?', a: 'Todos nuestros proyectos incluyen SEO técnico básico: estructura semántica correcta, meta tags optimizados, Open Graph, sitemap, robots.txt, optimización de velocidad y Core Web Vitals. Para estrategias SEO avanzadas (link building, contenidos, posicionamiento competitivo), ofrecemos planes mensuales especializados.' },
  { q: '¿Puedo ver el progreso del proyecto?', a: 'Por supuesto. Utilizamos herramientas de gestión de proyectos como Notion o Linear donde puedes ver en tiempo real el avance de tu proyecto, revisar entregables, aprobar diseños y comunicarte directamente con el equipo. Además, realizamos presentaciones semanales de avance por videollamada.' },
];

const faqContainer = document.getElementById('faq-container');
faqContainer.innerHTML = faqs.map((f, i) => `
  <div class="faq-item" id="faq-${i}">
    <button class="faq-btn" onclick="toggleFaq(${i})" aria-expanded="false" aria-controls="faqbody-${i}">
      <span>${sanitizeHTML(f.q)}</span>
      <span class="faq-icon"><svg width="10" height="10" fill="none" stroke="currentColor" stroke-width="3" viewBox="0 0 24 24"><path d="M12 5v14M5 12h14"/></svg></span>
    </button>
    <div class="faq-body" id="faqbody-${i}" role="region"><p>${sanitizeHTML(f.a)}</p></div>
  </div>
`).join('');

function toggleFaq(idx) {
  const item = document.getElementById('faq-' + idx);
  const body = document.getElementById('faqbody-' + idx);
  const btn = item.querySelector('.faq-btn');
  const isOpen = item.classList.contains('open');
  // Close all
  document.querySelectorAll('.faq-item').forEach(el => {
    el.classList.remove('open');
    el.querySelector('.faq-body').classList.remove('open');
    el.querySelector('.faq-btn').setAttribute('aria-expanded', 'false');
  });
  if (!isOpen) {
    item.classList.add('open');
    body.classList.add('open');
    btn.setAttribute('aria-expanded', 'true');
  }
}

// ========================
// CONTACT FORM
// ========================
function escapeForDisplay(str) {
  return String(str || '').replace(/&/g, '&amp;').replace(/</g, '&lt;').replace(/>/g, '&gt;').replace(/"/g, '&quot;').replace(/'/g, '&#39;');
}

// Real-time validation
const emailRe = /^[a-zA-Z0-9._%+\-]+@[a-zA-Z0-9.\-]+\.[a-zA-Z]{2,}$/;
const nameRe = /^[a-zA-ZÀ-ÖØ-öø-ÿ\s'-]{1,50}$/;

function setFieldError(id, show, msg) {
  const input = document.getElementById(id);
  const err = document.getElementById(id + '-err');
  if (!input || !err) return;
  if (show) {
    input.classList.add('error');
    err.textContent = msg;
    err.classList.add('show');
  } else {
    input.classList.remove('error');
    err.classList.remove('show');
  }
}

['fname', 'lname', 'email', 'service', 'message'].forEach(id => {
  const el = document.getElementById(id);
  if (!el) return;
  el.addEventListener('blur', () => validateField(id));
  el.addEventListener('input', () => { if (el.classList.contains('error')) validateField(id); });
});

function validateField(id) {
  const val = (document.getElementById(id)?.value || '').trim();
  if (id === 'fname' || id === 'lname') {
    if (!val) { setFieldError(id, true, 'Campo requerido'); return false; }
    if (!nameRe.test(val)) { setFieldError(id, true, 'Solo letras y espacios'); return false; }
    setFieldError(id, false); return true;
  }
  if (id === 'email') {
    if (!val) { setFieldError(id, true, 'Email requerido'); return false; }
    if (!emailRe.test(val)) { setFieldError(id, true, 'Email inválido'); return false; }
    setFieldError(id, false); return true;
  }
  if (id === 'service') {
    if (!val) { setFieldError(id, true, 'Selecciona un servicio'); return false; }
    setFieldError(id, false); return true;
  }
  if (id === 'message') {
    if (!val || val.length < 10) { setFieldError(id, true, 'Mínimo 10 caracteres'); return false; }
    setFieldError(id, false); return true;
  }
  return true;
}

document.getElementById('contact-form').addEventListener('submit', function(e) {
  e.preventDefault();

  // Honeypot check (anti-spam)
  if (document.getElementById('honeypot').value !== '') return;

  const fields = ['fname', 'lname', 'email', 'service', 'message'];
  const valid = fields.every(f => validateField(f));
  if (!valid) return;

  // Rate limiting (client-side basic)
  const lastSubmit = parseInt(sessionStorage.getItem('last_submit') || '0');
  if (Date.now() - lastSubmit < 30000) {
    alert('Por favor espera 30 segundos antes de enviar otro mensaje.');
    return;
  }

  const btn = document.getElementById('submit-btn');
  const txt = document.getElementById('submit-text');
  btn.disabled = true;
  txt.textContent = 'Enviando...';

  // Simulate API call (replace with real endpoint)
  setTimeout(() => {
    sessionStorage.setItem('last_submit', Date.now());
    btn.disabled = false;
    txt.textContent = 'Enviar Solicitud';
    document.getElementById('contact-form').reset();
    document.getElementById('form-success').style.display = 'block';
    setTimeout(() => { document.getElementById('form-success').style.display = 'none'; }, 6000);
  }, 1800);
});

// ========================
// SCROLL TO CONTACT
// ========================
function scrollToContact() {
  document.getElementById('contact').scrollIntoView({ behavior: 'smooth' });
}

// ========================
// AOS INIT
// ========================
AOS.init({ duration: 700, easing: 'ease-out-cubic', once: true, offset: 60 });

// ========================
// SMOOTH ACTIVE NAV
// ========================
const sections = ['hero','about','services','technologies','portfolio','team','testimonials','faq','contact'];
const navLinks = document.querySelectorAll('.nav-link');
const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      navLinks.forEach(link => {
        link.style.color = link.getAttribute('href') === '#' + entry.target.id ? '#10b897' : 'rgba(255,255,255,.7)';
      });
    }
  });
}, { threshold: .3 });
sections.forEach(id => { const el = document.getElementById(id); if (el) observer.observe(el); });

// ========================
// HERO RESPONSIVE FIX
// ========================
function fixHeroLayout() {
  const heroGridLayout = document.querySelector('.hero-grid-layout');
  const footerGrid = document.querySelector('.footer-grid');
  if (!heroGridLayout || !footerGrid) return;
  if (window.innerWidth < 900) {
    heroGridLayout.style.gridTemplateColumns = '1fr';
    footerGrid.style.gridTemplateColumns = 'repeat(2, 1fr)';
  } else {
    heroGridLayout.style.gridTemplateColumns = '1fr 1fr';
    footerGrid.style.gridTemplateColumns = '2fr 1fr 1fr 1fr';
  }
  if (window.innerWidth < 560) {
    footerGrid.style.gridTemplateColumns = '1fr';
  }
}
fixHeroLayout();
window.addEventListener('resize', fixHeroLayout, { passive: true });

console.log('%cNexaCore Studio', 'color:#10b897;font-size:2rem;font-weight:900;font-family:Syne');
console.log('%c🚀 Desarrollo web premium — hola@nexacore.studio', 'color:#a3ff57;font-size:.9rem');
</script>
</body>
</html>”