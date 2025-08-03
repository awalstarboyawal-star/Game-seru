# Game-seru
Game yang sangat menghibur saat bosan
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Tebak Angka - Cahyadi Games</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Tebak Angka</h1>
  <div class="game-box">
    <p>Tebak angka dari 1 sampai 10</p>
    <input type="number" id="guess" placeholder="Masukkan tebakan" min="1" max="10">
    <button onclick="checkGuess()">Tebak!</button>
    <div class="message" id="message"></div>
  </div>
  <div class="footer">Dikembangkan oleh Cahyadi Games</div>

  <script src="script.js"></script>
</body>
</html>
