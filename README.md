<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SLOOP</title>

<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;600&display=swap" rel="stylesheet">

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    background: radial-gradient(circle at top, #0a0a0f, #000);
    color: white;
    font-family: 'Orbitron', sans-serif;
    overflow-x: hidden;
}

/* Glow background */
body::before {
    content: "";
    position: fixed;
    width: 200%;
    height: 200%;
    background: radial-gradient(circle, rgba(255,0,255,0.08), transparent 60%);
    animation: pulse 6s infinite;
    z-index: -1;
}

@keyframes pulse {
    0% { transform: scale(1); opacity: 0.6; }
    50% { transform: scale(1.3); opacity: 0.2; }
    100% { transform: scale(1); opacity: 0.6; }
}

/* HERO */
.hero {
    height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    text-align: center;
}

.logo {
    font-size: 4rem;
    letter-spacing: 4px;
    color: #ff00ff;
    text-shadow: 0 0 20px #ff00ff;
}

.tagline {
    margin-top: 20px;
    font-size: 1.2rem;
    color: #aaa;
}

/* BUTTON */
.btn {
    margin-top: 40px;
    padding: 15px 40px;
    border: 1px solid #ff00ff;
    background: transparent;
    color: #ff00ff;
    cursor: pointer;
    text-transform: uppercase;
    letter-spacing: 2px;
    transition: 0.3s;
}

.btn:hover {
    background: #ff00ff;
    color: black;
    box-shadow: 0 0 20px #ff00ff;
}

/* SECTION */
.section {
    padding: 100px 20px;
    max-width: 900px;
    margin: auto;
    text-align: center;
}

.section h2 {
    margin-bottom: 20px;
    color: #ff00ff;
}

.section p {
    color: #ccc;
    line-height: 1.6;
}

/* FEED */
.feed {
    margin-top: 40px;
}

.feed-item {
    background: rgba(255,255,255,0.03);
    border: 1px solid rgba(255,0,255,0.2);
    padding: 20px;
    margin-bottom: 20px;
    transition: 0.3s;
}

.feed-item:hover {
    box-shadow: 0 0 15px #ff00ff50;
}

/* FOOTER */
.footer {
    padding: 40px;
    text-align: center;
    color: #666;
    font-size: 0.9rem;
}
</style>
</head>

<body>

<div class="hero">
    <div class="logo">SLOOP</div>
    <div class="tagline">Enter the loop. Stay because it feels right.</div>
    <button class="btn" onclick="enterLoop()">Enter</button>
</div>

<div class="section">
    <h2>No rush. No noise.</h2>
    <p>
        We are not launching anything.
        <br><br>
        We are not pumping anything.
        <br><br>
        We are building something people choose to stay in.
    </p>
</div>

<div class="section">
    <h2>The Loop</h2>
    <p>
        If you're here early, you're not lucky.
        <br>
        You're aligned.
    </p>

    <div class="feed">
        <div class="feed-item">“Nobody wants to look stupid being early.”</div>
        <div class="feed-item">“This is not hype. This is gravity.”</div>
        <div class="feed-item">“You don’t join. You get pulled in.”</div>
    </div>
</div>

<div class="footer">
    SLOOP © 2026 — No exit
</div>

<script>
function enterLoop() {
    alert("You're already in.");
}
</script>

</body>
</html>
