<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>SOLGEN | Green Mining Simulator</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
  <style>
    body {
      background-color: #f4f4f4;
      font-family: 'Segoe UI', sans-serif;
      text-align: center;
      padding-top: 50px;
    }
    .counter {
      font-size: 2em;
      margin: 20px;
    }
    .mining-box {
      background: #fff;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 5px 20px rgba(0,0,0,0.1);
    }
    .btn-mine {
      background-color: #28a745;
      color: #fff;
      font-weight: bold;
      padding: 15px 30px;
      border-radius: 10px;
    }
  </style>
</head>
<body>

  <div class="container">
    <h1>Welcome to <strong>SOLGEN</strong></h1>
    <p>The Future of Green, Simulated Mining!</p>

    <div class="mining-box mt-5">
      <h3>Your Virtual Mining Rig</h3>
      <div class="counter" id="earnings">0.0000 SOL</div>
      <button class="btn btn-mine" onclick="mine()">Start Mining</button>
    </div>
  </div>

  <script>
    let earnings = 0;
    function mine() {
      let earned = (Math.random() * 0.005).toFixed(4);
      earnings += parseFloat(earned);
      document.getElementById('earnings').innerText = earnings.toFixed(4) + ' SOL';
    }
  </script>

</body>
</html>
