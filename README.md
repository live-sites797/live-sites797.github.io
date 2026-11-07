
```html
<!doctype html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="theme-color" content="#100919">
  <meta name="description" content="Conheça o servidor Minecraft Acer. Endereço acerSrV.aternos.me e porta Bedrock 55598.">

  <title>Acer — Entre em outra dimensão</title>

  <style>
    @import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Space+Mono:wght@400;700&display=swap');

    :root {
      --bg: #100919;
      --text: #f6f0ff;
      --muted: #afa0bf;
      --purple: #b575ff;
      --red: #ff435d;
    }

    * {
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
      scroll-padding-top: 30px;
    }

    body {
      margin: 0;
      background: var(--bg);
      color: var(--text);
      font-family: 'Space Grotesk', sans-serif;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    button {
      font: inherit;
      cursor: pointer;
    }

    header,
    main,
    footer {
      max-width: 1240px;
      margin: auto;
    }

    header {
      height: 100px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0 32px;
      border-bottom: 1px solid #ffffff16;
    }

    .brand {
      font-size: 27px;
      font-weight: 700;
      letter-spacing: 3px;
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .mark {
      color: var(--purple);
      font-size: 35px;
    }

    nav {
      display: flex;
      gap: 34px;
      align-items: center;
      font-size: 13px;
    }

    nav a:hover {
      color: var(--purple);
    }

    .nav-play {
      border: 1px solid #795096;
      padding: 12px 20px;
    }

    .hero {
      min-height: 650px;
      display: grid;
      grid-template-columns: 1.05fr 1fr;
      align-items: center;
      padding: 60px 32px 35px;
      position: relative;
    }

    .eyebrow {
      font-family: 'Space Mono', monospace;
      text-transform: uppercase;
      letter-spacing: 2px;
      font-size: 11px;
      color: var(--purple);
    }

    .eyebrow::before {
      content: '■';
      margin-right: 12px;
      color: var(--red);
    }

    h1 {
      font-size: clamp(54px, 6.1vw, 82px);
      line-height: 1.04;
      letter-spacing: -4px;
      margin: 25px 0;
    }

    h1 em {
      font-style: normal;
      color: var(--purple);
    }

    .hero p {
      max-width: 410px;
      font-size: 16px;
      line-height: 1.8;
      color: var(--muted);
    }

    .buttons {
      display: flex;
      gap: 14px;
      margin-top: 30px;
      flex-wrap: wrap;
    }

    .primary,
    .secondary {
      padding: 17px 23px;
      border: 1px solid #ffffff25;
      font-size: 14px;
      font-weight: 700;
      color: white;
      display: inline-flex;
      gap: 24px;
      align-items: center;
    }

    .primary {
      background: var(--red);
      border-color: var(--red);
      box-shadow: 5px 5px 0 #75253b;
    }

    .primary:hover {
      background: #ff6278;
    }

    .secondary {
      background: #21152d;
    }

    .secondary:hover {
      border-color: var(--purple);
    }

    .micro {
      font: 10px 'Space Mono', monospace;
      color: #8e7f9d;
      letter-spacing: 1px;
      margin-top: 25px;
    }

    /* Cenário do Enderman */

    .scene {
      height: 520px;
      position: relative;
      display: flex;
      align-items: center;
      justify-content: center;
      isolation: isolate;
      background: radial-gradient(
        ellipse at 55% 45%,
        #632c8e66,
        transparent 64%
      );
    }

    .scene::after {
      content: '';
      position: absolute;
      bottom: 18px;
      width: 86%;
      height: 100px;
      background:
        repeating-linear-gradient(
          90deg,
          transparent 0 49px,
          #b575ff15 50px
        ),
        repeating-linear-gradient(
          0deg,
          transparent 0 24px,
          #b575ff15 25px
        );
      transform: perspective(150px) rotateX(45deg);
      z-index: -1;
    }

    .portal {
      position: absolute;
      width: 255px;
      height: 395px;
      border: 16px solid #32203f;
      box-shadow:
        0 0 0 4px #724398,
        0 0 70px #9f36ff55,
        inset 0 0 65px #7d28c977;
      transform: rotate(-9deg);
      background: repeating-linear-gradient(
        0deg,
        #8724cb15 0 18px,
        #d571ff15 19px 20px
      );
    }

    .enderman {
      width: 220px;
      height: 390px;
      position: relative;
      filter: drop-shadow(12px 12px 0 #05030766);
      transform: rotate(6deg);
      animation: float 5s ease-in-out infinite;
    }

    .head {
      position: absolute;
      top: 12px;
      left: 58px;
      width: 108px;
      height: 94px;
      background: #17121f;
      border-top: 12px solid #2c2235;
      border-right: 14px solid #09070d;
      z-index: 3;
    }

    .eye {
      position: absolute;
      width: 40px;
      height: 13px;
      top: 45px;
      background: #d991ff;
      box-shadow: 0 0 20px #d261ff;
    }

    .eye::after {
      content: '';
      position: absolute;
      left: 15px;
      top: 0;
      width: 12px;
      height: 13px;
      background: #f5c7ff;
    }

    .eye.left {
      left: 0;
    }

    .eye.right {
      right: -6px;
    }

    .torso {
      position: absolute;
      top: 106px;
      left: 73px;
      width: 80px;
      height: 110px;
      background: #17121f;
      border-right: 15px solid #08060c;
    }

    .arm,
    .leg {
      position: absolute;
      background: #17121f;
      border-right: 9px solid #08060c;
      width: 23px;
    }

    .arm {
      top: 108px;
      height: 183px;
    }

    .arm.a {
      left: 40px;
      transform: rotate(9deg);
    }

    .arm.b {
      right: 36px;
      transform: rotate(-12deg);
    }

    .leg {
      top: 211px;
      height: 174px;
      width: 27px;
    }

    .leg.a {
      left: 76px;
      transform: rotate(4deg);
    }

    .leg.b {
      left: 125px;
      transform: rotate(-4deg);
    }

    .particle {
      position: absolute;
      width: 7px;
      height: 7px;
      background: #bd70ff;
      box-shadow: 0 0 12px #a542ee;
      animation: float 4s infinite;
    }

    .p1 {
      top: 17%;
      left: 17%;
    }

    .p2 {
      top: 36%;
      right: 7%;
      background: var(--red);
    }

    .p3 {
      bottom: 23%;
      left: 9%;
    }

    .p4 {
      bottom: 16%;
      right: 20%;
    }

    .scene-label {
      position: absolute;
      right: 5px;
      bottom: 5px;
      font: 10px 'Space Mono', monospace;
      letter-spacing: 2px;
      color: #9e7db6;
    }

    .strip {
      margin: 10px 32px 0;
      padding: 23px 0;
      display: flex;
      justify-content: space-between;
      border-block: 1px solid #ffffff19;
      font: 11px 'Space Mono', monospace;
      letter-spacing: 2px;
      color: #b9a9c9;
    }

    .strip span b {
      color: var(--red);
      margin-right: 10px;
    }

    /* Área de conexão */

    .connect {
      padding: 95px 32px 80px;
      display: grid;
      grid-template-columns: .85fr 1.15fr;
      gap: 75px;
    }

    h2 {
      font-size: 44px;
      line-height: 1.1;
      letter-spacing: -2px;
      margin: 20px 0;
    }

    .intro p {
      color: var(--muted);
      line-height: 1.8;
      max-width: 350px;
    }

    .connection {
      background: #1a1024;
      border: 1px solid #543366;
      padding: 28px;
    }

    .tabs {
      display: flex;
      border-bottom: 1px solid #ffffff17;
      margin-bottom: 25px;
    }

    .tab {
      flex: 1;
      padding: 0 0 17px;
      background: none;
      border: 0;
      color: #93829f;
      text-align: left;
      font-size: 15px;
    }

    .tab[aria-selected="true"] {
      color: var(--purple);
      border-bottom: 2px solid var(--purple);
    }

    .tag {
      font: 9px 'Space Mono', monospace;
      margin-left: 8px;
      border: 1px solid #8052a0;
      padding: 3px 6px;
    }

    .label {
      display: block;
      font: 10px 'Space Mono', monospace;
      letter-spacing: 1px;
      color: var(--muted);
      margin-bottom: 10px;
    }

    .address {
      display: flex;
      align-items: center;
      gap: 14px;
      background: #110a18;
      border: 1px solid #382444;
      padding: 15px;
    }

    .address code {
      font-size: clamp(13px, 1.5vw, 18px);
      flex: 1;
      word-break: break-all;
    }

    .copy {
      border: 0;
      background: #30203f;
      color: #dbc1f0;
      padding: 10px;
      font-size: 11px;
    }

    .copy:hover {
      background: #513165;
    }

    .port {
      padding: 16px 0 0;
      color: var(--muted);
      font-size: 13px;
    }

    .port strong {
      color: #fff;
      font-family: monospace;
      font-size: 17px;
      margin-left: 12px;
    }

    .steps {
      padding-left: 22px;
      margin: 23px 0 0;
      color: #c2b5cf;
      font-size: 13px;
      line-height: 1.9;
    }

    .steps li {
      padding-left: 5px;
      margin-top: 6px;
    }

    .steps li::marker {
      color: var(--purple);
    }

    .note {
      font-size: 11px;
      color: #95849f;
      margin: 18px 0 0;
      line-height: 1.7;
    }

    .about {
      margin: 0 32px 75px;
      border-left: 3px solid var(--red);
      padding: 15px 28px;
      background: linear-gradient(90deg, #51162744, transparent);
      display: flex;
      justify-content: space-between;
      gap: 30px;
      align-items: center;
    }

    .about h3 {
      font-size: 22px;
      margin: 0 0 9px;
    }

    .about p {
      font-size: 14px;
      line-height: 1.7;
      color: var(--muted);
      max-width: 690px;
      margin: 0;
    }

    .about .pixel {
      font-size: 48px;
      color: var(--red);
    }

    footer {
      border-top: 1px solid #ffffff16;
      padding: 28px 32px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      color: #83748e;
      font-size: 11px;
    }

    .foot-brand {
      color: #c5b1d6;
      font-weight: 700;
      letter-spacing: 3px;
    }

    .toast {
      position: fixed;
      bottom: 25px;
      left: 50%;
      transform: translateX(-50%);
      padding: 14px 24px;
      background: #b575ff;
      color: #170c21;
      box-shadow: 0 4px 30px #0008;
      font-size: 13px;
      z-index: 10;
      max-width: 90%;
      text-align: center;
    }

    .toast:empty {
      display: none;
    }

    :focus-visible {
      outline: 2px solid #e1adff;
      outline-offset: 5px;
    }

    @keyframes float {
      50% {
        translate: 0 -12px;
      }
    }

    @media (prefers-reduced-motion: reduce) {
      * {
        animation: none !important;
        scroll-behavior: auto !important;
      }
    }

    /* Ajustes para celular */

    @media (max-width: 760px) {
      header {
        height: 80px;
        padding: 0 22px;
      }

      nav {
        gap: 17px;
      }

      nav .about-link {
        display: none;
      }

      .hero {
        grid-template-columns: 1fr;
        padding: 50px 24px 20px;
        overflow: hidden;
      }

      h1 {
        font-size: 60px;
      }

      .hero p {
        max-width: 100%;
      }

      .scene {
        height: 420px;
        margin-top: 25px;
      }

      .enderman {
        scale: .88;
      }

      .portal {
        height: 340px;
        width: 230px;
      }

      .strip {
        margin: 0 24px;
        font-size: 9px;
        letter-spacing: 0;
        gap: 10px;
      }

      .connect {
        grid-template-columns: 1fr;
        gap: 24px;
        padding: 65px 24px;
      }

      .intro p {
        max-width: 100%;
      }

      h2 {
        font-size: 39px;
      }

      .connection {
        padding: 20px;
      }

      .about {
        margin: 0 24px 45px;
        padding: 14px 20px;
      }

      .about .pixel {
        display: none;
      }

      footer {
        gap: 20px;
        padding: 25px 24px;
        align-items: flex-start;
      }

      footer span:last-child {
        max-width: 235px;
        text-align: right;
        line-height: 1.7;
      }
    }

    @media (max-width: 360px) {
      h1 {
        font-size: 50px;
      }

      nav .nav-play {
        padding: 10px;
      }

      .address {
        padding: 10px;
        gap: 5px;
      }
    }
  </style>
</head>

<body>
  <header>
    <a href="#" class="brand" aria-label="Acer início">
      <span class="mark">▧</span>
      ACER<span style="color: #ff435d">.</span>
    </a>

    <nav aria-label="Menu principal">
      <a class="about-link" href="#sobre">O servidor</a>
      <a href="#conectar">Como entrar</a>
      <a class="nav-play" href="#conectar">Bora jogar ↗</a>
    </nav>
  </header>

  <main>
    <section class="hero">
      <div>
        <div class="eyebrow">Servidor Minecraft • Acer</div>

        <h1>
          Entre em<br>
          outra <em>dimensão.</em>
        </h1>

        <p>
          Seu próximo mundo começa aqui. Prepare sua picareta,
          chame os amigos e entre no universo do Acer.
        </p>

        <div class="buttons">
          <a href="#conectar" class="primary">
            Quero jogar <span>↗</span>
          </a>

          <button class="secondary" data-copy="acerSrV.aternos.me">
            Copiar IP <span>▣</span>
          </button>
        </div>

        <div class="micro">
          JAVA EDITION + ACESSO BEDROCK
        </div>
      </div>

      <div
        class="scene"
        role="img"
        aria-label="Enderman em arte de blocos, com olhos roxos brilhantes diante de um portal roxo"
      >
        <div class="portal"></div>

        <div class="enderman">
          <div class="head">
            <i class="eye left"></i>
            <i class="eye right"></i>
          </div>

          <div class="torso"></div>
          <div class="arm a"></div>
          <div class="arm b"></div>
          <div class="leg a"></div>
          <div class="leg b"></div>
        </div>

        <i class="particle p1"></i>
        <i class="particle p2"></i>
        <i class="particle p3"></i>
        <i class="particle p4"></i>

        <span class="scene-label">
          NÃO OLHE DIRETO NOS OLHOS.
        </span>
      </div>
    </section>

    <div class="strip">
      <span><b>01 /</b> UM NOVO MUNDO</span>
      <span><b>02 /</b> SUA PRÓXIMA HISTÓRIA</span>
      <span><b>03 /</b> ACER MINECRAFT</span>
    </div>

    <section class="connect" id="conectar">
      <div class="intro">
        <div class="eyebrow">Seu ponto de partida</div>

        <h2>
          O próximo bloco<br>
          é com você.
        </h2>

        <p>
          Escolha sua edição, adicione o servidor e venha jogar.
          O endereço está aqui, pronto para copiar.
        </p>
      </div>

      <div class="connection">
        <div
          class="tabs"
          role="tablist"
          aria-label="Edição do Minecraft"
        >
          <button
            id="java-tab"
            class="tab"
            role="tab"
            aria-selected="true"
            aria-controls="instructions"
            data-edition="java"
          >
            Java <span class="tag">PC</span>
          </button>

          <button
            id="bedrock-tab"
            class="tab"
            role="tab"
            aria-selected="false"
            aria-controls="instructions"
            data-edition="bedrock"
            tabindex="-1"
          >
            Bedrock
          </button>
        </div>

        <div
          id="instructions"
          role="tabpanel"
          aria-labelledby="java-tab"
        >
          <span class="label">
            ENDEREÇO DO SERVIDOR
          </span>

          <div class="address">
            <code>acerSrV.aternos.me</code>

            <button
              class="copy"
              data-copy="acerSrV.aternos.me"
              aria-label="Copiar endereço do servidor"
            >
              Copiar ▣
            </button>
          </div>

          <div id="port" class="port" hidden>
            Porta Bedrock
            <strong>55598</strong>

            <button
              class="copy"
              data-copy="55598"
              aria-label="Copiar porta Bedrock"
            >
              Copiar
            </button>
          </div>

          <ol class="steps" id="steps">
            <li>
              Abra o Minecraft Java e vá em
              <strong>Multijogador</strong>.
            </li>
            <li>
              Clique em <strong>Adicionar servidor</strong>
              e dê o nome Acer.
            </li>
            <li>
              Cole o endereço, salve e conecte-se ao servidor.
            </li>
          </ol>

          <p class="note">
            O servidor precisa estar ligado para você entrar.
            Se não conectar, confirme com a administração se ele
            está disponível e qual versão usar.
          </p>
        </div>
      </div>
    </section>

    <section id="sobre" class="about">
      <div>
        <h3>Acer. Uma aventura com a sua marca.</h3>

        <p>
          Um servidor de Minecraft Java, com dados de acesso para
          Bedrock. Entre no clima do Enderman: roxo, vermelho e
          um mundo de possibilidades para a sua próxima sessão
          de Minecraft.
        </p>
      </div>

      <span class="pixel" aria-hidden="true">✦</span>
    </section>
  </main>

  <footer>
    <span class="foot-brand">ACER.</span>

    <span>
      Feito para quem vive Minecraft.<br>
      Site independente, sem afiliação à Mojang ou Microsoft.
    </span>
  </footer>

  <div class="toast" role="status" aria-live="polite"></div>

  <script>
    let timer;

    const toast = document.querySelector('.toast');

    // Copiar endereço ou porta.
    document.querySelectorAll('[data-copy]').forEach(button => {
      button.addEventListener('click', async () => {
        try {
          await navigator.clipboard.writeText(button.dataset.copy);
          toast.textContent = 'Copiado: ' + button.dataset.copy;
        } catch {
          toast.textContent = 'Copie manualmente: ' + button.dataset.copy;
        }

        clearTimeout(timer);

        timer = setTimeout(() => {
          toast.textContent = '';
        }, 4000);
      });
    });

    // Alternar instruções entre Java e Bedrock.
    const tabs = [...document.querySelectorAll('[data-edition]')];

    function select(tab) {
      const bedrock = tab.dataset.edition === 'bedrock';

      tabs.forEach(item => {
        item.setAttribute('aria-selected', String(item === tab));
        item.tabIndex = item === tab ? 0 : -1;
      });

      document.querySelector('#instructions').setAttribute(
        'aria-labelledby',
        tab.id
      );

      document.querySelector('#port').hidden = !bedrock;

      document.querySelector('#steps').innerHTML = bedrock
        ? `
          <li>
            Abra o Minecraft Bedrock e vá em
            <strong>Jogar → Servidores</strong>.
          </li>
          <li>
            Em <strong>Adicionar servidor</strong>,
            use o nome Acer e o endereço acima.
          </li>
          <li>
            Informe a porta <strong>55598</strong>,
            salve e entre.
          </li>
        `
        : `
          <li>
            Abra o Minecraft Java e vá em
            <strong>Multijogador</strong>.
          </li>
          <li>
            Clique em <strong>Adicionar servidor</strong>
            e dê o nome Acer.
          </li>
          <li>
            Cole o endereço, salve e conecte-se ao servidor.
          </li>
        `;
    }

    tabs.forEach((tab, index) => {
      tab.addEventListener('click', () => {
        select(tab);
      });

      // Navegação das abas pelo teclado.
      tab.addEventListener('keydown', event => {
        const keys = ['ArrowLeft', 'ArrowRight', 'Home', 'End'];

        if (!keys.includes(event.key)) {
          return;
        }

        event.preventDefault();

        const next =
          event.key === 'Home'
            ? tabs[0]
            : event.key === 'End'
              ? tabs[1]
              : tabs[1 - index];

        select(next);
        next.focus();
      });
    });
  </script>
</body>
</html>
```
