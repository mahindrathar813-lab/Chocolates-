<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy Chocolate Day 💖</title>
<link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Poppins:wght@300;500&display=swap" rel="stylesheet">

<style>
body {
  margin: 0;
  padding: 0;
  font-family: 'Poppins', sans-serif;
  background: linear-gradient(135deg, #ffd6e8, #ffc2d1);
  text-align: center;
  color: #5a2a41;
  overflow-x: hidden;
}

.card {
  margin: 60px auto;
  padding: 35px;
  max-width: 600px;
  background: #fff0f6;
  border-radius: 25px;
  box-shadow: 0 10px 30px rgba(0,0,0,0.1);
}

h1 {
  font-family: 'Pacifico', cursive;
  font-size: 40px;
  color: #d63384;
}

p {
  font-size: 18px;
  line-height: 1.6;
}

button {
  margin-top: 25px;
  padding: 14px 28px;
  font-size: 18px;
  color: white;
  background: #ff4d88;
  border: none;
  border-radius: 30px;
  cursor: pointer;
  transition: 0.3s;
}

button:hover {
  background: #e6005c;
  transform: scale(1.05);
}

.click-text {
  margin-top: 25px;
  font-weight: bold;
  font-size: 20px;
  color: #c9184a;
}

/* Surprise Page */
#surprisePage {
  display: none;
  padding: 30px 20px 80px;
}

#surprisePage h2 {
  font-family: 'Pacifico', cursive;
  font-size: 36px;
  color: #b30059;
}

#surprisePage img {
  width: 250px;
  margin: 20px 0;
  border-radius: 20px;
  box-shadow: 0 8px 20px rgba(0,0,0,0.15);
}

.footer {
  font-size: 22px;
  font-weight: bold;
  margin-top: 40px;
  color: #880e4f;
}

/* Chocolate Rain */
.choco {
  position: fixed;
  top: -50px;
  font-size: 24px;
  animation: fall linear infinite;
}

@keyframes fall {
  to {
    transform: translateY(110vh);
  }
}
</style>
</head>

<body>

<div class="card" id="homePage">
  <h1>Happy Chocolate Day My Bacha 🍫💗</h1>

  <p>
    You are sweeter than every chocolate in the world.  
    Every smile of yours melts my heart like warm cocoa.  
    Being with you makes my life soft, sweet, and full of love.
  </p>

  <p>
    I wish I could hand you chocolates right now…  
    but for now, I’m sending all my love wrapped in sweetness 💕
  </p>

  <div class="click-text">Click there for your chocolate 🍫👇</div>
  <button id="surpriseBtn">Click Here 💝</button>
</div>

<div id="surprisePage">
  <h2>Yayyy Apka Chocolate Idhar Hai 🍫💖</h2>

  <img src="cute.jpg" alt="Cute Teddy with Chocolate">

  <p style="font-size:20px; max-width:600px; margin:auto;">
    A chocolate for the cutest person in my life.  
    May your days always be this sweet and full of love.  
    You deserve all the happiness in the world, my jaan 💕
  </p>

  <div class="footer">
    Once again Happy Chocolate Day Bacha 💗  
    I love you sooo much my Shubhuuu 💞🍫
  </div>
</div>

<script>
document.getElementById("surpriseBtn").addEventListener("click", function() {
  document.getElementById("homePage").style.display = "none";
  document.getElementById("surprisePage").style.display = "block";
  startChocolateRain();
});

function startChocolateRain() {
  setInterval(() => {
    const choco = document.createElement("div");
    choco.classList.add("choco");
    choco.innerHTML = "🍫";
    choco.style.left = Math.random() * window.innerWidth + "px";
    choco.style.animationDuration = (Math.random() * 3 + 2) + "s";
    document.body.appendChild(choco);
    setTimeout(() => choco.remove(), 5000);
  }, 300);
}
</script>

</body>
</html>
