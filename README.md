<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Meu Projeto no GitHub</title>
  <meta name="description" content="Página inicial simples para um projeto hospedado no GitHub Pages." />
  <style>
    :root {
      --bg: #0f172a;      /* fundo (slate-900) */
      --panel: #111827;  /* painel (gray-900) */
      --text: #e5e7eb;   /* texto (gray-200) */
      --muted: #9ca3af;  /* texto secundário */
      --primary: #60a5fa;/* azul */
      --accent: #22d3ee; /* ciano */
      --card: #1f2937;   /* card */
    }
    * { box-sizing: border-box; }
    html, body {
      margin: 0;
      padding: 0;
      background: linear-gradient(120deg, var(--bg), #0b1020 60%, #0a0f1a);
      color: var(--text);
      font-family: system-ui, -apple-system, Segoe UI, Roboto, Ubuntu, Cantarell, "Helvetica Neue", Arial, "Noto Sans", "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", sans-serif;
      line-height: 1.6;
    }
    a { color: var(--primary); text-decoration: none; }
    a:hover { color: var(--accent); }

    /* Cabeçalho e navegação */
    header {
      position: sticky;
      top: 0;
      z-index: 50;
      backdrop-filter: saturate(180%) blur(8px);
      background: rgba(17, 24, 39, 0.7);
      border-bottom: 1px solid rgba(96, 165, 250, 0.2);
    }
    .container {
      max-width: 960px;
      margin: 0 auto;
      padding: 0 16px;
    }
    .nav {
      display: flex;
      align-items: center;
      justify-content: space-between;
      min-height: 64px;
    }
    .brand {
      display: flex;
      align-items: center;
      gap: 10px;
      font-weight: 700;
      letter-spacing: 0.2px;
    }
    .brand .logo {
      width: 28px;
      height: 28px;
      border-radius: 8px;
      background: linear-gradient(135deg, var(--primary), var(--accent));
      box-shadow: 0 6px 20px rgba(96, 165, 250, 0.35);
    }
    .menu {
      display: flex;
      gap: 20px;
    }
    .menu a {
      padding: 8px 10px;
      border-radius: 6px;
      transition: background 0.2s;
    }
    .menu a:hover {
      background: rgba(96,165,250,0.1);
    }

    /* Hero */
    .hero {
      padding: 64px 0;
      text-align: center;
    }
    .hero h1 {
      font-size: clamp(28px, 4.5vw, 44px);
      margin: 0 0 12px;
    }
    .hero p {
      max-width: 720px;
      margin: 0 auto 24px;
      color: var(--muted);
    }
    .hero .cta {
      display: inline-block;
      margin-top: 8px;
      padding: 10px 16px;
      border-radius: 8px;
      background: linear-gradient(135deg, rgba(96,165,250,0.25), rgba(34,211,238,0.25));
      border: 1px solid rgba(96,165,250,0.35);
      color: var(--text);
      transition: transform 0.15s ease, box-shadow 0.15s ease;
    }
    .cta:hover {
      transform: translateY(-1px);
      box-shadow: 0 10px 24px rgba(34,211,238,0.25);
    }
    .hero img {
      width: 100%;
      max-width: 960px;
      height: auto;
      border-radius: 12px;
      margin-top: 24px;
      border: 1px solid rgba(96,165,250,0.25);
      box-shadow: 0 12px 30px rgba(0,0,0,0.35);
    }

    /* Seções */
    section {
      padding: 40px 0;
      border-top: 1px solid rgba(96,165,250,0.12);
    }
    section h2 {
      font-size: 24px;
      margin: 0 0 12px;
    }
    .cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
      gap: 16px;
      margin-top: 12px;
    }
    .card {
      background: linear-gradient(180deg, var(--card), #172032);
      border: 1px solid rgba(96,165,250,0.15);
      border-radius: 12px;
      padding: 16px;
    }
    .card h3 {
      margin: 0 0 8px;
      font-size: 18px;
    }
    .card p {
      margin: 0;
      color: var(--muted);
    }

    /* Rodapé */
    footer {
      padding: 28px 0 40px;
      border-top: 1px solid rgba(96,165,250,0.12);
      color: var(--muted);
    }
    .footer-links {
      display: flex;
      gap: 16px;
      flex-wrap: wrap;
      margin-bottom: 8px;
    }
    .footer-note {
      font-size: 14px;
    }
  </style>
</head>
<body>
  <!-- Cabeçalho -->
  <header>
    <div class="container nav">
      <div class="brand">
        <span class="logo" aria-hidden="true"></span>
        <span>Meu Projeto</span>
      </div>
      <nav class="menu" aria-label="Navegação principal">
        <a href="#sobre">Sobre</a>
        <a href="#projetos">Projetos</a>
        <a href="#contato">Contato</a>
      </nav>
    </div>
  </header>

  <!-- Hero -->
  <main>
    <section class="hero container">
      <h1>Bem-vindo ao Meu Projeto</h1>
      <p>Uma página inicial simples, moderna e leve para apresentar seu repositório no GitHub. Edite os textos, links e a imagem abaixo para personalizar.</p>
      <a class="cta" href="https://github.com/seu-usuario/seu-repositorio" target="_blank" rel="noopener">Ver no GitHub</a>

      <!-- Imagem de destaque: troque o src por uma imagem sua -->
      <img src="https://images.unsplash.com/photo-1518770660439-4636190af475?q=80&w=1600&auto=format&fit=crop" alt="Imagem de destaque do projeto" />
    </section>

    <!-- Seção Sobre -->
    <section id="sobre">
      <div class="container">
        <h2>Sobre</h2>
        <p>Este projeto demonstra uma página inicial para GitHub Pages, com navegação simples e cards de conteúdo. Ideal para apresentar objetivos, tecnologias e links importantes.</p>
        <div class="cards">
          <div class="card">
            <h3>Tecnologias</h3>
            <p>HTML, CSS, e recursos estáticos. Sem dependências externas.</p>
          </div>
          <div class="card">
            <h3>Objetivo</h3>
            <p>Fornecer um ponto de entrada claro e bonito para seus repositórios.</p>
          </div>
          <div class="card">
            <h3>Customização</h3>
            <p>Edite cores em <code>:root</code>, troque textos e adicione seções conforme necessário.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Seção Projetos -->
    <section id="projetos">
      <div class="container">
        <h2>Projetos</h2>
        <div class="cards">
          <div class="card">
            <h3>Projeto A</h3>
            <p>Descrição breve do Projeto A. <a href="https://github.com/seu-usuario/projeto-a" target="_blank" rel="noopener">Repositório</a></p>
          </div>
          <div class="card">
            <h3>Projeto B</h3>
            <p>Descrição breve do Projeto B. <a href="https://github.com/seu-usuario/projeto-b" target="_blank" rel="noopener">Repositório</a></p>
          </div>
          <div class="card">
            <h3>Projeto C</h3>
            <p>Descrição breve do Projeto C. <a href="https://github.com/seu-usuario/projeto-c" target="_blank" rel="noopener">Repositório</a></p>
          </div>
        </div>
      </div>
    </section>

    <!-- Seção Contato -->
    <section id="contato">
      <div class="container">
        <h2>Contato</h2>
        <p>Quer trocar uma ideia ou contribuir? Envie uma mensagem:</p>
        <div class="cards">
          <div class="card">
            <h3>Email</h3>
            <p><a href="mailto:voce@exemplo.com">voce@exemplo.com</a></p>
          </div>
          <div class="card">
            <h3>GitHub</h3>
            <p><a href="https://github.com/seu-usuario" target="_blank" rel="noopener">@seu-usuario</a></p>
          </div>
          <div class="card">
            <h3>LinkedIn</h3>
            <p><a href="https://linkedin.com/in/seu-usuario" target="_blank" rel="noopener">linkedin.com/in/seu-usuario</a></p>
          </div>
        </div>
      </div>
    </section>
  </main>

  <!-- Rodapé -->
  <footer>
    <div class="container">
      <div class="footer-links">
        <a href="#sobre">Sobre</a>
        <a href="#projetos">Projetos</a>
        <a href="#contato">Contato</a>
      </div>
      <div class="footer-note">© <span id="year"></span> Meu Projeto · Feito com HTML + CSS</div>
    </div>
  </footer>

  <script>
    // Atualiza o ano automaticamente
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>
