<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Agrinho 2026 | Educação e Transformação</title>

  <meta name="description" content="Site sobre o Agrinho 2026 - educação, cidadania, sustentabilidade e transformação.">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    :root {
      --verde: #16853a;
      --verde-escuro: #075b28;
      --verde-claro: #e8f7ed;
      --amarelo: #ffc928;
      --laranja: #f28c28;
      --branco: #ffffff;
      --cinza: #f5f7f6;
      --texto: #26332b;
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      color: var(--texto);
      background: var(--branco);
      line-height: 1.6;
    }

    /* HEADER */

    header {
      position: fixed;
      width: 100%;
      top: 0;
      z-index: 1000;
      background: rgba(255, 255, 255, 0.96);
      box-shadow: 0 2px 15px rgba(0,0,0,0.08);
    }

    nav {
      max-width: 1200px;
      margin: auto;
      height: 75px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0 25px;
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 10px;
      font-size: 25px;
      font-weight: bold;
      color: var(--verde);
    }

    .logo span {
      color: var(--laranja);
    }

    .menu {
      display: flex;
      gap: 25px;
      list-style: none;
    }

    .menu a {
      text-decoration: none;
      color: var(--texto);
      font-weight: bold;
      transition: 0.3s;
    }

    .menu a:hover {
      color: var(--verde);
    }

    /* HERO */

    .hero {
      min-height: 100vh;
      padding: 130px 25px 80px;
      display: flex;
      align-items: center;
      background:
        linear-gradient(135deg, rgba(7,91,40,0.95), rgba(22,133,58,0.85)),
        radial-gradient(circle at top right, #ffc928, transparent 35%);
      color: white;
      overflow: hidden;
    }

    .hero-content {
      max-width: 1200px;
      width: 100%;
      margin: auto;
      display: grid;
      grid-template-columns: 1.2fr 0.8fr;
      gap: 50px;
      align-items: center;
    }

    .hero h1 {
      font-size: clamp(45px, 7vw, 85px);
      line-height: 0.95;
      margin-bottom: 25px;
    }

    .hero h1 span {
      color: var(--amarelo);
    }

    .hero p {
      font-size: 20px;
      max-width: 650px;
      margin-bottom: 35px;
      color: #f1fff4;
    }

    .buttons {
      display: flex;
      gap: 15px;
      flex-wrap: wrap;
    }

    .btn {
      display: inline-block;
      padding: 14px 25px;
      border-radius: 50px;
      text-decoration: none;
      font-weight: bold;
      transition: 0.3s;
    }

    .btn-primary {
      background: var(--amarelo);
      color: #503900;
    }

    .btn-primary:hover {
      transform: translateY(-3px);
      box-shadow: 0 10px 25px rgba(0,0,0,0.2);
    }

    .btn-secondary {
      border: 2px solid white;
      color: white;
    }

    .btn-secondary:hover {
      background: white;
      color: var(--verde);
    }

    .hero-card {
      background: rgba(255,255,255,0.12);
      border: 1px solid rgba(255,255,255,0.25);
      backdrop-filter: blur(10px);
      border-radius: 30px;
      padding: 45px;
      text-align: center;
      box-shadow: 0 20px 50px rgba(0,0,0,0.2);
    }

    .hero-card .emoji {
      font-size: 100px;
      margin-bottom: 15px;
    }

    .hero-card h2 {
      font-size: 32px;
      color: var(--amarelo);
    }

    /* SEÇÕES */

    section {
      padding: 90px 25px;
    }

    .container {
      max-width: 1150px;
      margin: auto;
    }

    .section-title {
      text-align: center;
      margin-bottom: 55px;
    }

    .section-title small {
      color: var(--verde);
      text-transform: uppercase;
      font-weight: bold;
      letter-spacing: 2px;
    }

    .section-title h2 {
      font-size: 42px;
      color: var(--verde-escuro);
      margin-top: 8px;
    }

    .section-title p {
      max-width: 700px;
      margin: 15px auto 0;
      color: #66736b;
    }

    /* SOBRE */

    .about {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 50px;
      align-items: center;
    }

    .about-image {
      min-height: 400px;
      border-radius: 30px;
      background: linear-gradient(135deg, var(--verde), #52b96e);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 130px;
      box-shadow: 15px 15px 0 var(--amarelo);
    }

    .about-text h3 {
      font-size: 32px;
      color: var(--verde-escuro);
      margin-bottom: 20px;
    }

    .about-text p {
      margin-bottom: 15px;
      color: #5b665f;
    }

    /* CARDS */

    .cards {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 25px;
    }

    .card {
      background: white;
      border-radius: 20px;
      padding: 35px 28px;
      box-shadow: 0 10px 35px rgba(0,0,0,0.08);
      border-top: 5px solid var(--verde);
      transition: 0.3s;
    }

    .card:hover {
      transform: translateY(-8px);
    }

    .card-icon {
      font-size: 45px;
      margin-bottom: 15px;
    }

    .card h3 {
      color: var(--verde-escuro);
      margin-bottom: 10px;
      font-size: 22px;
    }

    .card p {
      color: #68736d;
    }

    /* OBJETIVOS */

    .objectives {
      background: var(--cinza);
    }

    .objective-list {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 20px;
    }

    .objective {
      display: flex;
      gap: 18px;
      align-items: flex-start;
      padding: 25px;
      background: white;
      border-radius: 15px;
      box-shadow: 0 5px 20px rgba(0,0,0,0.05);
    }

    .check {
      width: 40px;
      height: 40px;
      min-width: 40px;
      background: var(--verde);
      color: white;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: bold;
    }

    /* DESTAQUE */

    .highlight {
      background: linear-gradient(135deg, var(--laranja), #f6a52d);
      color: white;
      text-align: center;
    }

    .highlight h2 {
      font-size: 45px;
      margin-bottom: 15px;
    }

    .highlight p {
      max-width: 750px;
      margin: auto;
      font-size: 18px;
    }

    /* PARTICIPAÇÃO */

    .participation {
      text-align: center;
    }

    .participation-box {
      max-width: 800px;
      margin: auto;
      padding: 50px;
      border-radius: 30px;
      background: var(--verde-claro);
    }

    .participation-box h2 {
      color: var(--verde-escuro);
      font-size: 35px;
      margin-bottom: 15px;
    }

    .participation-box p {
      margin-bottom: 25px;
      color: #536058;
    }

    /* FOOTER */

    footer {
      background: #063d1d;
      color: white;
      padding: 45px 25px;
      text-align: center;
    }

    footer h3 {
      color: var(--amarelo);
      font-size: 25px;
      margin-bottom: 10px;
    }

    footer p {
      color: #cde5d4;
    }

    .footer-line {
      width: 70px;
      height: 4px;
      background: var(--laranja);
      margin: 20px auto;
      border-radius: 5px;
    }

    /* RESPONSIVO */

    @media (max-width: 850px) {

      .menu {
        display: none;
      }

      .hero-content {
        grid-template-columns: 1fr;
        text-align: center;
      }

      .hero p {
        margin-left: auto;
        margin-right: auto;
      }

      .buttons {
        justify-content: center;
      }

      .about {
        grid-template-columns: 1fr;
      }

      .cards {
        grid-template-columns: 1fr;
      }

      .objective-list {
        grid-template-columns: 1fr;
      }

      .about-image {
        min-height: 300px;
      }
    }

    @media (max-width: 500px) {

      .hero {
        padding-top: 110px;
      }

      .hero-card {
        padding: 30px 20px;
      }

      .hero-card .emoji {
        font-size: 70px;
      }

      .section-title h2 {
        font-size: 32px;
      }

      .highlight h2 {
        font-size: 32px;
      }

      .participation-box {
        padding: 35px 20px;
      }
    }
  </style>
</head>

<body>

  <!-- MENU -->

  <header>
    <nav>
      <div class="logo">
        🌱 Agrinho <span>2026</span>
      </div>

      <ul class="menu">
        <li><a href="#inicio">Início</a></li>
        <li><a href="#sobre">Sobre</a></li>
        <li><a href="#temas">Temas</a></li>
        <li><a href="#objetivos">Objetivos</a></li>
        <li><a href="#participar">Participação</a></li>
      </ul>
    </nav>
  </header>

  <!-- HERO -->

  <main>

    <section class="hero" id="inicio">
      <div class="hero-content">

        <div>
          <h1>
            Agrinho<br>
            <span>2026</span>
          </h1>

          <p>
            Educação, criatividade e cidadania para construir um futuro
            melhor para todos.
          </p>

          <div class="buttons">
            <a href="#sobre" class="btn btn-primary">
              Conheça o projeto
            </a>

            <a href="#participar" class="btn btn-secondary">
              Saiba como participar
            </a>
          </div>
        </div>

        <div class="hero-card">
          <div class="emoji">🌱🚜</div>
          <h2>Educação que transforma</h2>
          <p>
            Aprender, criar e transformar a realidade.
          </p>
        </div>

      </div>
    </section>

    <!-- SOBRE -->

    <section id="sobre">
      <div class="container">

        <div class="section-title">
          <small>Conheça</small>
          <h2>Sobre o Agrinho</h2>
          <p>
            Um projeto que aproxima educação, comunidade e temas importantes
            para a formação dos estudantes.
          </p>
        </div>

        <div class="about">

          <div class="about-image">
            🌾
          </div>

          <div class="about-text">
            <h3>Aprender para transformar</h3>

            <p>
              O Agrinho é uma iniciativa educacional que trabalha diferentes
              temas relacionados à cidadania, sustentabilidade, meio ambiente,
              saúde, tecnologia e desenvolvimento social.
            </p>

            <p>
              Por meio de atividades educativas e projetos criativos,
              estudantes podem refletir sobre os desafios do presente e
              imaginar soluções para o futuro.
            </p>

            <p>
              Este site apresenta uma versão informativa sobre o tema
              <strong>Agrinho 2026</strong>.
            </p>
          </div>

        </div>
      </div>
    </section>

    <!-- TEMAS -->

    <section class="objectives" id="temas">
      <div class="container">

        <div class="section-title">
          <small>Explore</small>
          <h2>Temas importantes</h2>
          <p>
            Alguns assuntos que podem fazer parte de projetos educativos.
          </p>
        </div>

        <div class="cards">

          <div class="card">
            <div class="card-icon">🌳</div>
            <h3>Meio Ambiente</h3>
            <p>
              Preservação da natureza, sustentabilidade e responsabilidade
              ambiental.
            </p>
          </div>

          <div class="card">
            <div class="card-icon">💡</div>
            <h3>Inovação</h3>
            <p>
              Criatividade e tecnologia utilizadas para encontrar soluções
              para problemas do cotidiano.
            </p>
          </div>

          <div class="card">
            <div class="card-icon">🤝</div>
            <h3>Cidadania</h3>
            <p>
              Respeito, participação social, cooperação e construção de uma
              sociedade melhor.
            </p>
          </div>

          <div class="card">
            <div class="card-icon">📚</div>
            <h3>Educação</h3>
            <p>
              Conhecimento como ferramenta para transformar pessoas e
              comunidades.
            </p>
          </div>

          <div class="card">
            <div class="card-icon">🌱</div>
            <h3>Sustentabilidade</h3>
            <p>
              Desenvolvimento consciente e utilização responsável dos
              recursos naturais.
            </p>
          </div>

          <div class="card">
            <div class="card-icon">👩‍🏫</div>
            <h3>Escola</h3>
            <p>
              A escola como espaço de aprendizado, criatividade, diálogo e
              transformação.
            </p>
          </div>

        </div>
      </div>
    </section>

    <!-- OBJETIVOS -->

    <section id="objetivos">
      <div class="container">

        <div class="section-title">
          <small>Por que participar?</small>
          <h2>Objetivos</h2>
          <p>
            O aprendizado pode ultrapassar os limites da sala de aula.
          </p>
        </div>

        <div class="objective-list">

          <div class="objective">
            <div class="check">✓</div>
            <div>
              <h3>Estimular a criatividade</h3>
              <p>
                Incentivar os estudantes a desenvolverem novas ideias e
                soluções.
              </p>
            </div>
          </div>

          <div class="objective">
            <div class="check">✓</div>
            <div>
              <h3>Valorizar a educação</h3>
              <p>
                Mostrar como o conhecimento pode contribuir para a sociedade.
              </p>
            </div>
          </div>

          <div class="objective">
            <div class="check">✓</div>
            <div>
              <h3>Promover cidadania</h3>
              <p>
                Desenvolver consciência sobre direitos, deveres e participação
                social.
              </p>
            </div>
          </div>

          <div class="objective">
            <div class="check">✓</div>
            <div>
              <h3>Incentivar sustentabilidade</h3>
              <p>
                Refletir sobre atitudes que ajudam a preservar o planeta.
              </p>
            </div>
          </div>

        </div>
      </div>
    </section>

    <!-- DESTAQUE -->

    <section class="highlight">
      <div class="container">
        <h2>🌎 O futuro começa com nossas escolhas</h2>

        <p>
          Pequenas atitudes podem gerar grandes mudanças. A educação é uma
          das principais ferramentas para construir um futuro mais sustentável,
          justo e consciente.
        </p>
      </div>
    </section>

    <!-- PARTICIPAÇÃO -->

    <section id="participar" class="participation">
      <div class="container">

        <div class="section-title">
          <small>Faça parte</small>
          <h2>Participação</h2>
        </div>

        <div class="participation-box">

          <h2>Quer saber mais?</h2>

          <p>
            Para informações oficiais sobre regras, inscrições, categorias,
            datas e atividades do Agrinho 2026, consulte os canais oficiais
            da organização e da sua escola.
          </p>

          <a
            href="https://www.sistemafaep.org.br/"
            target="_blank"
            class="btn btn-primary"
          >
            Visitar site oficial
          </a>

        </div>
      </div>
    </section>

  </main>

  <!-- FOOTER -->

  <footer>
    <h3>🌱 Agrinho 2026</h3>

    <div class="footer-line"></div>

    <p>
      Projeto educativo • Educação • Cidadania • Sustentabilidade
    </p>

    <p style="margin-top: 15px; font-size: 14px;">
      Site desenvolvido para fins educacionais.
    </p>
  </footer>

</body>
</html>