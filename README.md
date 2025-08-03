# Game-seru
Game yang sangat menghibur saat bosan
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Tebak Angka - Cahyadi Games</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      background: linear-gradient(135deg, #1e3c72, #2a5298);
      color: white;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
    }

    h1 {
      font-size: 2.5rem;
      margin-bottom: 10px;
    }

    .game-box {
      background-color: rgba(0, 0, 0, 0.3);
      padding: 30px;
      border-radius: 12px;
      text-align: center;
      box-shadow: 0 0 15px rgba(0,0,0,0.5);
    }

    input {
      padding: 10px;
      font-size: 16px;
      border-radius: 8px;
      border: none;
      margin-right: 10px;
      width: 120px;
      text-align: center;
    }

    button {
      padding: 10px 20px;
      font-size: 16px;
      border-radius: 8px;
      border: none;
      background-color: #28a745;
      color: white;
      cursor: pointer;
    }

    button:hover {
      background-color: #218838;
    }

    .message {
      margin-top: 20px;
      font-size: 18px;
    }

    .footer {
      position: absolute;
      bottom: 10px;
      font-size: 14px;
      color: #ccc;
    }
  </style>
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

  <script>
    const secretNumber = Math.floor(Math.random() * 10) + 1;
    let attempts = 0;

    function checkGuess() {
      const userGuess = parseInt(document.getElementById('guess').value);
      const messageEl = document.getElementById('message');
      attempts++;

      if (isNaN(userGuess)) {
        messageEl.innerHTML = '❌ Masukkan angka yang valid.';
        return;
      }

      if (userGuess === secretNumber) {
        messageEl.innerHTML = `🎉 Benar! Angka rahasia adalah ${secretNumber}. Kamu menebak dalam ${attempts} kali.`;
      } else if (userGuess < secretNumber) {
        messageEl.innerHTML = '📈 Terlalu rendah!';
      } else if (userGuess > secretNumber) {
        messageEl.innerHTML = '📉 Terlalu tinggi!';
      }
    }
  </script>
</body>
</html>
