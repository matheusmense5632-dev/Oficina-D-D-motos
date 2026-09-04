<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>D&D-Motos — Oficina de Motos</title>
<meta name="description" content="Manutenção preventiva e corretiva para sua moto, diagnóstico elétrico e revisão completa. Agende seu horário online com a D&D-Motos.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Big+Shoulders+Display:wght@700;800&family=IBM+Plex+Sans:wght@400;500;600;700&family=IBM+Plex+Mono:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --steel-100: #EEF0F0;
    --steel-200: #E1E4E4;
    --steel-300: #C7CBCC;
    --steel-600: #5B6165;
    --ink-900: #1B1D1F;
    --ink-800: #232629;
    --ink-700: #34373C;
    --paper: #F5F0E4;
    --paper-line: #DCD2B8;
    --stamp: #A9291E;
    --stamp-dark: #872017;
    --pencil: #D69A3B;
    --white: #FFFFFF;

    --font-display: 'Big Shoulders Display', sans-serif;
    --font-body: 'IBM Plex Sans', sans-serif;
    --font-mono: 'IBM Plex Mono', monospace;

    --container: 1160px;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }
  html { scroll-behavior: smooth; }
  section[id] { scroll-margin-top: 76px; }

  body {
    font-family: var(--font-body);
    color: var(--ink-900);
    background: var(--steel-100);
    line-height: 1.5;
    -webkit-font-smoothing: antialiased;
  }

  img, svg { display: block; }
  a { color: inherit; text-decoration: none; }
  button { font-family: inherit; cursor: pointer; border: none; background: none; }
  ul { list-style: none; }

  :focus-visible { outline: 3px solid var(--pencil); outline-offset: 2px; }

  @media (prefers-reduced-motion: reduce) {
    *, *::before, *::after {
      animation-duration: 0.01ms !important;
      animation-iteration-count: 1 !important;
      transition-duration: 0.01ms !important;
      scroll-behavior: auto !important;
    }
  }

  .container { max-width: var(--container); margin: 0 auto; padding: 0 24px; }

  .icon { width: 24px; height: 24px; fill: none; stroke: currentColor; }

  .eyebrow {
    font-family: var(--font-mono);
    font-size: 0.8rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    font-weight: 500;
    display: block;
  }

  h1, h2, h3 {
    font-family: var(--font-display);
    font-weight: 800;
    line-height: 1.02;
    letter-spacing: 0.01em;
    text-transform: uppercase;
  }

  /* Buttons */
  .btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 8px;
    padding: 13px 26px;
    border-radius: 4px;
    font-weight: 600;
    font-size: 0.95rem;
    transition: transform 0.15s ease, background 0.15s ease, opacity .15s ease;
    white-space: nowrap;
  }
  .btn-primary { background: var(--stamp); color: var(--white); }
  .btn-primary:hover { background: var(--stamp-dark); transform: translateY(-1px); }
  .btn-primary:disabled { opacity: 0.6; transform: none; cursor: default; }
  .btn-outline { background: transparent; border: 1.5px solid currentColor; }
  .btn-outline:hover { background: rgba(0,0,0,0.05); }

  /* Header */
  .site-header {
    position: sticky; top: 0; z-index: 100;
    background: rgba(245, 240, 228, 0.92);
    backdrop-filter: blur(6px);
    border-bottom: 1px solid var(--paper-line);
  }
  .site-header .container { display: flex; align-items: center; justify-content: space-between; height: 76px; }
  .logo { display: flex; flex-direction: column; line-height: 1; }
  .logo .wordmark { font-family: var(--font-display); font-weight: 800; font-size: 1.5rem; letter-spacing: 0.02em; }
  .logo .caption { font-family: var(--font-mono); font-size: 0.62rem; letter-spacing: 0.15em; color: var(--steel-600); margin-top: 3px; }

  .nav-links { display: flex; gap: 30px; align-items: center; }
  .nav-links a:not(.btn) { font-size: 0.94rem; font-weight: 500; position: relative; padding: 4px 0; }
  .nav-links a:not(.btn)::after {
    content: ''; position: absolute; left: 0; bottom: 0; width: 0; height: 2px;
    background: var(--stamp); transition: width 0.2s ease;
  }
  .nav-links a:not(.btn):hover::after { width: 100%; }

  .menu-toggle { display: none; flex-direction: column; gap: 5px; padding: 8px; }
  .menu-toggle span { width: 24px; height: 2px; background: var(--ink-900); transition: transform 0.2s ease, opacity 0.2s ease; }
  .menu-toggle.active span:nth-child(1) { transform: translateY(7px) rotate(45deg); }
  .menu-toggle.active span:nth-child(2) { opacity: 0; }
  .menu-toggle.active span:nth-child(3) { transform: translateY(-7px) rotate(-45deg); }

  /* Hero */
  .hero { background: var(--ink-900); color: var(--white); padding: 88px 0 100px; }
  .hero .container { display: grid; grid-template-columns: 1.1fr 0.9fr; gap: 56px; align-items: center; }
  .hero-eyebrow { color: var(--pencil); margin-bottom: 22px; }
  .hero h1 { font-size: clamp(2.5rem, 5vw, 4.1rem); margin-bottom: 24px; }
  .hero .lead { font-size: 1.1rem; color: var(--steel-300); max-width: 46ch; margin-bottom: 36px; }
  .hero-ctas { display: flex; gap: 16px; flex-wrap: wrap; }
  .hero-ctas .btn-outline { border-color: var(--steel-300); }

  .ticket {
    background: var(--paper); color: var(--ink-900); border-radius: 6px;
    padding: 28px 28px 34px; box-shadow: 0 24px 48px -12px rgba(0,0,0,0.5);
    position: relative; transform: rotate(2deg);
  }
  .ticket-row-top {
    display: flex; justify-content: space-between; align-items: baseline;
    font-family: var(--font-mono); font-size: 0.72rem; letter-spacing: 0.08em;
    color: var(--steel-600); text-transform: uppercase; margin-bottom: 18px;
  }
  .ticket-row-top strong { color: var(--ink-900); font-size: 0.8rem; }
  .ticket-tear { border-top: 2px dashed var(--paper-line); margin: 18px 0; }
  .ticket-checklist { display: flex; flex-direction: column; gap: 13px; margin-bottom: 6px; }
  .ticket-checklist li { display: flex; align-items: center; gap: 10px; font-size: 0.96rem; font-weight: 500; }
  .ticket-checklist .icon { width: 17px; height: 17px; color: var(--pencil); flex-shrink: 0; stroke-width: 2.4; }
  .ticket-foot { font-family: var(--font-mono); font-size: 0.7rem; letter-spacing: 0.06em; color: var(--steel-600); text-transform: uppercase; }
  .ticket-stamp {
    position: absolute; bottom: -16px; right: -8px; width: 100px; height: 100px;
    border: 3px double var(--stamp); border-radius: 50%; color: var(--stamp);
    background: rgba(245,240,228,0.95); display: flex; align-items: center; justify-content: center;
    text-align: center; transform: rotate(-11deg); font-family: var(--font-mono);
    font-weight: 700; font-size: 0.7rem; letter-spacing: 0.06em; text-transform: uppercase; line-height: 1.3;
  }

  /* Section headings shared */
  .section-head { max-width: 640px; margin-bottom: 52px; }
  .section-head.center { margin-left: auto; margin-right: auto; text-align: center; }
  .section-head .eyebrow { color: var(--stamp); margin-bottom: 14px; }
  .section-head h2 { font-size: clamp(2rem, 3.4vw, 2.7rem); margin-bottom: 16px; }
  .section-head p { color: var(--steel-600); font-size: 1.04rem; }
  .agendamento .section-head .eyebrow { color: var(--pencil); }
  .agendamento .section-head p { color: var(--steel-300); }

  /* Diferenciais */
  .diferenciais { padding: 100px 0; background: var(--steel-100); }
  .cards-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 26px; }
  .card {
    background: var(--white); border: 1px solid var(--steel-200); border-radius: 8px;
    padding: 32px 24px; transition: transform 0.2s ease, box-shadow 0.2s ease;
  }
  .card:hover { transform: translateY(-4px); box-shadow: 0 18px 32px -18px rgba(27,29,31,0.25); }
  .card .icon { width: 28px; height: 28px; color: var(--stamp); margin-bottom: 20px; stroke-width: 1.6; }
  .card h3 { font-family: var(--font-body); text-transform: none; font-weight: 700; font-size: 1.08rem; letter-spacing: 0; margin-bottom: 10px; }
  .card p { color: var(--steel-600); font-size: 0.94rem; }

  /* Serviços */
  .servicos { padding: 100px 0; background: var(--paper); }
  .table-wrapper { overflow-x: auto; border: 1px solid var(--paper-line); border-radius: 8px; background: var(--white); }
  table.servicos-table { width: 100%; border-collapse: collapse; min-width: 760px; }
  .servicos-table th {
    font-family: var(--font-mono); font-size: 0.7rem; letter-spacing: 0.08em; text-transform: uppercase;
    text-align: left; padding: 16px 20px; background: var(--ink-900); color: var(--steel-300);
  }
  .servicos-table th:first-child { border-radius: 8px 0 0 0; }
  .servicos-table th:last-child { border-radius: 0 8px 0 0; }
  .servicos-table td { padding: 18px 20px; border-top: 1px solid var(--steel-200); font-size: 0.94rem; vertical-align: top; }
  .servicos-table tr:hover td { background: var(--steel-100); }
  .servicos-table .code { font-family: var(--font-mono); color: var(--stamp); font-weight: 600; white-space: nowrap; }
  .servicos-table .servico-nome { font-weight: 600; }
  .servicos-table .desc { color: var(--steel-600); }
  .servicos-table .duracao { white-space: nowrap; color: var(--steel-600); }
  .servicos-table .valor { font-family: var(--font-mono); font-weight: 600; white-space: nowrap; }
  .servicos-note { margin-top: 16px; font-size: 0.85rem; color: var(--steel-600); }

  /* Agendamento */
  .agendamento { padding: 100px 0; background: var(--ink-900); color: var(--white); }

  .form-ticket {
    background: var(--paper); color: var(--ink-900); border-radius: 10px; padding: 40px;
    max-width: 760px; margin: 0 auto; position: relative; border-top: 4px dashed var(--paper-line);
  }
  .form-ticket-number {
    position: absolute; top: -15px; right: 32px; background: var(--ink-900); color: var(--pencil);
    font-family: var(--font-mono); font-size: 0.72rem; padding: 6px 14px; border-radius: 4px; letter-spacing: 0.05em;
  }
  .form-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; }
  .form-field { display: flex; flex-direction: column; gap: 6px; }
  .form-field.full { grid-column: 1 / -1; }
  .form-field label { font-size: 0.82rem; font-weight: 600; color: var(--ink-700); }
  .form-field label .opt { font-weight: 400; color: var(--steel-600); font-size: 0.78rem; }
  .form-field input, .form-field select, .form-field textarea {
    font-family: var(--font-body); font-size: 0.95rem; padding: 12px 14px;
    border: 1.5px solid var(--paper-line); border-radius: 5px; background: var(--white); color: var(--ink-900);
  }
  .form-field input:focus, .form-field select:focus, .form-field textarea:focus { border-color: var(--stamp); outline: none; }
  .form-field textarea { resize: vertical; min-height: 88px; }

  .form-submit-row { margin-top: 26px; display: flex; align-items: center; gap: 16px; flex-wrap: wrap; }
  .form-note { font-size: 0.8rem; color: var(--steel-600); }

  .form-error {
    display: none; color: var(--stamp); background: rgba(169,41,30,0.08); border: 1px solid var(--stamp);
    padding: 12px 16px; border-radius: 5px; font-size: 0.85rem; margin-top: 18px;
  }
  .form-error.active { display: block; }

  .form-success { display: none; text-align: center; padding: 8px 0 16px; }
  .form-success.active { display: block; }
  .stamp-confirm {
    display: inline-flex; align-items: center; justify-content: center; border: 4px double var(--stamp);
    color: var(--stamp); border-radius: 50%; width: 124px; height: 124px; font-family: var(--font-mono);
    font-weight: 700; letter-spacing: 0.05em; text-transform: uppercase; transform: rotate(-8deg) scale(0);
    margin-bottom: 20px; font-size: 0.92rem; opacity: 0;
  }
  .stamp-confirm.animate { animation: stampIn 0.5s cubic-bezier(.2,1.4,.4,1) forwards; }
  @keyframes stampIn {
    0% { transform: rotate(-8deg) scale(2.4); opacity: 0; }
    60% { transform: rotate(-8deg) scale(0.92); opacity: 1; }
    100% { transform: rotate(-8deg) scale(1); opacity: 1; }
  }
  .form-success h3 { text-transform: none; font-family: var(--font-body); font-size: 1.3rem; margin-bottom: 8px; }
  .form-success p { color: var(--steel-600); max-width: 42ch; margin: 0 auto; }
  .os-summary {
    font-family: var(--font-mono); font-size: 0.85rem; background: var(--steel-100); border-radius: 6px;
    padding: 16px; margin: 20px auto 0; max-width: 420px; text-align: left; color: var(--ink-900); line-height: 1.7;
  }

  /* Footer */
  .site-footer { background: var(--ink-800); color: var(--steel-300); padding: 72px 0 32px; }
  .footer-grid { display: grid; grid-template-columns: 1.4fr 1fr 1.2fr 1fr; gap: 40px; padding-bottom: 44px; border-bottom: 1px solid var(--ink-700); }
  .footer-grid h4 { font-family: var(--font-mono); font-size: 0.72rem; letter-spacing: 0.1em; text-transform: uppercase; color: #7A8083; margin-bottom: 18px; }
  .footer-grid .wordmark { font-family: var(--font-display); font-size: 1.4rem; color: var(--white); font-weight: 800; margin-bottom: 12px; }
  .footer-grid > div > p { font-size: 0.9rem; line-height: 1.6; }
  .footer-list { display: flex; flex-direction: column; gap: 11px; font-size: 0.9rem; }
  .footer-list li { display: flex; gap: 10px; align-items: flex-start; }
  .footer-list .icon { width: 16px; height: 16px; flex-shrink: 0; margin-top: 3px; color: var(--pencil); stroke-width: 1.8; }
  .footer-list a:hover { color: var(--white); }
  .footer-bottom { padding-top: 26px; font-size: 0.8rem; color: #6C7376; }

  /* Responsive */
  @media (max-width: 968px) {
    .hero .container { grid-template-columns: 1fr; }
    .hero-visual { max-width: 460px; }
    .ticket { transform: none; }
    .cards-grid { grid-template-columns: repeat(2, 1fr); }
    .footer-grid { grid-template-columns: 1fr 1fr; row-gap: 36px; }
  }
  @media (max-width: 720px) {
    .nav-links {
      position: fixed; top: 76px; left: 0; right: 0; background: var(--paper);
      flex-direction: column; align-items: flex-start; padding: 22px 24px 28px; gap: 18px;
      border-bottom: 1px solid var(--paper-line); transform: translateY(-130%); transition: transform 0.25s ease;
    }
    .nav-links.active { transform: translateY(0); }
    .nav-links a.btn { margin-top: 6px; }
    .menu-toggle { display: flex; }
    .hero { padding: 56px 0 64px; }
    .diferenciais, .servicos, .agendamento { padding: 64px 0; }
    .cards-grid { grid-template-columns: 1fr; }
    .form-grid { grid-template-columns: 1fr; }
    .form-ticket { padding: 28px 20px; }
    .footer-grid { grid-template-columns: 1fr; gap: 32px; }
  }
  @media (max-width: 640px) {
    .table-wrapper { overflow-x: visible; border: none; background: none; }
    table.servicos-table { min-width: 0; display: block; }
    .servicos-table thead { display: none; }
    .servicos-table tbody { display: block; }
    .servicos-table tr { display: block; background: var(--white); border: 1px solid var(--paper-line); border-radius: 8px; margin-bottom: 14px; padding: 14px 16px; }
    .servicos-table td { display: block; padding: 4px 0; border: none; white-space: normal; }
    .servicos-table .servico-nome { font-size: 1rem; margin-bottom: 6px; }
    .servicos-table .duracao::before { content: "Duração: "; color: var(--steel-600); font-weight: 600; }
    .servicos-table .valor::before { content: "Valor: "; color: var(--steel-600); font-weight: 600; }
  }
</style>
</head>
<body>

<svg style="display:none" aria-hidden="true">
  <symbol id="icon-wrench" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.75"><path d="M21 7.5a5.5 5.5 0 0 1-7.44 5.16L6 20.24 3.76 18l7.58-7.56A5.5 5.5 0 0 1 18.5 3c.74 0 1.45.15 2.1.43l-4.2 4.2 1.94 1.94 4.2-4.2c.28.66.43 1.38.43 2.13z"/></symbol>
  <symbol id="icon-shield" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.75"><path d="M12 3l7 3.2v5.3c0 5-3.2 8.3-7 9.5-3.8-1.2-7-4.5-7-9.5V6.2L12 3z"/></symbol>
  <symbol id="icon-receipt" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.75"><path d="M6 3h12a1 1 0 0 1 1 1v17l-2.5-1.6L14 21l-2-1.6L10 21l-2.5-1.6L5 21V4a1 1 0 0 1 1-1z"/><line x1="8.5" y1="8" x2="15.5" y2="8"/><line x1="8.5" y1="12" x2="15.5" y2="12"/></symbol>
  <symbol id="icon-clock" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.75"><circle cx="12" cy="12" r="9"/><polyline points="12 7 12 12 15.5 14"/></symbol>
  <symbol id="icon-check" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round" stroke-width="2.2"><polyline points="4 12.5 9.5 18 20 6"/></symbol>
  <symbol id="icon-pin" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.75"><path d="M12 21s-7-7.1-7-12a7 7 0 0 1 14 0c0 4.9-7 12-7 12z"/><circle cx="12" cy="9" r="2.4"/></symbol>
  <symbol id="icon-phone" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.75"><path d="M6.6 10.8a15.9 15.9 0 0 0 6.6 6.6l2.2-2.2a1.4 1.4 0 0 1 1.45-.34c1.2.4 2.5.62 3.85.62.72 0 1.3.58 1.3 1.3v3.4c0 .72-.58 1.3-1.3 1.3C11.4 20.8 3.9 13.3 3.9 4.1c0-.72.58-1.3 1.3-1.3h3.4c.72 0 1.3.58 1.3 1.3 0 1.35.22 2.65.62 3.85.13.46.02.98-.34 1.45L6.6 10.8z"/></symbol>
  <symbol id="icon-mail" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.75"><rect x="3" y="5.5" width="18" height="13" rx="2"/><polyline points="3.5 6.5 12 13 20.5 6.5"/></symbol>
</svg>

<header class="site-header">
  <div class="container">
    <a href="#inicio" class="logo">
      <img src="data:image/jpeg;base64,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" alt="D&amp;D Motos" style="height: 52px; border-radius: 6px; display: block;">
    </a>
    <nav class="nav-links" id="navLinks">
      <a href="#inicio">Início</a>
      <a href="#servicos">Serviços</a>
      <a href="#diferenciais">Diferenciais</a>
      <a href="#contato">Contato</a>
      <a href="#agendamento" class="btn btn-primary">Agendar Horário</a>
    </nav>
    <button class="menu-toggle" id="menuToggle" aria-label="Abrir menu" aria-expanded="false">
      <span></span><span></span><span></span>
    </button>
  </div>
</header>

<section class="hero" id="inicio">
  <div class="container">
    <div class="hero-text">
      <span class="eyebrow hero-eyebrow">Oficina de Motos</span>
      <h1>Sua moto em boas mãos. Do jeito certo.</h1>
      <p class="lead">Diagnóstico preciso, peças de qualidade e uma ordem de serviço transparente do início ao fim — sem letra miúda e sem susto no caixa.</p>
      <div class="hero-ctas">
        <a href="#agendamento" class="btn btn-primary">Agendar um Horário</a>
        <a href="#servicos" class="btn btn-outline">Ver Tabela de Serviços</a>
      </div>
    </div>
    <div class="hero-visual">
      <div class="ticket">
        <div class="ticket-row-top">
          <span>Ordem de Serviço</span>
          <strong>Nº 04582</strong>
        </div>
        <ul class="ticket-checklist">
          <li><svg class="icon"><use href="#icon-check"></use></svg> Troca de óleo e filtro</li>
          <li><svg class="icon"><use href="#icon-check"></use></svg> Relação — corrente e coroa</li>
          <li><svg class="icon"><use href="#icon-check"></use></svg> Revisão dos freios</li>
          <li><svg class="icon"><use href="#icon-check"></use></svg> Diagnóstico elétrico</li>
        </ul>
        <div class="ticket-tear"></div>
        <span class="ticket-foot">Orçamento aprovado antes de iniciar</span>
        <div class="ticket-stamp">Garantia<br>90 Dias</div>
      </div>
    </div>
  </div>
</section>

<section class="diferenciais" id="diferenciais">
  <div class="container">
    <div class="section-head">
      <span class="eyebrow">Por que a D&amp;D-Motos</span>
      <h2>Feito para durar, não só para sair da oficina</h2>
      <p>Trabalhamos como se a moto fosse nossa — com diagnóstico correto antes de qualquer troca de peça.</p>
    </div>
    <div class="cards-grid">
      <div class="card">
        <svg class="icon"><use href="#icon-wrench"></use></svg>
        <h3>Mão de Obra Certificada</h3>
        <p>Mecânicos treinados e atualizados com as principais marcas nacionais e importadas.</p>
      </div>
      <div class="card">
        <svg class="icon"><use href="#icon-shield"></use></svg>
        <h3>90 Dias de Garantia</h3>
        <p>Garantia em peças e serviço, por escrito, em toda ordem de serviço fechada.</p>
      </div>
      <div class="card">
        <svg class="icon"><use href="#icon-receipt"></use></svg>
        <h3>Orçamento Antes, Sempre</h3>
        <p>Nenhum serviço começa sem sua aprovação do valor final.</p>
      </div>
      <div class="card">
        <svg class="icon"><use href="#icon-clock"></use></svg>
        <h3>Pronto no Mesmo Dia</h3>
        <p>A maioria dos serviços do dia a dia sai no mesmo dia útil.</p>
      </div>
    </div>
  </div>
</section>

<section class="servicos" id="servicos">
  <div class="container">
    <div class="section-head">
      <span class="eyebrow">Tabela de Serviços</span>
      <h2>O que sai da nossa bancada</h2>
      <p>Valores de referência para mão de obra — o orçamento final é sempre aprovado por você antes de começarmos.</p>
    </div>
    <div class="table-wrapper">
      <table class="servicos-table">
        <thead>
          <tr><th>Serviço</th><th>Duração</th><th>Valor</th></tr>
        </thead>
        <tbody>
          <tr><td class="servico-nome">Cabos de Frio / Embragem / Acelerador</td><td class="duracao">30 min a 1h30</td><td class="valor">Consultar</td></tr>
          <tr><td class="servico-nome">Cacharia (250cc a 300cc)</td><td class="duracao">3h a 5h</td><td class="valor">Consultar</td></tr>
          <tr><td class="servico-nome">Troca de Rolamentos (125/150/160cc e 250/300cc)</td><td class="duracao">1h a 1h30</td><td class="valor">Consultar</td></tr>
          <tr><td class="servico-nome">Troca de Lona ou Pastilha de Freio (250cc e 300cc)</td><td class="duracao">30 min a 1h30</td><td class="valor">Consultar</td></tr>
          <tr><td class="servico-nome">Diagnóstico Elétrico, com agendamento — todas as motos</td><td class="duracao">1 dia</td><td class="valor">Consultar</td></tr>
          <tr><td class="servico-nome">Troca de Relação, marca Riffel</td><td class="duracao">1h30</td><td class="valor">Consultar</td></tr>
          <tr><td class="servico-nome">Revisão Completa — todas as motos</td><td class="duracao">1 dia</td><td class="valor">Consultar</td></tr>
          <tr><td class="servico-nome">Limpeza de Carburador (motos até aprox. 2020)</td><td class="duracao">2h</td><td class="valor">R$ 80</td></tr>
          <tr><td class="servico-nome">Troca de Óleo, Mobil 10W30 incluso (2009 a 2025)</td><td class="duracao">40 min a 1h30</td><td class="valor">R$ 80</td></tr>
          <tr><td class="servico-nome">Troca de Óleo, Mobil 20W50 incluso (até 2008)</td><td class="duracao">40 min a 1h30</td><td class="valor">R$ 60</td></tr>
          <tr><td class="servico-nome">Troca de Relação Completa (Biz 100/125cc até 2014)</td><td class="duracao">1h30</td><td class="valor">R$ 170</td></tr>
          <tr><td class="servico-nome">Troca de Relação Completa (Titan/CG/Cargo 150/160cc)</td><td class="duracao">1h30</td><td class="valor">R$ 190</td></tr>
          <tr><td class="servico-nome">Troca de Lona ou Pastilha de Freio, qualquer ano (100/125/150/160cc)</td><td class="duracao">30 min a 1h30</td><td class="valor">R$ 70</td></tr>
          <tr><td class="servico-nome">Retentor de Bengala (125 a 160cc até 2017)</td><td class="duracao">3h</td><td class="valor">R$ 80 cada lado</td></tr>
          <tr><td class="servico-nome">Pré-Diagnóstico — qualquer moto e ano</td><td class="duracao">40 min</td><td class="valor">R$ 100</td></tr>
          <tr><td class="servico-nome">Revisão Básica (125/150/160cc, 2008 a 2017) — óleo, filtro, lubrificação de cabos, engraxamento da cacharia, limpeza do sistema de freios, lâmpadas e lavagem</td><td class="duracao">5h</td><td class="valor">R$ 250</td></tr>
          <tr><td class="servico-nome">Troca de Cacharia, marca Riffel (Biz 100cc até 2008 / 125cc até 2014)</td><td class="duracao">2h a 4h</td><td class="valor">R$ 160</td></tr>
          <tr><td class="servico-nome">Troca de Cacharia, marca Riffel (150cc e 160cc)</td><td class="duracao">1h30 a 2h30</td><td class="valor">R$ 160</td></tr>
          <tr><td class="servico-nome">Lâmpada de Lanterna Traseira — todas as motos</td><td class="duracao">40 min</td><td class="valor">R$ 15</td></tr>
          <tr><td class="servico-nome">Lâmpada de Farol H4 Phillips (125cc a partir de 2019; 150/160cc todos os anos)</td><td class="duracao">40 min a 1h30</td><td class="valor">R$ 80</td></tr>
        </tbody>
      </table>
    </div>
    <p class="servicos-note">* Valores de mão de obra. Peças são cobradas à parte, conforme orçamento aprovado.</p>
  </div>
</section>

<section class="agendamento" id="agendamento">
  <div class="container">
    <div class="section-head center">
      <span class="eyebrow">Nova Ordem de Serviço</span>
      <h2>Agende seu Horário</h2>
      <p>Preencha os dados abaixo — confirmamos por telefone ou WhatsApp em até 1 dia útil.</p>
    </div>

    <form class="form-ticket" id="agendamentoForm" novalidate>
      <span class="form-ticket-number" id="ticketNumber">OS Nº ------</span>
      <div class="form-grid">
        <div class="form-field full">
          <label for="nome">Nome completo</label>
          <input type="text" id="nome" name="nome" required autocomplete="name">
        </div>
        <div class="form-field">
          <label for="telefone">Telefone / WhatsApp</label>
          <input type="tel" id="telefone" name="telefone" required placeholder="(11) 90000-0000" autocomplete="tel">
        </div>
        <div class="form-field">
          <label for="email">E-mail <span class="opt">(opcional)</span></label>
          <input type="email" id="email" name="email" autocomplete="email">
        </div>
        <div class="form-field">
          <label for="veiculo">Moto — marca e modelo</label>
          <input type="text" id="veiculo" name="veiculo" required placeholder="Ex.: Honda CG 160 2020">
        </div>
        <div class="form-field">
          <label for="alimentacao">Tipo de alimentação</label>
          <select id="alimentacao" name="alimentacao" required>
            <option value="" disabled selected>Carburada ou Injetada?</option>
            <option>Carburada</option>
            <option>Injetada</option>
          </select>
        </div>
        <div class="form-field">
          <label for="servico">Serviço desejado</label>
          <select id="servico" name="servico" required>
            <option value="" disabled selected>Selecione um serviço</option>
            <option>Cabos de Frio / Embragem / Acelerador</option>
            <option>Cacharia</option>
            <option>Troca de Rolamentos</option>
            <option>Troca de Lona ou Pastilha de Freio</option>
            <option>Diagnóstico Elétrico</option>
            <option>Troca de Relação</option>
            <option>Revisão Completa</option>
            <option>Limpeza de Carburador</option>
            <option>Troca de Óleo</option>
            <option>Retentor de Bengala</option>
            <option>Pré-Diagnóstico</option>
            <option>Revisão Básica</option>
            <option>Lâmpada de Lanterna Traseira</option>
            <option>Lâmpada de Farol</option>
            <option>Outro / ainda não sei</option>
          </select>
        </div>
        <div class="form-field">
          <label for="data">Data preferida</label>
          <input type="date" id="data" name="data" required>
        </div>
        <div class="form-field">
          <label for="horario">Horário preferido</label>
          <select id="horario" name="horario" required>
            <option value="" disabled selected>Selecione um horário</option>
            <option>08:00</option><option>09:00</option><option>10:00</option><option>11:00</option>
            <option>13:00</option><option>14:00</option><option>15:00</option><option>16:00</option><option>17:00</option>
          </select>
        </div>
        <div class="form-field full">
          <label for="observacoes">Observações <span class="opt">(opcional)</span></label>
          <textarea id="observacoes" name="observacoes" placeholder="Algum barulho, luz acesa no painel ou detalhe que devemos saber?"></textarea>
        </div>
      </div>
      <div class="form-submit-row">
        <button type="submit" class="btn btn-primary" id="submitBtn">Confirmar Agendamento</button>
        <span class="form-note">Não cobramos nada para agendar — o orçamento é feito na avaliação.</span>
      </div>
      <p class="form-error" id="formError" role="alert"></p>

      <div class="form-success" id="formSuccess">
        <div class="stamp-confirm" id="stampConfirm">Confirmado</div>
        <h3>Ordem de serviço registrada</h3>
        <p>Recebemos seu pedido. Nossa equipe entra em contato pelo telefone informado para confirmar o horário.</p>
        <div class="os-summary" id="osSummary"></div>
        <div class="form-submit-row" style="justify-content:center; margin-top:24px;">
          <button type="button" class="btn btn-outline" id="novoAgendamento">Fazer novo agendamento</button>
        </div>
      </div>
    </form>
  </div>
</section>

<footer class="site-footer" id="contato">
  <div class="container">
    <div class="footer-grid">
      <div>
        <p class="wordmark">D&amp;D-MOTOS</p>
        <p>Oficina de motos de bairro, cuidando da sua moto com dedicação.</p>
      </div>
      <div>
        <h4>Horário</h4>
        <ul class="footer-list">
          <li>Segunda a sexta — 09h às 17h</li>
          <li>Sábado — somente com agendamento</li>
          <li>Domingo — fechado</li>
        </ul>
      </div>
      <div>
        <h4>Contato</h4>
        <ul class="footer-list">
          <li><svg class="icon"><use href="#icon-pin"></use></svg> Rua Treze, 57 — Guarujá, SP</li>
          <li><svg class="icon"><use href="#icon-phone"></use></svg> (13) 99798-5442</li>
        </ul>
      </div>
      <div>
        <h4>Links Rápidos</h4>
        <ul class="footer-list">
          <li><a href="#servicos">Tabela de Serviços</a></li>
          <li><a href="#agendamento">Agendar Horário</a></li>
          <li><a href="#diferenciais">Diferenciais</a></li>
        </ul>
      </div>
    </div>
    <div class="footer-bottom">© 2026 D&amp;D-Motos. Todos os direitos reservados.</div>
  </div>
</footer>

<script>
  // Menu mobile
  const menuToggle = document.getElementById('menuToggle');
  const navLinks = document.getElementById('navLinks');
  menuToggle.addEventListener('click', () => {
    const isActive = navLinks.classList.toggle('active');
    menuToggle.classList.toggle('active');
    menuToggle.setAttribute('aria-expanded', String(isActive));
    menuToggle.setAttribute('aria-label', isActive ? 'Fechar menu' : 'Abrir menu');
  });
  navLinks.querySelectorAll('a').forEach(link => {
    link.addEventListener('click', () => {
      navLinks.classList.remove('active');
      menuToggle.classList.remove('active');
      menuToggle.setAttribute('aria-expanded', 'false');
      menuToggle.setAttribute('aria-label', 'Abrir menu');
    });
  });

  // Data mínima = hoje
  const dataInput = document.getElementById('data');
  const todayISO = new Date().toISOString().split('T')[0];
  dataInput.setAttribute('min', todayISO);

  // Número da OS (cosmético, gerado no cliente)
  const ticketNumberEl = document.getElementById('ticketNumber');
  function novoNumeroOS() { return Math.floor(10000 + Math.random() * 89999); }
  let osAtual = novoNumeroOS();
  ticketNumberEl.textContent = `OS Nº ${osAtual}`;

  function formatarDataBR(isoDate) {
    const [y, m, d] = isoDate.split('-');
    return `${d}/${m}/${y}`;
  }

  // Envio via WhatsApp (número da oficina)
  const numeroWhatsApp = '5513997985442';
  function montarMensagemWhatsApp(dados) {
    const linhas = [
      'Olá! Gostaria de agendar um horário na D&D-Motos 🔧',
      '',
      `*OS Nº* ${dados.ticket}`,
      `*Nome:* ${dados.nome}`,
      `*Telefone:* ${dados.telefone}`,
      `*Moto:* ${dados.veiculo}`,
      `*Alimentação:* ${dados.alimentacao}`,
      `*Serviço:* ${dados.servico}`,
      `*Data:* ${formatarDataBR(dados.data)}`,
      `*Horário:* ${dados.horario}`,
      `*Observações:* ${dados.observacoes || 'Nenhuma'}`
    ];
    return linhas.join('\n');
  }

  const form = document.getElementById('agendamentoForm');
  const formGrid = form.querySelector('.form-grid');
  const submitRow = form.querySelector('.form-submit-row');
  const formSuccess = document.getElementById('formSuccess');
  const stampConfirm = document.getElementById('stampConfirm');
  const osSummary = document.getElementById('osSummary');
  const submitBtn = document.getElementById('submitBtn');
  const formError = document.getElementById('formError');
  const novoAgendamentoBtn = document.getElementById('novoAgendamento');

  form.addEventListener('submit', async (e) => {
    e.preventDefault();

    if (!form.checkValidity()) {
      form.reportValidity();
      return;
    }

    formError.classList.remove('active');
    submitBtn.disabled = true;
    submitBtn.textContent = 'Enviando...';

    const dados = {
      ticket: osAtual,
      nome: document.getElementById('nome').value.trim(),
      telefone: document.getElementById('telefone').value.trim(),
      email: document.getElementById('email').value.trim(),
      veiculo: document.getElementById('veiculo').value.trim(),
      alimentacao: document.getElementById('alimentacao').value,
      servico: document.getElementById('servico').value,
      data: document.getElementById('data').value,
      horario: document.getElementById('horario').value,
      observacoes: document.getElementById('observacoes').value.trim(),
      status: 'pendente',
      criadoEm: new Date().toISOString()
    };

    try {
      const mensagem = montarMensagemWhatsApp(dados);
      const linkWhatsApp = `https://wa.me/${numeroWhatsApp}?text=${encodeURIComponent(mensagem)}`;
      const novaAba = window.open(linkWhatsApp, '_blank');

      let resumoHTML = `<strong>OS Nº ${dados.ticket}</strong><br>Serviço: ${dados.servico}<br>Data: ${formatarDataBR(dados.data)} às ${dados.horario}<br>Moto: ${dados.veiculo} (${dados.alimentacao})`;
      if (!novaAba) {
        resumoHTML += `<br><br><a href="${linkWhatsApp}" target="_blank" style="color: var(--stamp); font-weight: 600;">Toque aqui para enviar pelo WhatsApp</a>`;
      }
      osSummary.innerHTML = resumoHTML;

      formGrid.style.display = 'none';
      submitRow.style.display = 'none';
      formSuccess.classList.add('active');
      requestAnimationFrame(() => stampConfirm.classList.add('animate'));
    } catch (err) {
      console.error('Erro ao preparar agendamento:', err);
      formError.textContent = 'Não foi possível enviar seu agendamento agora. Tente novamente em instantes ou fale com a gente pelo telefone (13) 99798-5442.';
      formError.classList.add('active');
    } finally {
      submitBtn.disabled = false;
      submitBtn.textContent = 'Confirmar Agendamento';
    }
  });

  novoAgendamentoBtn.addEventListener('click', () => {
    form.reset();
    formGrid.style.display = 'grid';
    submitRow.style.display = 'flex';
    formSuccess.classList.remove('active');
    stampConfirm.classList.remove('animate');
    formError.classList.remove('active');
    osAtual = novoNumeroOS();
    ticketNumberEl.textContent = `OS Nº ${osAtual}`;
    dataInput.setAttribute('min', todayISO);
  });
</script>
</body>
</html>
