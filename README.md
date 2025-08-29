<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Jam Digital Kucing Pembalap</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      height: 100vh;
      background-image: url('Lucid_Origin_A_sleek_cat_with_bright_green_eyes_and_grey_fur_w_2.jpg');
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    #clock {
      font-family: 'Courier New', monospace;
      font-size: 80px;
      color: white;
      background-color: rgba(0, 0, 0, 0.5); /* Transparan gelap */
      padding: 20px 40px;
      border-radius: 20px;
      box-shadow: 0 0 20px black;
    }
  </style>
</head>
<body>
  <div id="clock">00:00:00</div>

  <script>
    function updateClock() {
      const now = new Date();
      const jam = now.getHours().toString().padStart(2, '0');
      const menit = now.getMinutes().toString().padStart(2, '0');
      const detik = now.getSeconds().toString().padStart(2, '0');
      document.getElementById('clock').textContent = `${jam}:${menit}:${detik}`;
    }

    setInterval(updateClock, 1000);
    updateClock(); // Tampilkan jam langsung saat halaman dimuat
  </script>
</body>
</html>
