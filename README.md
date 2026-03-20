<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Para yuyu 💜</title>

  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: linear-gradient(180deg, #6a0dad, #2e003e);
      color: white;
      text-align: center;
    }

    h1 {
      margin-top: 80px;
      font-size: 24px;
    }

    button {
      margin-top: 30px;
      padding: 14px 24px;
      font-size: 18px;
      border: none;
      border-radius: 20px;
      background: #b266ff;
      color: white;
      cursor: pointer;
    }

    #conteudo {
      display: none;
      margin: 20px;
      animation: aparecer 1.5s ease;
    }

    @keyframes aparecer {
      from {opacity: 0;}
      to {opacity: 1;}
    }

    .galeria img {
      width: 85%;
      max-width: 280px;
      margin: 10px;
      border-radius: 15px;
    }

    .heart {
      position: fixed;
      bottom: -20px;
      font-size: 18px;
      animation: subir 6s linear infinite;
      color: #d9a3ff;
    }

    @keyframes subir {
      0% {transform: translateY(0); opacity: 1;}
      100% {transform: translateY(-100vh); opacity: 0;}
    }

    iframe {
      margin-top: 20px;
      border-radius: 12px;
    }
  </style>
</head>

<body>

  <h1>Abra seu presente 💜</h1>

  <button onclick="abrir()">Abrir</button>

  <div id="conteudo">
    <p>
      Oi gato, fiz esse presentinho pra tentar aquecer um pouquinho mais seu coração 💜 <br><br>
      Hoje é seu dia, mas quem fica feliz somos nós… por ter seu carinho, por ter seu sorriso, 
      seu carisma, seu dom em deixar tudo mais leve quando está por perto 💜<br><br>
      Feliz aniversário, yuyu 💜
    </p>

    <div class="galeria">
      <img src="foto1.jpg">
      <img src="foto2.jpg">
      <img src="foto3.jpg">
      <img src="foto4.jpg">
    </div>

    <!-- Música Sobre Nós -->
    <iframe style="border-radius:12px" 
    src="https://open.spotify.com/embed/track/0VjIjW4GlUZAMYd2vXMi3b?utm_source=generator" 
    width="300" height="80" frameBorder="0" allowfullscreen="" 
    allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture">
    </iframe>

  </div>

  <script>
    function abrir() {
      document.getElementById("conteudo").style.display = "block";
      document.querySelector("button").style.display = "none";
    }

    function criarCoracao() {
      const heart = document.createElement("div");
      heart.classList.add("heart");
      heart.innerHTML = "💜";
      heart.style.left = Math.random() * 100 + "vw";
      document.body.appendChild(heart);

      setTimeout(() => heart.remove(), 6000);
    }

    setInterval(criarCoracao, 400);
  </script>

</body>
</html>
