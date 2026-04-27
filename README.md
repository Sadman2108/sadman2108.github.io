<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Sadman Portfolio</title>

<style>
body {
  margin: 0;
  font-family: Arial;
  background: linear-gradient(to right, #2b1055, #1a1a40);
  color: white;
  text-align: center;
}

.container {
  padding: 20px;
}

.profile-emoji {
  width: 130px;
  height: 130px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 55px;
  margin: 20px auto;
  background: #111;
  border: 3px solid #8a2be2;
  box-shadow: 0 0 15px #8a2be2;
  animation: glow s infinite alternate, float 3s ease-in-out infinite;
}

@keyframes glow {
  from { box-shadow: 0 0 10px #8a2be2; }
  to { box-shadow: 0 0 25px #ff00ff; }
}

@keyframes float {
  0% { transform: translateY(0px); }
  50% { transform: translateY(-10px); }
  100% { transform: translateY(0px); }
}

.skill {
  text-align: left;
  margin: 15px 20px;
}

.bar {
  background: #444;
  border-radius: 10px;
  overflow: hidden;
}

.fill {
  height: 15px;
  width: 0;
  transition: width 2s ease;
}

.percent {
  color: #00ff88;
  font-size: 14px;
}
</style>

</head>
<body>

<div class="container">

<div class="profile-emoji">☠️</div>

<h1>Sadman</h1>
<div>WEB & APP DEVELOPER</div>

<p>
Hey there! I am Sadman, a skilled app and web developer.
</p>

<div class="skill">JAVA
<div class="bar"><div class="fill" data-width="20%" style="background:red;"></div></div>
<div class="percent">20%</div>
</div>

<div class="skill">JAVASCRIPT
<div class="bar"><div class="fill" data-width="30%" style="background:lime;"></div></div>
<div class="percent">30%</div>
</div>

<div class="skill">PYTHON
<div class="bar"><div class="fill" data-width="35%" style="background:pink;"></div></div>
<div class="percent">35%</div>
</div>

</div>

<script>
const fills = document.querySelectorAll(".fill");

fills.forEach(fill => {
  setTimeout(() => {
    fill.style.width = fill.getAttribute("data-width");
  }, 500);
});
</script>

</body>
</html>
