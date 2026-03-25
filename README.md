<!DOCTYPE html>
<html>
<head>
  <title>Happy Birthday Sara 💖</title>

  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: linear-gradient(to bottom right, #ffc0cb, #ffe4e1);
      font-family: 'Arial', sans-serif;
      overflow: hidden;
    }

    .container {
      text-align: center;
      color: white;
    }

    h1 {
      font-size: 50px;
      animation: float 3s infinite ease-in-out;
    }

    p {
      font-size: 22px;
      opacity: 0;
      animation: fadeText 2s forwards;
    }

    .msg1 { animation-delay: 2s; }
    .msg2 { animation-delay: 4s; }
    .msg3 { animation-delay: 6s; }

    @keyframes fadeText {
      to {opacity: 1;}
    }

    @keyframes float {
      0% {transform: translateY(0);}
      50% {transform: translateY(-10px);}
      100% {transform: translateY(0);}
    }

    .heart {
      position: absolute;
      color: white;
      font-size: 20px;
      animation: fall linear infinite;
    }

    @keyframes fall {
      0% {transform: translateY(-10vh);}
      100% {transform: translateY(110vh);}
    }

    button {
      margin-top: 20px;
      padding: 10px 20px;
      border: none;
      border-radius: 20px;
      background: white;
      color: pink;
      font-size: 16px;
      cursor: pointer;
    }
  </style>
</head>

<body>

<!-- MUSIC (user clicks to play) -->
<audio id="music" loop>
  <source src="https://www2.cs.uic.edu/~i101/SoundFiles/HappyBirthday.mid" type="audio/midi">
</audio>

<div class="container">
  <h1>Happy Birthday Sara 🎂💖</h1>

  <p class="msg1">You are literally the best person ever 🥹</p>
  <p class="msg2">Life is so much better with you in it ✨</p>
  <p class="msg3">I hope today is as amazing as you are 💕</p>

  <button onclick="playMusic()">Tap for a surprise 🎶</button>
</div>

<script>
  function playMusic() {
    document.getElementById("music").play();
  }

  // floating hearts
  setInterval(() => {
    let heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML = "💖";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.animationDuration = (Math.random() * 3 + 2) + "s";
    document.body.appendChild(heart);

    setTimeout(() => {
      heart.remove();
    }, 5000);
  }, 300);
</script>

</body>
</html>
