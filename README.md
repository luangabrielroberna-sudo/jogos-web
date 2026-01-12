# jogos-web
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>PlayZone - Jogos Online</title>
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; font-family: Arial, sans-serif; }
    body { background: #f4f6fb; }
    header {
      background: #1e88e5;
      color: white;
      padding: 15px 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    header h1 { font-size: 22px; }
    input {
      padding: 8px;
      border-radius: 5px;
      border: none;
      width: 200px;
    }
    main {
      padding: 20px;
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
      gap: 20px;
    }
    .game {
      background: white;
      border-radius: 10px;
      padding: 10px;
      text-align: center;
      cursor: pointer;
      transition: transform 0.2s;
    }
    .game:hover { transform: scale(1.05); }
    .game img {
      width: 100%;
      border-radius: 10px;
    }
    .game p { margin-top: 8px; font-weight: bold; }
    footer {
      text-align: center;
      padding: 15px;
      background: #e0e0e0;
      margin-top: 20px;
    }
  </style>
</head>
<body>

<header>
  <h1>🎮 PlayZone</h1>
  <input type="text" id="search" placeholder="Buscar jogos..." />
</header>

<main id="games">
  <div class="game" onclick="openGame('https://example.com')">
    <img src="https://via.placeholder.com/300x200" />
    <p>Jogo 1</p>
  </div>
  <div class="game" onclick="openGame('https://example.com')">
    <img src="https://via.placeholder.com/300x200" />
    <p>Jogo 2</p>
  </div>
  <div class="game" onclick="openGame('https://example.com')">
    <img src="https://via.placeholder.com/300x200" />
    <p>Jogo 3</p>
  </div>
</main>

<footer>
  <p>© 2026 PlayZone - Jogos Online</p>
</footer>

<script>
  const search = document.getElementById('search');
  search.addEventListener('keyup', () => {
    const term = search.value.toLowerCase();
    document.querySelectorAll('.game').forEach(game => {
      const name = game.innerText.toLowerCase();
      game.style.display = name.includes(term) ? 'block' : 'none';
    });
  });

  function openGame(url) {
    window.open(url, '_blank');
  }
</script>

</body>
</html>
