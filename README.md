<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>I LOVE YOU KURUTTE</title>
  <style>
    body {
      margin: 0;
      overflow: hidden;
      background: linear-gradient(to bottom, #ffdee9, #b5fffc);
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      font-family: 'Segoe UI', sans-serif;
    }

    h1 {
      font-size: 3rem;
      color: #fff;
      text-shadow: 0 0 10px #ff0080, 0 0 20px #ff0080;
      animation: pulse 2s ease-in-out infinite;
      z-index: 1;
    }

    @keyframes pulse {
      0%, 100% {
        transform: scale(1);
      }
      50% {
        transform: scale(1.1);
      }
    }

    .heart {
      position: absolute;
      top: -50px;
      font-size: 2rem;
      animation: fall linear infinite;
      color: red;
      opacity: 0.8;
      z-index: 0;
    }

    @keyframes fall {
      to {
        transform: translateY(110vh);
        opacity: 1;
      }
    }
  </style>
</head>
<body>
  <h1>I LOVE YOU KURUTTE 💖</h1>

  <script>
    const hearts = ["❤️","💖","💕","💘"];
    for (let i = 0; i < 50; i++) {
      const heart = document.createElement("div");
      heart.className = "heart";
      heart.innerText = hearts[Math.floor(Math.random() * hearts.length)];
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.animationDuration = (2 + Math.random() * 3) + "s";
      heart.style.fontSize = (1 + Math.random() * 2) + "rem";
      document.body.appendChild(heart);
    }
  </script>
</body>
</html>
