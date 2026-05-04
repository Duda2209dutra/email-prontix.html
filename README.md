<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Email Marketing – Prontix Saúde</title>
<link href="https://fonts.googleapis.com/css2?family=Sora:wght@300;400;500;600;700&family=Inter:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }
  body {
    background: #f0f2f5;
    font-family: 'Inter', sans-serif;
    color: #2b2f86;
    -webkit-font-smoothing: antialiased;
  }
  .email-wrapper {
    max-width: 640px;
    margin: 40px auto;
    background: #ffffff;
    border-radius: 20px;
    overflow: hidden;
    box-shadow: 0 20px 60px rgba(43,47,134,0.12);
  }
  .header {
    background: #2b2f86;
    padding: 40px 48px 0;
    position: relative;
    overflow: hidden;
  }
  .header::before {
    content: '';
    position: absolute;
    width: 420px;
    height: 420px;
    border-radius: 50%;
    background: rgba(235,92,88,0.12);
    top: -160px;
    right: -100px;
  }
  .header::after {
    content: '';
    position: absolute;
    width: 200px;
    height: 200px;
    border-radius: 50%;
    background: rgba(255,255,255,0.04);
    bottom: 40px;
    left: -60px;
  }
  .instituto-label {
    font-family: 'Sora', sans-serif;
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 3px;
    color: rgba(255,255,255,0.5);
    text-transform: uppercase;
    margin-bottom: 6px;
  }
  .header-logo {
    font-family: 'Sora', sans-serif;
    font-size: 22px;
    font-weight: 700;
    color: #ffffff;
    margin-bottom: 32px;
  }
  .header-logo span { color: #eb5c58; }
  .hero-box {
    background: #eb5c58;
    border-radius: 16px 16px 0 0;
    padding: 40px 40px 44px;
    position: relative;
    z-index: 1;
  }
  .hero-eyebrow {
    display: inline-block;
    font-family: 'Sora', sans-serif;
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 2.5px;
    color: rgba(255,255,255,0.8);
    text-transform: uppercase;
    background: rgba(255,255,255,0.15);
    padding: 6px 14px;
    border-radius: 100px;
    margin-bottom: 18px;
  }
  .hero-title {
    font-family: 'Sora', sans-serif;
    font-size: 34px;
    font-weight: 700;
    color: #ffffff;
    line-height: 1.15;
    margin-bottom: 14px;
  }
  .hero-subtitle {
    font-size: 15px;
    font-weight: 400;
    color: rgba(255,255,255,0.85);
    line-height: 1.6;
    max-width: 420px;
  }
  .body { padding: 48px; }
  .greeting {
    font-family: 'Sora', sans-serif;
    font-size: 19px;
    font-weight: 600;
    color: #2b2f86;
    margin-bottom: 16px;
  }
  .intro-text {
    font-size: 15px;
    line-height: 1.75;
    color: #444;
    margin-bottom: 36px;
  }
  .section-label {
    font-family: 'Sora', sans-serif;
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 2.5px;
    color: #eb5c58;
    text-transform: uppercase;
    margin-bottom: 10px;
  }
  .section-title {
    font-family: 'Sora', sans-serif;
    font-size: 20px;
    font-weight: 700;
    color: #2b2f86;
    margin-bottom: 24px;
  }
  .features-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 14px;
    margin-bottom: 36px;
  }
  .feature-card {
    background: #f7f8ff;
    border: 1.5px solid #e8eaff;
    border-radius: 14px;
    padding: 20px 18px;
  }
  .feature-icon {
    width: 40px;
    height: 40px;
    border-radius: 10px;
    background: #2b2f86;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 12px;
  }
  .feature-icon.red { background: #eb5c58; }
  .feature-icon svg {
    width: 20px;
    height: 20px;
    fill: none;
    stroke: #fff;
    stroke-width: 1.8;
    stroke-linecap: round;
    stroke-linejoin: round;
  }
  .feature-title {
    font-family: 'Sora', sans-serif;
    font-size: 13px;
    font-weight: 700;
    color: #2b2f86;
    margin-bottom: 6px;
  }
  .feature-desc { font-size: 12.5px; color: #666; line-height: 1.55; }
  .highlight-banner {
    background: #2b2f86;
    border-radius: 16px;
    padding: 28px 32px;
    margin-bottom: 36px;
    display: flex;
    gap: 20px;
    align-items: center;
  }
  .highlight-icon-wrap {
    width: 56px;
    height: 56px;
    border-radius: 14px;
    background: #eb5c58;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
  }
  .highlight-icon-wrap svg {
    width: 28px; height: 28px; fill: none; stroke: #fff;
    stroke-width: 1.8; stroke-linecap: round; stroke-linejoin: round;
  }
  .highlight-text-title {
    font-family: 'Sora', sans-serif;
    font-size: 16px; font-weight: 700; color: #ffffff; margin-bottom: 5px;
  }
  .highlight-text-desc { font-size: 13.5px; color: rgba(255,255,255,0.75); line-height: 1.55; }
  .divider { height: 1px; background: #f0f1f8; margin: 0 0 36px; }
  .benefits-section { margin-bottom: 40px; }
  .benefit-item {
    display: flex; align-items: flex-start; gap: 14px;
    padding: 14px 0; border-bottom: 1px solid #f0f1f8;
  }
  .benefit-item:last-child { border-bottom: none; }
  .benefit-dot {
    width: 28px; height: 28px; border-radius: 8px; background: #eb5c58;
    display: flex; align-items: center; justify-content: center;
    flex-shrink: 0; margin-top: 1px;
  }
  .benefit-dot svg {
    width: 14px; height: 14px; fill: none; stroke: white;
    stroke-width: 2.2; stroke-linecap: round; stroke-linejoin: round;
  }
  .benefit-text { font-size: 14px; color: #333; line-height: 1.6; }
  .benefit-text strong { color: #2b2f86; font-weight: 600; }
  .cta-block {
    background: linear-gradient(135deg, #f7f8ff 0%, #fff0f0 100%);
    border-radius: 16px; padding: 36px; text-align: center;
    margin-bottom: 40px; border: 1.5px solid #e8eaff;
  }
  .cta-title {
    font-family: 'Sora', sans-serif;
    font-size: 18px; font-weight: 700; color: #2b2f86; margin-bottom: 10px;
  }
  .cta-desc { font-size: 14px; color: #666; margin-bottom: 24px; line-height: 1.6; }
  .cta-button {
    display: inline-block; background: #eb5c58; color: #ffffff;
    font-family: 'Sora', sans-serif; font-size: 14px; font-weight: 700;
    padding: 16px 40px; border-radius: 100px; text-decoration: none; margin-bottom: 14px;
  }
  .cta-secondary { display: block; font-size: 12.5px; color: #999; }
  .cta-secondary a { color: #2b2f86; text-decoration: none; font-weight: 500; }
  .quote-block {
    border-left: 4px solid #eb5c58; padding: 16px 20px;
    background: #fff8f8; border-radius: 0 10px 10px 0; margin-bottom: 36px;
  }
  .quote-text {
    font-family: 'Sora', sans-serif; font-size: 15px;
    font-style: italic; color: #2b2f86; line-height: 1.6;
  }
  .quote-author { font-size: 12px; color: #999; margin-top: 8px; font-weight: 500; }
  .footer { background: #2b2f86; padding: 36px 48px; text-align: center; }
  .footer-logo {
    font-family: 'Sora', sans-serif; font-size: 16px;
    font-weight: 700; color: #fff; margin-bottom: 8px;
  }
  .footer-logo span { color: #eb5c58; }
  .footer-tagline { font-size: 12px; color: rgba(255,255,255,0.5); margin-bottom: 20px; }
  .footer-links { display: flex; justify-content: center; gap: 24px; margin-bottom: 20px; }
  .footer-links a { font-size: 12px; color: rgba(255,255,255,0.6); text-decoration: none; }
  .footer-copy { font-size: 11px; color: rgba(255,255,255,0.3); line-height: 1.6; }
  @media (max-width: 520px) {
    .body { padding: 28px 24px; }
    .header { padding: 28px 24px 0; }
    .features-grid { grid-template-columns: 1fr; }
    .hero-title { font-size: 24px; }
    .highlight-banner { flex-direction: column; }
    .footer { padding: 28px 24px; }
    .footer-links { flex-wrap: wrap; gap: 12px; }
    .hero-box { padding: 28px 24px 32px; }
  }
</style>
</head>
<body>
<div class="email-wrapper">
  <div class="header">
    <div class="instituto-label">Instituto de Saúde</div>
    <div class="header-logo">Instituto <span>●</span> Saúde</div>
    <div class="hero-box">
      <span class="hero-eyebrow">Novidade Exclusiva</span>
      <h1 class="hero-title">Conheça o<br>Prontix Saúde</h1>
      <p class="hero-subtitle">A plataforma digital que transforma a gestão da sua clínica — do agendamento ao prontuário eletrônico — com praticidade e segurança.</p>
    </div>
  </div>
  <div class="body">
    <p class="greeting">Prezado(a) colaborador(a),</p>
    <p class="intro-text">É com muito entusiasmo que apresentamos o <strong style="color:#2b2f86;">Prontix Saúde</strong>, a nova solução tecnológica adotada pelo Instituto para modernizar e aprimorar nossos processos internos. Desenvolvido especialmente para instituições e profissionais de saúde, o Prontix integra em um único ambiente tudo que você precisa para oferecer um atendimento de excelência.</p>
    <div class="section-label">Funcionalidades</div>
    <div class="section-title">O que o Prontix oferece</div>
    <div class="features-grid">
      <div class="feature-card">
        <div class="feature-icon">
          <svg viewBox="0 0 24 24"><rect x="3" y="4" width="18" height="18" rx="2"/><line x1="16" y1="2" x2="16" y2="6"/><line x1="8" y1="2" x2="8" y2="6"/><line x1="3" y1="10" x2="21" y2="10"/></svg>
        </div>
        <div class="feature-title">Agendamento Online</div>
        <div class="feature-desc">Agenda digital integrada com confirmações automáticas e gestão de horários em tempo real.</div>
      </div>
      <div class="feature-card">
        <div class="feature-icon red">
          <svg viewBox="0 0 24 24"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><polyline points="14 2 14 8 20 8"/><line x1="12" y1="18" x2="12" y2="12"/><line x1="9" y1="15" x2="15" y2="15"/></svg>
        </div>
        <div class="feature-title">Prontuário Eletrônico</div>
        <div class="feature-desc">Histórico clínico completo, seguro e acessível a qualquer momento e dispositivo.</div>
      </div>
      <div class="feature-card">
        <div class="feature-icon red">
          <svg viewBox="0 0 24 24"><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 0 0-3-3.87"/><path d="M16 3.13a4 4 0 0 1 0 7.75"/></svg>
        </div>
        <div class="feature-title">Gestão de Pacientes</div>
        <div class="feature-desc">Cadastro unificado com histórico de consultas, exames e documentos por paciente.</div>
      </div>
      <div class="feature-card">
        <div class="feature-icon">
          <svg viewBox="0 0 24 24"><line x1="12" y1="1" x2="12" y2="23"/><path d="M17 5H9.5a3.5 3.5 0 0 0 0 7h5a3.5 3.5 0 0 1 0 7H6"/></svg>
        </div>
        <div class="feature-title">Faturamento e Cobrança</div>
        <div class="feature-desc">Emissão de recibos, controle financeiro e integração com planos de saúde simplificados.</div>
      </div>
      <div class="feature-card">
        <div class="feature-icon">
          <svg viewBox="0 0 24 24"><polyline points="22 12 18 12 15 21 9 3 6 12 2 12"/></svg>
        </div>
        <div class="feature-title">Telemedicina</div>
        <div class="feature-desc">Consultas remotas integradas à plataforma, com vídeo, chat e prescrição digital.</div>
      </div>
      <div class="feature-card">
        <div class="feature-icon red">
          <svg viewBox="0 0 24 24"><path d="M18 20V10"/><path d="M12 20V4"/><path d="M6 20v-6"/></svg>
        </div>
        <div class="feature-title">Relatórios e Dashboards</div>
        <div class="feature-desc">Indicadores de desempenho e relatórios gerenciais para tomada de decisão estratégica.</div>
      </div>
    </div>
    <div class="highlight-banner">
      <div class="highlight-icon-wrap">
        <svg viewBox="0 0 24 24"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>
      </div>
      <div>
        <div class="highlight-text-title">Segurança e Conformidade com a LGPD</div>
        <div class="highlight-text-desc">O Prontix Saúde segue rigorosamente a Lei Geral de Proteção de Dados (LGPD), garantindo privacidade e segurança no tratamento dos dados dos seus pacientes e colaboradores.</div>
      </div>
    </div>
    <div class="divider"></div>
    <div class="section-label">Por que adotar</div>
    <div class="section-title">Benefícios para o Instituto</div>
    <div class="benefits-section">
      <div class="benefit-item">
        <div class="benefit-dot"><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg></div>
        <div class="benefit-text"><strong>Redução de erros operacionais</strong> — processos automatizados eliminam retrabalho e falhas no agendamento e faturamento.</div>
      </div>
      <div class="benefit-item">
        <div class="benefit-dot"><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg></div>
        <div class="benefit-text"><strong>Acesso em qualquer dispositivo</strong> — plataforma 100% em nuvem, acessível por computadores, tablets e smartphones.</div>
      </div>
      <div class="benefit-item">
        <div class="benefit-dot"><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg></div>
        <div class="benefit-text"><strong>Agilidade no atendimento</strong> — prontuários digitais agilizam a consulta e o registro de informações clínicas.</div>
      </div>
      <div class="benefit-item">
        <div class="benefit-dot"><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg></div>
        <div class="benefit-text"><strong>Integração completa</strong> — todas as áreas do Instituto conectadas em uma única plataforma, do front-desk ao gestor.</div>
      </div>
      <div class="benefit-item">
        <div class="benefit-dot"><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg></div>
        <div class="benefit-text"><strong>Suporte especializado</strong> — equipe técnica dedicada para onboarding e treinamento de todos os colaboradores.</div>
      </div>
    </div>
    <div class="quote-block">
      <div class="quote-text">"A tecnologia a serviço da saúde não é o futuro — é o presente. O Prontix Saúde é o passo que o Instituto precisava para levar nosso atendimento a um novo patamar de qualidade."</div>
      <div class="quote-author">— Diretoria do Instituto</div>
    </div>
    <div class="cta-block">
      <div class="cta-title">Explore o Prontix Saúde</div>
      <div class="cta-desc">Acesse a plataforma e descubra como o Prontix pode transformar a rotina da sua equipe. Uma demonstração completa será realizada em breve para todos os colaboradores.</div>
      <a href="https://prontixsaude.com.br/" class="cta-button">Acessar o Prontix Saúde →</a>
      <span class="cta-secondary">Dúvidas? Entre em contato com o setor de TI ou acesse <a href="https://prontixsaude.com.br/">prontixsaude.com.br</a></span>
    </div>
  </div>
  <div class="footer">
    <div class="footer-logo">Instituto <span>●</span> Saúde</div>
    <div class="footer-tagline">Cuidando de quem cuida</div>
    <div class="footer-links">
      <a href="#">Site Institucional</a>
      <a href="#">Portal do Colaborador</a>
      <a href="#">Prontix Saúde</a>
      <a href="#">Contato</a>
    </div>
    <div class="footer-copy">
      © 2025 Instituto Saúde — Todos os direitos reservados.<br>
      Você está recebendo este e-mail por ser colaborador(a) do Instituto.<br>
      <a href="#" style="color:rgba(255,255,255,0.4);text-decoration:none;">Cancelar inscrição</a>
    </div>
  </div>
</div>
</body>
</html>
