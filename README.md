<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Amine Dev 👾</title>

<style>
body {
  margin: 0;
  font-family: 'Segoe UI', sans-serif;
  background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
  color: white;
  text-align: center;
  overflow: hidden;
}

/* خلفية نجوم */
.stars {
  position: fixed;
  width: 100%;
  height: 100%;
  background: transparent;
}

.stars::after {
  content: "";
  position: absolute;
  width: 2px;
  height: 2px;
  background: white;
  box-shadow: 100px 200px white, 300px 400px white, 500px 100px white,
              700px 300px white, 900px 200px white;
  animation: moveStars 10s linear infinite;
}

@keyframes moveStars {
  from {transform: translateY(0);}
  to {transform: translateY(-1000px);}
}

.container {
  margin-top: 120px;
  z-index: 2;
  position: relative;
}

h1 {
  font-size: 50px;
  color: #00f7ff;
  text-shadow: 0 0 10px #00f7ff, 0 0 40px #00f7ff;
}

#typing {
  font-size: 24px;
  color: #ffcc00;
  margin-top: 20px;
}

.card {
  margin-top: 30px;
  padding: 20px;
  border-radius: 20px;
  background: rgba(255,255,255,0.05);
  box-shadow: 0 0 20px rgba(0,255,255,0.3);
  display: inline-block;
}

button {
  margin-top: 20px;
  padding: 10px 25px;
  border: none;
  border-radius: 10px;
  background: #ff00c8;
  color: white;
  cursor: pointer;
  transition: 0.3s;
}

button:hover {
  background: #00f7ff;
  transform: scale(1.1);
}

.progress {
  width: 300px;
  height: 10px;
  background: #222;
  border-radius: 10px;
  margin: 10px auto;
}

.progress-bar {
  height: 100%;
  width: 0;
  background: #00f7ff;
  border-radius: 10px;
}

</style>
</head>

<body>

<div class="stars"></div>

<div class="container">
  <h1>👾 Amine.dev</h1>

  <h2 id="typing"></h2>

  <div class="card">
    <p>💻 Learning Web Dev</p>
    <p>🎮 Gamer | Anime Lover</p>

    <h3>🚀 Skills Progress</h3>

    <p>HTML</p>
    <div class="progress"><div class="progress-bar" id="html"></div></div>

    <p>CSS</p>
    <div class="progress"><div class="progress-bar" id="css"></div></div>

    <p>JavaScript</p>
    <div class="progress"><div class="progress-bar" id="js"></div></div>

    <button onclick="levelUp()">Level Up 🎯</button>
    <p id="msg"></p>
  </div>
</div>

<script>
const text = "🚀 I’m learning Web Development...";
let i = 0;

function typingEffect() {
  if (i < text.length) {
    document.getElementById("typing").innerHTML += text.charAt(i);
    i++;
    setTimeout(typingEffect, 50);
  }
}
typingEffect();

// Progress animation
function animateBar(id, value) {
  let bar = document.getElementById(id);
  let width = 0;
  let interval = setInterval(() => {
    if (width >= value) {
      clearInterval(interval);
    } else {
      width++;
      bar.style.width = width + "%";
    }
  }, 20);
}

animateBar("html", 80);
animateBar("css", 70);
animateBar("js", 50);

// Button
function levelUp() {
  document.getElementById("msg").innerHTML =
    "🔥 +10 XP | You are leveling up as a DEV!";
}
</script>

</body>
</html>

<!--
**AkselAM/AkselAM** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
