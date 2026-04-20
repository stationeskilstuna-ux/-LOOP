# -LOOP
$LOOP — You buy. You hold. You loop. Repeat forever.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$LOOP — Everything is a Loop</title>

  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      overflow-x: hidden;
      background: black;
      color: white;
      text-align: center;
    }

    /* Animated background */
    body::before {
      content: "";
      position: fixed;
      width: 300%;
      height: 300%;
      background: linear-gradient(270deg, #ff00cc, #3333ff, #00ffcc);
      animation: bgLoop 10s infinite linear;
      z-index: -1;
    }

    @keyframes bgLoop {
      0% { transform: translate(0,0); }
      50% { transform: translate(-50%, -50%); }
      100% { transform: translate(0,0); }
    }

    header {
      padding: 60px 20px;
    }

    /* Glitch effect */
    h1 {
      font-size: 4rem;
      position: relative;
      animation: glitch 1s infinite;
    }

    @keyframes glitch {
      0% { text-shadow: 2px 2px #ff00cc, -2px -2px #00ffcc; }
      50% { text-shadow: -2px 2px #ff00cc, 2px -2px #00ffcc; }
      100% { text-shadow: 2px -2px #ff00cc, -2px 2px #00ffcc; }
    }

    .btn {
      margin-top: 20px;
      padding: 15px 35px;
      background: white;
      color: black;
      border-radius: 30px;
      font-weight: bold;
      text-decoration: none;
      display: inline-block;
      transition: 0.3s;
    }

    .btn:hover {
      background: black;
      color: white;
      border: 2px solid white;
    }

    /* Spinner */
    .loop-circle {
      margin: 40px auto;
      width: 150px;
      height: 150px;
      border: 8px solid white;
      border-top: 8px solid transparent;
      border-radius: 50%;
      animation: spin 1.5s linear infinite;
    }

    @keyframes spin {
      to { transform: rotate(360deg); }
    }

    /* Fake price ticker */
    .ticker {
      margin-top: 30px;
      font-size: 1.5rem;
      font-weight: bold;
    }

    /* Scrolling text */
    .marquee {
      position: fixed;
      bottom: 0;
      width: 100%;
      white-space: nowrap;
      overflow: hidden;
      background: rgba(0,0,0,0.7);
      padding: 10px 0;
      font-weight: bold;
    }

    .marquee span {
      display: inline-block;
      padding-left: 100%;
      animation: scroll 10s linear infinite;
    }

    @keyframes scroll {
      0% { transform: translateX(0); }
      100% { transform: translateX(-100%); }
    }

    section {
      margin-top: 50px;
      padding: 0 20px;
    }

    footer {
      margin-top: 80px;
      padding: 20px;
      opacity: 0.7;
    }
  </style>
</head>

<body>

  <header>
    <h1>$LOOP</h1>
    <p>Everything loops. You can't escape.</p>
    <a href="#" class="btn" onclick="location.reload()">ENTER LOOP</a>
    <br>
    <a href="#" class="btn">BUY $LOOP</a>
  </header>

  <div class="loop-circle"></div>

  <div class="ticker" id="price">$LOOP Price: $0.0001</div>

  <section>
    <h2>What is $LOOP?</h2>
    <p>It goes up. It goes down. It goes up again. Forever.</p>
  </section>

  <section>
    <h2>Tokenomics</h2>
    <p>100% vibes — 0% logic — infinite loop</p>
  </section>

  <section>
    <h2>Roadmap</h2>
    <p>Launch → Pump → Dump → Repeat 🔁</p>
  </section>

  <div class="marquee">
    <span>🔁 BUY LOOP 🔁 HOLD LOOP 🔁 BECOME LOOP 🔁 REPEAT 🔁</span>
  </div>

  <footer>
    <p>© 2026 $LOOP — There is no exit.</p>
  </footer>

  <script>
    // Fake price movement
    let price = 0.0001;

    function updatePrice() {
      let change = (Math.random() - 0.5) * 0.00005;
      price += change;

      if (price < 0.00001) price = 0.00001;

      document.getElementById("price").innerText =
        "$LOOP Price: $" + price.toFixed(6);
    }

    setInterval(updatePrice, 1000);
  </script>

</body>
</html>
