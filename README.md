<!DOCTYPE html>
<html lang="pt">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Bot Aviator Pro</title>
  <style>
    body {
      margin: 0;
      font-family: 'Arial', sans-serif;
      background: linear-gradient(to bottom right, #0f0c29, #302b63, #24243e);
      color: white;
      text-align: center;
      padding: 30px;
    }
    .container {
      max-width: 500px;
      margin: auto;
      padding: 30px;
      background: rgba(255, 255, 255, 0.05);
      border-radius: 20px;
      box-shadow: 0 0 15px rgba(0,0,0,0.5);
      animation: fadeIn 1.5s ease;
    }
    h1 {
      font-size: 2rem;
      margin-bottom: 20px;
    }
    button {
      padding: 15px 30px;
      font-size: 16px;
      margin: 10px;
      border: none;
      border-radius: 10px;
      background: #00c6ff;
      color: white;
      cursor: pointer;
      transition: background 0.3s;
    }
    button:hover {
      background: #0072ff;
    }
    #page2, #page3, #downloadBtn {
      display: none;
    }
    @keyframes fadeIn {
      from {opacity: 0; transform: translateY(20px);}
      to {opacity: 1; transform: translateY(0);}
    }
  </style>
</head>
<body>
  <div class="container" id="page1">
    <h1>Bem-vindo ao Bot Aviator Pro</h1>
    <p>Para continuar, entre no nosso canal oficial:</p>
    <button onclick="entrarNoCanal()">Entrar no Canal</button>
  </div>

  <div class="container" id="page2">
    <h1>Passo 2: Registra-te</h1>
    <p>Clica no botão abaixo para te registrar e usar o Bot Aviator</p>
    <a href="https://media1.placard.co.mz/redirect.aspx?pid=2204&bid=1690" target="_blank">
      <button>Registar Agora</button>
    </a>
    <p>Depois de registrar, baixe o APK:</p>
    <button onclick="irParaDownload()">Baixar Bot APK</button>
  </div>

  <div class="container" id="page3">
    <h1>Último Passo: Compartilha para Liberar o Download</h1>
    <p>Compartilhe a mensagem no WhatsApp para desbloquear o botão de download:</p>
    <button onclick="compartilharWhatsapp()">Compartilhar no WhatsApp</button>
    <br><br>
    <button id="downloadBtn" onclick="window.location.href='https://www.mediafire.com/file/vy75wve56yrr6sl/gen_signed.apk/file'">Começar o Download</button>
  </div>

  <script>
    function entrarNoCanal() {
      window.open("https://whatsapp.com/channel/0029Vb5qcXa9mrGjHiNmku21", "_blank");
      setTimeout(() => {
        document.getElementById("page1").style.display = "none";
        document.getElementById("page2").style.display = "block";
      }, 1500);
    }

    function irParaDownload() {
      document.getElementById("page2").style.display = "none";
      document.getElementById("page3").style.display = "block";
    }

    function compartilharWhatsapp() {
      const mensagem = `🎯 QUERES GANHAR MAIS NO AVIATOR?%0AJá está disponível gratuitamente o Bot Aviator com sinais em tempo real que te ajudam a prever os melhores momentos para apostar!%0A%0A🔗 CLICA AQUI:%0A%0A✅ Fácil de usar%0A✅ Grátis%0A✅ Resultados rápidos%0A%0ATesta agora e vê a diferença! 🚀💸%0A%0APara acessar:`;
      const url = `https://api.whatsapp.com/send?text=${mensagem}`;
      window.open(url, "_blank");
      setTimeout(() => {
        document.getElementById("downloadBtn").style.display = "inline-block";
      }, 2000);
    }
  </script>
</body>
</html>

