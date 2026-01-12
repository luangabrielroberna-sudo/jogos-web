# jogos-web
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Jogo Aleatório</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #1e1e2f, #3a3a6a);
      color: white;
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
    }

    .game {
      background: rgba(0,0,0,0.5);
      padding: 30px;
      border-radius: 15px;
      text-align: center;
      width: 320px;
      box-shadow: 0 0 20px rgba(0,0,0,0.5);
    }

    button {
      margin-top: 20px;
      padding: 12px 20px;
      border: none;
      border-radius: 10px;
      background: #00ffcc;
      color: #000;
      font-size: 16px;
      cursor: pointer;
    }

    button:hover {
      background: #00ccaa;
    }

    .challenge {
      font-size: 18px;
      margin-top: 15px;
    }
  </style>
</head>
<body>

  <div class="game">
    <h1>🎲 Desafio Aleatório</h1>
    <p>Clique no botão para receber um desafio!</p>
    <div class="challenge" id="challenge">---</div>
    <button onclick="novoDesafio()">Novo Desafio</button>
  </div>

  <script>
    const desafios = [
      "Clique no botão 10 vezes seguidas!",
      "Conte até 20 sem errar!",
      "Pense em um número de 1 a 10!",
      "Faça 5 flexões 😄",
      "Levante e sente 10 vezes!",
      "Escolha um número da sorte!",
      "Espere 5 segundos sem piscar!",
      "Desafie um amigo agora!",
      "Gire a cadeira 3 vezes!",
      "Bata palmas 7 vezes!"
    ];

    function novoDesafio() {
      const sorteio = Math.floor(Math.random() * desafios.length);
      document.getElementById("challenge").innerText = desafios[sorteio];
    }
  </script>

</body>
</html>
