<!doctype html>
<html lang="pt-BR">
 <head><script>window["__codeletBootstrap__"]=JSON.parse('{"A":"A","B":"20260824-05-39521aa","C":{"Abril Fatface":"YACgEZbkUVE,0","Alfa Slab One":"YACgEYS9sJU,0","Anton":"YACgEcYqQ-A,0","Archivo":"YAHO2-t-jNE,0","Arial":"YAGyDvJ_4Ts,0","Bebas Neue":"YACgESME5ew,0","Bricolage Grotesque":"YAFyMcdwzpc,0","Canva Sans":"YAFLd8sKbwc,2","Caveat":"YALBs2ploWQ,0","Comic Sans MS":"YAHO2VMiyZo,0","Cormorant Garamond":"YAFdJhX-538,0","Courier New":"YAGzXiGs0_8,0","DM Sans":"YAD1aU3sLnI,0","DM Serif Display":"YAD1aYG82rc,0","Forum":"YACgEcnnqB4,0","Fraunces":"YAEul-FRQw4,0","Georgia":"YAGzXkO0pEM,0","Helvetica Neue":"YAFcf6CtJfI,0","Impact":"YAFcfnjI7Vk,0","Inter":"YAFdJvSyp_k,3","Iowan Old Style":"YAGNIFa8j9o,0","Jacques Francois":"YAHO2a5g66Q,0","JetBrains Mono":"YAFdJksXcAk,0","Libre Baskerville":"YACgEUFdPdA,0","Manrope":"YAHO2b2feC4,0","Merriweather":"YACgEXvHxxs,0","Montserrat":"YADLjI9qxTA,0","Nunito":"YACgEX8C5Gg,0","Oleo Script":"YACgEQQ14jI,0","Phantom Sans":"YAHO2E8Pb88,0","Playfair Display":"YACgEYmuCJE,0","Poppins":"YAFdJjbTu24,1","Press Start 2P":"YAFyGr-8pmQ,0","Quicksand":"YADWjpfPmdk,0","Raleway":"YACgEVg3xZg,0","Segoe UI":"YAHNdRD1Klw,0","Source Sans 3":"YAG4lO1Mj10,0","Spectral":"YAHO2rVUHIM,0","Times New Roman":"YAGzXW3gftg,0","Times":"YAGzXW3gftg,0","Ubuntu":"YACgERDU--Q,0","Work Sans":"YAGXhLOKv44,0","Yellowtail":"YACgEYG4kG4,0","ui-monospace":"YADlN8CFZ8Q,0","ui-sans-serif":"YACkoN-xg4g,0"}}');</script><script src="/_sdk/50d846425a1e5082.telemetry_sdk.js" integrity="sha512-Otbex+ztlVbcEGql0rXGd/3E3ee/hqAntg6DeuUEMG6pIPbXGOSvZbFZVzknAXi1tH/itQ+ijEhOTr2aWj6CXg=="></script>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sistema Térmico e Parâmetros Climáticos por CEP</title>
  <script src="https://cdn.tailwindcss.com/3.4.17"></script>
  <script src="https://cdn.jsdelivr.net/npm/lucide@0.263.0/dist/umd/lucide.min.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&amp;family=Fraunces:opsz,wght@9..144,600;9..144,700&amp;display=swap" rel="stylesheet">
  <style>
    :root {
      --rose-950: #4c102f;
      --rose-900: #741342;
      --rose-700: #be185d;
      --rose-600: #db2777;
      --rose-200: #fbcfe8;
      --rose-100: #fce7f3;
      --cream: #fff8fb;
      --ink: #321021;
    }

    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      width: 100%;
      margin: 0;
      color: var(--ink);
      font-family: "DM Sans", sans-serif;
      overflow-x: hidden;
    }

    .site-shell { width: 100%; }
    .display-font { font-family: "Fraunces", serif; }

    .soft-grid {
      background-image:
        linear-gradient(rgba(190, 24, 93, .055) 1px, transparent 1px),
        linear-gradient(90deg, rgba(190, 24, 93, .055) 1px, transparent 1px);
      background-size: 32px 32px;
    }

    .hero-orb {
      position: absolute;
      width: 34rem;
      height: 34rem;
      border-radius: 999px;
      background: radial-gradient(circle, rgba(251, 207, 232, .96), rgba(251, 207, 232, 0));
      filter: blur(8px);
      pointer-events: none;
    }

    .nav-link {
      color: #70133f;
      font-weight: 600;
      transition: color .2s ease;
    }

    .nav-link:hover { color: #ec4899; }

    .pink-button {
      background: #be185d;
      color: #fff;
      box-shadow: 0 10px 22px rgba(190, 24, 93, .24);
      transition: transform .2s ease, box-shadow .2s ease, background .2s ease;
    }

    .pink-button:hover:not(:disabled) {
      background: #9d174d;
      transform: translateY(-2px);
      box-shadow: 0 14px 26px rgba(190, 24, 93, .32);
    }

    .pink-button:disabled { cursor: not-allowed; opacity: .7; }

    .photo-frame { position: relative; overflow: hidden; }
    .photo-frame::after {
      content: "";
      position: absolute;
      inset: 0;
      background: linear-gradient(145deg, rgba(76, 16, 47, .28), transparent 55%);
      pointer-events: none;
    }

    .lift-card { transition: transform .25s ease, box-shadow .25s ease; }
    .lift-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 18px 34px rgba(103, 19, 63, .12);
    }

    .mobile-menu { display: none; }
    .mobile-menu.is-open { display: flex; }

    .metric-card {
      border: 1px solid #fbcfe8;
      background: #fff;
      border-radius: 1rem;
      padding: 1rem;
    }

    .metric-value {
      color: #4c102f;
      font-family: "Fraunces", serif;
      font-size: 1.55rem;
      font-weight: 700;
      line-height: 1.1;
    }

    .status-dot {
      width: .7rem;
      height: .7rem;
      flex: 0 0 auto;
      border-radius: 999px;
      background: #f59e0b;
      box-shadow: 0 0 0 5px rgba(245, 158, 11, .14);
      transition: background .25s ease, box-shadow .25s ease;
    }

    .status-dot.is-success {
      background: #22c55e;
      box-shadow: 0 0 0 5px rgba(34, 197, 94, .14);
    }

    .status-dot.is-error {
      background: #ef4444;
      box-shadow: 0 0 0 5px rgba(239, 68, 68, .14);
    }

    .status-dot.is-loading {
      animation: pulse 1s ease-in-out infinite;
    }

    button:focus-visible,
    a:focus-visible,
    input:focus-visible {
      outline: 3px solid #831843;
      outline-offset: 3px;
    }

    @keyframes rise {
      from { opacity: 0; transform: translateY(18px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes pulse {
      0%, 100% { transform: scale(1); opacity: 1; }
      50% { transform: scale(.72); opacity: .55; }
    }

    .reveal { animation: rise .7s ease both; }
    .delay-1 { animation-delay: .12s; }
    .delay-2 { animation-delay: .24s; }

    @media (max-width: 767px) {
      .desktop-nav { display: none; }
      .menu-toggle { display: inline-flex; }
      .hero-orb { width: 22rem; height: 22rem; }
    }

    @media (min-width: 768px) {
      .menu-toggle { display: none; }
    }
  </style>
  <script src="/_sdk/b3bf9e8ac58e6ad6.data_sdk.js" type="text/javascript" integrity="sha512-otc1u9NYq9Ms5Jt//7vmhrrqR5CLPr8Jdgs6741gqniClfLMcfmC+jK/cKuQdhLv6G0esJ/FzaMS9tv0T/vj/Q=="></script>
  <script src="/_sdk/a27879be4562f807.resizing_sdk.js" type="text/javascript" integrity="sha512-trcxRwz+QLrzK0Dqg95xqVRryR7WtWui2YopXyzOIr3WMde3j/xCRgT63/b/EAg7klDsAOuHzoRgoryhwm8QFw=="></script>
 </head>
 <body data-template-id="__page-root">
  <div class="site-shell">
   <header data-template-id="site-header" class="canva-header sticky top-0 z-50 border-b border-pink-100 bg-[#fff8fb]/95 backdrop-blur">
    <nav class="mx-auto flex max-w-7xl items-center justify-between px-5 py-4 lg:px-8" aria-label="Navegação principal"><a href="#inicio" class="flex items-center gap-3 rounded-lg"> <span class="flex h-10 w-10 items-center justify-center rounded-full bg-pink-700 text-white" aria-hidden="true"> <i data-lucide="waves" class="h-5 w-5"></i> </span> <span data-template-id="brand-name" class="canva-text text-sm font-bold tracking-wide text-pink-950"></span> </a>
     <div class="desktop-nav flex items-center gap-7 text-sm"><a class="nav-link" href="#balanco">Balanço térmico</a> <a class="nav-link" href="#tecnologias">Tecnologias</a> <a class="nav-link" href="#integracao">Integração CEP</a> <a class="nav-link" href="#demonstrador">Simulador</a>
     </div><button id="menu-toggle" type="button" class="menu-toggle rounded-lg p-2 text-pink-900" aria-label="Abrir menu" aria-expanded="false" aria-controls="mobile-menu"> <i data-lucide="menu" class="h-6 w-6"></i> </button>
    </nav>
    <div id="mobile-menu" class="mobile-menu flex-col gap-4 border-t border-pink-100 px-6 py-5 text-sm"><a class="nav-link" href="#balanco">Balanço térmico</a> <a class="nav-link" href="#tecnologias">Tecnologias</a> <a class="nav-link" href="#integracao">Integração CEP</a> <a class="nav-link" href="#demonstrador">Simulador</a>
    </div>
   </header>
   <main>
    <section id="inicio" class="soft-grid relative overflow-hidden">
     <div class="hero-orb -right-24 -top-24"></div>
     <div class="relative mx-auto grid max-w-7xl items-center gap-12 px-5 py-16 md:py-24 lg:grid-cols-2 lg:px-8">
      <div>
       <p data-template-id="hero-eyebrow" class="canva-text reveal mb-5 inline-flex rounded-full bg-pink-100 px-4 py-2 text-sm font-bold uppercase tracking-[.13em] text-pink-800">Plataforma técnico-científica</p>
       <h1 data-template-id="hero-title" class="canva-text display-font reveal delay-1 mb-6 max-w-3xl font-bold leading-[1.05] text-pink-950">Sistema térmico para piscinas parametrizado pelo clima local.</h1>
       <p data-template-id="hero-description" class="canva-text reveal delay-2 mb-8 max-w-xl text-lg leading-8 text-[#6a3650]">Uma leitura integrada das perdas evaporativas, da radiação solar incidente e das tecnologias de aquecimento para orientar decisões energéticas a partir do CEP.</p><a data-template-id="hero-cta" href="#demonstrador" class="canva-button pink-button inline-flex items-center gap-2 rounded-xl px-6 py-4 font-bold"> <span data-template-id="hero-cta-label" class="canva-text"></span> <i data-lucide="arrow-down" class="h-5 w-5" aria-hidden="true"></i> </a>
       <div class="mt-10 flex flex-wrap gap-3"><span class="inline-flex items-center gap-2 rounded-full border border-pink-200 bg-white px-4 py-2 text-sm font-semibold text-pink-900"> <i data-lucide="droplets" class="h-4 w-4" aria-hidden="true"></i> Evaporação </span> <span class="inline-flex items-center gap-2 rounded-full border border-pink-200 bg-white px-4 py-2 text-sm font-semibold text-pink-900"> <i data-lucide="sun" class="h-4 w-4" aria-hidden="true"></i> Irradiância solar </span> <span class="inline-flex items-center gap-2 rounded-full border border-pink-200 bg-white px-4 py-2 text-sm font-semibold text-pink-900"> <i data-lucide="wind" class="h-4 w-4" aria-hidden="true"></i> Clima local </span>
       </div>
      </div>
      <div class="photo-frame rounded-[2rem] border-8 border-white shadow-2xl shadow-pink-900/20"><img data-template-id="hero-thermal-image" loading="lazy" class="canva-image h-[440px] w-full object-cover">
       <div class="absolute bottom-5 left-5 right-5 z-10 rounded-2xl bg-[#4c102f]/90 p-5 text-white backdrop-blur">
        <p data-template-id="hero-image-caption" class="canva-text text-sm font-medium leading-6"></p>
       </div>
      </div>
     </div>
    </section>
    <section id="balanco" class="w-full bg-white py-20">
     <div class="mx-auto max-w-7xl px-5 lg:px-8">
      <div class="mb-12 max-w-3xl">
       <p data-template-id="thermal-kicker" class="canva-text mb-3 text-sm font-bold uppercase tracking-[.15em] text-pink-600">Módulo 1 · balanço energético</p>
       <h2 data-template-id="thermal-title" class="canva-text display-font mb-4 font-bold text-pink-950">Variáveis que definem a carga térmica da piscina.</h2>
       <p data-template-id="thermal-intro" class="canva-text text-lg leading-8 text-[#6a3650]">A temperatura da água resulta do equilíbrio entre ganhos e perdas de calor. Em superfícies abertas, o vento, a umidade e a insolação tornam o comportamento térmico altamente dependente do local de instalação.</p>
      </div>
      <div class="grid gap-6 md:grid-cols-3">
       <article data-template-id="thermal-card-evaporation" class="canva-card lift-card rounded-3xl border border-pink-100 p-7">
        <div class="mb-6 flex h-12 w-12 items-center justify-center rounded-2xl bg-pink-100 text-pink-700"><i data-lucide="cloud-fog" class="h-6 w-6" aria-hidden="true"></i>
        </div>
        <h3 data-template-id="thermal-card-evaporation-title" class="canva-text mb-3 font-bold text-pink-950"></h3>
        <p data-template-id="thermal-card-evaporation-text" class="canva-text leading-7 text-[#6a3650]"></p>
       </article>
       <article data-template-id="thermal-card-solar" class="canva-card lift-card rounded-3xl border border-pink-100 p-7">
        <div class="mb-6 flex h-12 w-12 items-center justify-center rounded-2xl bg-pink-100 text-pink-700"><i data-lucide="sun-medium" class="h-6 w-6" aria-hidden="true"></i>
        </div>
        <h3 data-template-id="thermal-card-solar-title" class="canva-text mb-3 font-bold text-pink-950"></h3>
        <p data-template-id="thermal-card-solar-text" class="canva-text leading-7 text-[#6a3650]"></p>
       </article>
       <article data-template-id="thermal-card-climate" class="canva-card lift-card rounded-3xl border border-pink-100 p-7">
        <div class="mb-6 flex h-12 w-12 items-center justify-center rounded-2xl bg-pink-100 text-pink-700"><i data-lucide="thermometer-sun" class="h-6 w-6" aria-hidden="true"></i>
        </div>
        <h3 data-template-id="thermal-card-climate-title" class="canva-text mb-3 font-bold text-pink-950"></h3>
        <p data-template-id="thermal-card-climate-text" class="canva-text leading-7 text-[#6a3650]"></p>
       </article>
      </div>
      <div class="mt-10 grid gap-6 overflow-hidden rounded-[2rem] border border-pink-100 bg-[#fff8fb] p-3 shadow-lg md:grid-cols-[1.15fr_.85fr] md:items-center">
       <img data-template-id="thermal-context-image" loading="lazy" class="canva-image h-56 w-full rounded-[1.5rem] object-cover md:h-64">
       <div class="px-4 py-5 md:px-6">
        <p data-template-id="thermal-context-kicker" class="canva-text mb-2 text-sm font-bold uppercase tracking-[.14em] text-pink-600"></p>
        <p data-template-id="thermal-context-text" class="canva-text text-lg leading-8 text-[#6a3650]"></p>
       </div>
      </div>
     </div>
    </section>
    <section id="tecnologias" class="w-full bg-[#fff2f8] py-20">
     <div class="mx-auto grid max-w-7xl gap-12 px-5 lg:grid-cols-2 lg:px-8">
      <div class="photo-frame min-h-[550px] rounded-[2rem] border-4 border-white shadow-xl shadow-pink-900/10"><img data-template-id="solar-collectors-image" loading="lazy" class="canva-image absolute inset-0 h-full w-full object-cover">
       <div class="absolute bottom-5 left-5 right-5 z-10 rounded-2xl bg-[#4c102f]/90 p-5 text-white">
        <p data-template-id="solar-image-caption" class="canva-text text-sm font-medium leading-6"></p>
       </div>
      </div>
      <div>
       <p data-template-id="technology-kicker" class="canva-text mb-3 text-sm font-bold uppercase tracking-[.15em] text-pink-600">Módulo 2 · conversão térmica</p>
       <h2 data-template-id="technology-title" class="canva-text display-font mb-5 font-bold text-pink-950">Três rotas para manter o conforto térmico.</h2>
       <p data-template-id="technology-intro" class="canva-text mb-7 text-lg leading-8 text-[#6a3650]">O sistema combina fontes renováveis e auxiliares conforme a demanda, a disponibilidade de sol e a eficiência instantânea de cada tecnologia.</p>
       <div class="space-y-4">
        <article data-template-id="technology-card-solar" class="canva-card rounded-2xl p-5 shadow-sm">
         <h3 data-template-id="technology-card-solar-title" class="canva-text mb-2 font-bold text-pink-950"></h3>
         <p data-template-id="technology-card-solar-text" class="canva-text leading-7 text-[#6a3650]"></p>
        </article>
        <article data-template-id="technology-card-pump" class="canva-card rounded-2xl p-5 shadow-sm">
         <h3 data-template-id="technology-card-pump-title" class="canva-text mb-2 font-bold text-pink-950"></h3>
         <p data-template-id="technology-card-pump-text" class="canva-text leading-7 text-[#6a3650]"></p>
        </article>
        <article data-template-id="technology-card-backup" class="canva-card rounded-2xl p-5 shadow-sm">
         <h3 data-template-id="technology-card-backup-title" class="canva-text mb-2 font-bold text-pink-950"></h3>
         <p data-template-id="technology-card-backup-text" class="canva-text leading-7 text-[#6a3650]"></p>
        </article>
        <article data-template-id="technology-card-ldr" class="canva-card rounded-2xl p-5 shadow-sm">
         <h3 data-template-id="technology-card-ldr-title" class="canva-text mb-2 font-bold text-pink-950"></h3>
         <p data-template-id="technology-card-ldr-text" class="canva-text leading-7 text-[#6a3650]"></p>
        </article>
       </div>
      </div>
     </div>
    </section>
    <section id="integracao" class="w-full bg-white py-20">
     <div class="mx-auto max-w-7xl px-5 lg:px-8">
      <div class="grid gap-12 lg:grid-cols-2 lg:items-center">
       <div>
        <p data-template-id="architecture-kicker" class="canva-text mb-3 text-sm font-bold uppercase tracking-[.15em] text-pink-600"></p>
        <h2 data-template-id="architecture-title" class="canva-text display-font mb-5 font-bold text-pink-950"></h2>
        <p data-template-id="architecture-text" class="canva-text mb-7 text-lg leading-8 text-[#6a3650]"></p><img data-template-id="heat-pump-image" loading="lazy" class="canva-image h-64 w-full rounded-3xl object-cover shadow-lg"><img data-template-id="pool-overview-image" loading="lazy" class="canva-image mt-4 h-64 w-full rounded-3xl object-cover shadow-lg">
       </div>
       <aside data-template-id="architecture-flow-panel" class="canva-panel rounded-[2rem] border border-pink-100 bg-[#fff8fb] p-6 md:p-8">
        <h3 data-template-id="flow-title" class="canva-text mb-8 font-bold text-pink-950"></h3>
        <div class="space-y-3">
         <div data-template-id="flow-input" class="canva-card rounded-2xl p-5">
          <p data-template-id="flow-input-title" class="canva-text font-bold text-pink-950"></p>
          <p data-template-id="flow-input-text" class="canva-text mt-1 text-sm leading-6 text-[#6a3650]"></p>
         </div>
         <div class="text-center text-2xl text-pink-600" aria-hidden="true">
          ↓
         </div>
         <div data-template-id="flow-location" class="canva-card rounded-2xl p-5">
          <p data-template-id="flow-location-title" class="canva-text font-bold text-pink-950"></p>
          <p data-template-id="flow-location-text" class="canva-text mt-1 text-sm leading-6 text-[#6a3650]"></p>
         </div>
         <div class="text-center text-2xl text-pink-600" aria-hidden="true">
          ↓
         </div>
         <div data-template-id="flow-calculation" class="canva-card rounded-2xl p-5">
          <p data-template-id="flow-calculation-title" class="canva-text font-bold text-pink-950"></p>
          <p data-template-id="flow-calculation-text" class="canva-text mt-1 text-sm leading-6 text-[#6a3650]"></p>
         </div>
         <div class="text-center text-2xl text-pink-600" aria-hidden="true">
          ↓
         </div>
         <div data-template-id="flow-control" class="canva-card rounded-2xl p-5">
          <p data-template-id="flow-control-title" class="canva-text font-bold text-pink-950"></p>
          <p data-template-id="flow-control-text" class="canva-text mt-1 text-sm leading-6 text-[#6a3650]"></p>
         </div>
        </div>
       </aside>
      </div>
     </div>
    </section>
    <section id="demonstrador" class="w-full bg-pink-950 py-20 text-white">
     <div class="mx-auto max-w-7xl px-5 lg:px-8">
      <div class="mb-10 max-w-3xl">
       <p data-template-id="demo-kicker" class="canva-text mb-3 text-sm font-bold uppercase tracking-[.15em] text-pink-200">Demonstrador interativo · CEP e clima</p>
       <h2 data-template-id="demo-title" class="canva-text display-font mb-4 font-bold">Consulte o clima local e estime a operação térmica.</h2>
       <p data-template-id="demo-intro" class="canva-text text-lg leading-8 text-pink-100">Digite um CEP brasileiro para reunir município, condições meteorológicas atuais e uma estimativa indicativa de perdas, ganho solar e desempenho da bomba de calor.</p>
      </div>
      <div class="grid gap-8 rounded-[2rem] bg-white p-6 text-[#321021] shadow-2xl md:p-9 lg:grid-cols-[1.05fr_.95fr]">
       <div>
        <form id="cep-form" class="space-y-5" novalidate>
         <div><label data-template-id="cep-input-label" class="canva-text mb-3 block font-bold text-pink-950" for="cep-input"></label>
          <div class="flex flex-col gap-3 sm:flex-row"><input id="cep-input" class="canva-input w-full rounded-xl border border-pink-200 bg-[#fff8fb] px-4 py-3 text-lg font-semibold text-pink-950 placeholder:text-pink-300" type="text" inputmode="numeric" autocomplete="postal-code" maxlength="9"> <button id="cep-submit" data-template-id="cep-submit-button" class="canva-button pink-button inline-flex shrink-0 items-center justify-center gap-2 rounded-xl px-5 py-3 font-bold" type="submit"> <i data-lucide="search" class="h-5 w-5" aria-hidden="true"></i> <span data-template-id="cep-submit-label" class="canva-text"></span> </button>
          </div>
         </div>
         <p data-template-id="cep-helper-text" class="canva-text text-sm leading-6 text-[#6a3650]"></p>
        </form>
        <section class="mt-8 rounded-3xl border border-pink-100 bg-[#fff8fb] p-6" aria-labelledby="location-result-title">
         <div class="mb-5 flex items-center justify-between gap-4">
          <h3 id="location-result-title" data-template-id="location-result-title" class="canva-text font-bold text-pink-950"></h3><span class="inline-flex items-center gap-2 rounded-full bg-pink-100 px-3 py-1 text-sm font-bold text-pink-800"> <span id="status-dot" class="status-dot" aria-hidden="true"></span> <span id="request-status" aria-live="polite">Aguardando consulta</span> </span>
         </div>
         <div id="location-empty" data-template-id="location-empty" class="canva-banner rounded-2xl border border-dashed border-pink-200 bg-white p-5 text-sm leading-6 text-[#6a3650]"></div>
         <dl id="location-data" class="hidden grid gap-x-6 gap-y-4 text-sm sm:grid-cols-2">
          <div>
           <dt class="font-bold text-pink-800">
            Município / UF
           </dt>
           <dd id="result-city" class="mt-1 text-[#6a3650]">
            —
           </dd>
          </div>
          <div>
           <dt class="font-bold text-pink-800">
            Coordenadas aproximadas
           </dt>
           <dd id="result-coordinates" class="mt-1 text-[#6a3650]">
            —
           </dd>
          </div>
          <div>
           <dt class="font-bold text-pink-800">
            Temperatura ambiente
           </dt>
           <dd id="result-temperature" class="mt-1 text-[#6a3650]">
            —
           </dd>
          </div>
          <div>
           <dt class="font-bold text-pink-800">
            Umidade relativa
           </dt>
           <dd id="result-humidity" class="mt-1 text-[#6a3650]">
            —
           </dd>
          </div>
          <div>
           <dt class="font-bold text-pink-800">
            Velocidade do vento
           </dt>
           <dd id="result-wind" class="mt-1 text-[#6a3650]">
            —
           </dd>
          </div>
          <div>
           <dt class="font-bold text-pink-800">
            Irradiância diária estimada
           </dt>
           <dd id="result-radiation" class="mt-1 text-[#6a3650]">
            —
           </dd>
          </div>
         </dl>
        </section>
       </div>
       <aside class="rounded-3xl bg-[#fff2f8] p-6">
        <p data-template-id="estimate-panel-kicker" class="canva-text mb-5 text-center text-sm font-bold uppercase tracking-[.14em] text-pink-700"></p>
        <div id="estimate-empty" data-template-id="estimate-empty" class="canva-banner rounded-2xl border border-dashed border-pink-200 bg-white p-5 text-center text-sm leading-6 text-[#6a3650]"></div>
        <div id="estimate-data" class="hidden">
         <div class="grid gap-3 sm:grid-cols-2">
          <div class="metric-card">
           <p class="text-xs font-bold uppercase tracking-[.12em] text-pink-700">Perda evaporativa</p>
           <p id="evaporation-value" class="metric-value mt-2">—</p>
           <p class="mt-1 text-xs text-[#6a3650]">estimativa diária</p>
          </div>
          <div class="metric-card">
           <p class="text-xs font-bold uppercase tracking-[.12em] text-pink-700">Ganho solar</p>
           <p id="solar-gain-value" class="metric-value mt-2">—</p>
           <p class="mt-1 text-xs text-[#6a3650]">absorção potencial</p>
          </div>
          <div class="metric-card">
           <p class="text-xs font-bold uppercase tracking-[.12em] text-pink-700">COP previsto</p>
           <p id="cop-value" class="metric-value mt-2">—</p>
           <p class="mt-1 text-xs text-[#6a3650]">bomba de calor</p>
          </div>
          <div class="metric-card">
           <p class="text-xs font-bold uppercase tracking-[.12em] text-pink-700">Operação sugerida</p>
           <p id="operation-value" class="metric-value mt-2">—</p>
           <p class="mt-1 text-xs text-[#6a3650]">janela de aquecimento</p>
          </div>
         </div>
         <div class="mt-5 rounded-2xl bg-[#4c102f] p-5 text-pink-100">
          <p data-template-id="estimate-note-title" class="canva-text mb-2 text-sm font-bold uppercase tracking-[.12em]"></p>
          <p id="estimate-note" class="text-sm leading-7" aria-live="polite"></p>
         </div>
        </div>
       </aside>
      </div>
     </div>
    </section>
   </main>
   <footer data-template-id="site-footer" class="canva-footer w-full bg-pink-950 px-5 py-10 text-center text-pink-100">
    <p data-template-id="footer-text" class="canva-text mx-auto max-w-3xl text-sm leading-7"></p>
   </footer>
  </div>
  <script src="/_sdk/489148d8756906ef.editing_sdk.js" integrity="sha512-hxxSbMNp1t+UEu3j/dIQUU4MJnmsCo0Gs3iQVVS706vrCJ3Yt2+ySOlfJEaPyiyQVLjZRmn1dNVqg6M40VZZHQ=="></script>
  <script>
    const menuToggle = document.getElementById("menu-toggle");
    const mobileMenu = document.getElementById("mobile-menu");

    menuToggle.addEventListener("click", () => {
      const isOpen = mobileMenu.classList.toggle("is-open");
      menuToggle.setAttribute("aria-expanded", String(isOpen));
      menuToggle.setAttribute("aria-label", isOpen ? "Fechar menu" : "Abrir menu");
    });

    document.querySelectorAll("#mobile-menu a").forEach((link) => {
      link.addEventListener("click", () => {
        mobileMenu.classList.remove("is-open");
        menuToggle.setAttribute("aria-expanded", "false");
        menuToggle.setAttribute("aria-label", "Abrir menu");
      });
    });

    const cepForm = document.getElementById("cep-form");
    const cepInput = document.getElementById("cep-input");
    const submitButton = document.getElementById("cep-submit");
    const requestStatus = document.getElementById("request-status");
    const statusDot = document.getElementById("status-dot");
    const locationEmpty = document.getElementById("location-empty");
    const locationData = document.getElementById("location-data");
    const estimateEmpty = document.getElementById("estimate-empty");
    const estimateData = document.getElementById("estimate-data");

    const resultCity = document.getElementById("result-city");
    const resultCoordinates = document.getElementById("result-coordinates");
    const resultTemperature = document.getElementById("result-temperature");
    const resultHumidity = document.getElementById("result-humidity");
    const resultWind = document.getElementById("result-wind");
    const resultRadiation = document.getElementById("result-radiation");

    const evaporationValue = document.getElementById("evaporation-value");
    const solarGainValue = document.getElementById("solar-gain-value");
    const copValue = document.getElementById("cop-value");
    const operationValue = document.getElementById("operation-value");
    const estimateNote = document.getElementById("estimate-note");

    cepInput.addEventListener("input", () => {
      const digits = cepInput.value.replace(/\D/g, "").slice(0, 8);
      cepInput.value = digits.length > 5 ? digits.slice(0, 5) + "-" + digits.slice(5) : digits;
    });

    function setStatus(type, text) {
      statusDot.classList.remove("is-success", "is-error", "is-loading");
      if (type === "loading") statusDot.classList.add("is-loading");
      if (type === "success") statusDot.classList.add("is-success");
      if (type === "error") statusDot.classList.add("is-error");
      requestStatus.textContent = text;
    }

    function showMessage(message) {
      locationData.classList.add("hidden");
      locationEmpty.classList.remove("hidden");
      locationEmpty.textContent = message;
      estimateData.classList.add("hidden");
      estimateEmpty.classList.remove("hidden");
      estimateEmpty.textContent = message;
    }

    function calculateEstimates(temperature, humidity, wind, radiation) {
      const vaporFactor = Math.max(0.35, (100 - humidity) / 100);
      const windFactor = 1 + Math.min(wind, 35) / 18;
      const temperatureFactor = Math.max(0.55, (temperature + 8) / 30);
      const evaporation = Math.max(1.2, 4.7 * vaporFactor * windFactor * temperatureFactor);
      const solarGain = Math.max(0.4, radiation * 0.56);
      const cop = Math.min(6.2, Math.max(2.1, 2.35 + temperature * 0.095 - humidity * 0.004));
      const operation = radiation >= 3.5 ? "10h–16h" : "12h–18h";
      return { evaporation, solarGain, cop, operation };
    }

    function showResults(address, geo, weather) {
      const current = weather.current;
      const daily = weather.daily;
      const radiation = daily.shortwave_radiation_sum && daily.shortwave_radiation_sum[0]
        ? daily.shortwave_radiation_sum[0] / 1000
        : 0;

      const temperature = current.temperature_2m;
      const humidity = current.relative_humidity_2m;
      const wind = current.wind_speed_10m;
      const estimates = calculateEstimates(temperature, humidity, wind, radiation);

      resultCity.textContent = address.localidade + " · " + address.uf;
      resultCoordinates.textContent = geo.latitude.toFixed(2) + "°, " + geo.longitude.toFixed(2) + "°";
      resultTemperature.textContent = temperature.toFixed(1) + " °C";
      resultHumidity.textContent = Math.round(humidity) + " %";
      resultWind.textContent = wind.toFixed(1) + " km/h";
      resultRadiation.textContent = radiation.toFixed(2) + " kWh/m²·dia";

      evaporationValue.textContent = estimates.evaporation.toFixed(1) + " kWh/m²";
      solarGainValue.textContent = estimates.solarGain.toFixed(1) + " kWh/m²";
      copValue.textContent = estimates.cop.toFixed(1);
      operationValue.textContent = estimates.operation;
      estimateNote.textContent =
        "Com umidade de " + Math.round(humidity) + "% e vento de " + wind.toFixed(1) +
        " km/h, a evaporação tende a ser o principal fator de perda. Priorize cobertura térmica fora do uso e acione a bomba de calor na janela sugerida.";

      locationEmpty.classList.add("hidden");
      locationData.classList.remove("hidden");
      estimateEmpty.classList.add("hidden");
      estimateData.classList.remove("hidden");
    }

    cepForm.addEventListener("submit", async (event) => {
      event.preventDefault();
      const cep = cepInput.value.replace(/\D/g, "");

      if (cep.length !== 8) {
        setStatus("error", "CEP inválido");
        showMessage("Informe um CEP composto por 8 dígitos para iniciar a consulta climática.");
        cepInput.focus();
        return;
      }

      submitButton.disabled = true;
      setStatus("loading", "Consultando clima");
      showMessage("Identificando município, coordenadas aproximadas e parâmetros climáticos locais...");

      try {
        const addressResponse = await fetch("https://viacep.com.br/ws/" + cep + "/json/", {
          headers: { "Accept": "application/json" }
        });

        if (!addressResponse.ok) throw new Error("Falha na consulta de CEP");
        const address = await addressResponse.json();
        if (address.erro || !address.localidade) throw new Error("CEP não localizado");

        const geoResponse = await fetch(
          "https://geocoding-api.open-meteo.com/v1/search?name=" +
          encodeURIComponent(address.localidade) +
          "&count=10&language=pt&format=json"
        );

        if (!geoResponse.ok) throw new Error("Falha na geolocalização");
        const geoData = await geoResponse.json();
        const match = (geoData.results || []).find((item) => item.country_code === "BR" && item.admin1 === address.uf) ||
          (geoData.results || []).find((item) => item.country_code === "BR");

        if (!match) throw new Error("Município não localizado");

        const weatherUrl =
          "https://api.open-meteo.com/v1/forecast?latitude=" + match.latitude +
          "&longitude=" + match.longitude +
          "&current=temperature_2m,relative_humidity_2m,wind_speed_10m" +
          "&daily=shortwave_radiation_sum&timezone=auto";

        const weatherResponse = await fetch(weatherUrl);
        if (!weatherResponse.ok) throw new Error("Falha na consulta meteorológica");
        const weather = await weatherResponse.json();

        showResults(address, match, weather);
        setStatus("success", "Parâmetros atualizados");
      } catch (error) {
        setStatus("error", "Consulta indisponível");
        showMessage("Não foi possível obter os parâmetros deste município agora. Verifique o CEP e tente novamente em instantes.");
      } finally {
        submitButton.disabled = false;
      }
    });

    lucide.createIcons();
  </script>
 </body>
</html>
