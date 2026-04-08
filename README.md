<!DOCTYPE html>
<html lang="en">
<head> google-site-verification: googledb6139517451342c.html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>3 Patti Apps</title>

<style>
body {
  margin: 0;
  font-family: Arial;
  background: white;
  color: black;
}

/* HEADER */
header {
  text-align: center;
  padding: 15px;
  background: #f1f5f9;
  font-weight: bold;
}

/* GRID */
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 15px;
  padding: 15px;
}

/* APP ICON */
.app {
  text-align: center;
  cursor: pointer;
}

.app img {
  width: 70px;
  height: 70px;
  border-radius: 20px;
}

.app p {
  font-size: 12px;
  margin-top: 5px;
}

/* POPUP */
.popup {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0,0,0,0.6);
  display: none;
  justify-content: center;
  align-items: center;
}

.popup-content {
  background: white;
  padding: 20px;
  border-radius: 15px;
  width: 90%;
  max-width: 350px;
  text-align: center;
}

.popup-content img {
  width: 90px;
  border-radius: 20px;
}

.btn {
  display: block;
  margin-top: 10px;
  padding: 10px;
  background: green;
  color: white;
  text-decoration: none;
  border-radius: 10px;
}

.close {
  margin-top: 10px;
  color: red;
  cursor: pointer;
}
</style>

</head>
<body>

<header>📱 3 Patti Apps</header>

<div class="container">

  <!-- APP 1 -->
  <div class="app" onclick="openApp('3Patti Pearl','images/pearl.png','4.8','150K','https://3pattipearl.com/?from_gameid=4457555&channelCode=4348309')">
    <img src="images/pearl.png">
    <p>Pearl</p>
  </div>

  <!-- APP 2 -->
  <div class="app" onclick="openApp('3pattiWorld','images/world.png','4.7','120K','https://3pattiworldpkk.com?from_gameid=5825951&channelCode=100000')">
    <img src="images/world.png">
    <p>World</p>
  </div>

  <!-- APP 3 -->
  <div class="app" onclick="openApp('3pattiShowy','images/showy.png','4.9','180K','https://teenpattishowy.com/?from_gameid=5545690&channelCode=100000')">
    <img src="images/showy.png">
    <p>Showy</p>
  </div>

  <!-- APP 4 -->
  <div class="app" onclick="openApp('3pattiBlue','images/blue.png','4.8','140K','https://3pattibluevip.com?from_gameid=9191920&channelCode=9131811')">
    <img src="images/blue.png">
    <p>Blue</p>
  </div>

  <!-- APP 5 -->
  <div class="app" onclick="openApp('3pattiVages','images/vages.png','4.6','110K','https://ludovegas.com/?from_gameid=5076422&channelCode=4913682')">
    <img src="images/vages.png">
    <p>Vages</p>
  </div>

  <!-- APP 6 -->
  <div class="app" onclick="openApp('3pattiBoss','images/boss.png','4.7','130K','https://3pattiboss.club/?from_gameid=2969921&channelCode=2968974')">
    <img src="images/boss.png">
    <p>Boss</p>
  </div>

</div>

<!-- POPUP -->
<div class="popup" id="popup">
  <div class="popup-content">
    <img id="appImg">
    <h2 id="appName"></h2>
    <p id="appRating"></p>
    <p id="appDownloads"></p>
    <a id="appLink" class="btn" target="_blank">Download</a>
    <div class="close" onclick="closeApp()">Close</div>
  </div>
</div>

<script>
function openApp(name, img, rating, downloads, link) {
  document.getElementById("popup").style.display = "flex";
  document.getElementById("appName").innerText = name;
  document.getElementById("appImg").src = img;
  document.getElementById("appRating").innerText = "⭐ " + rating;
  document.getElementById("appDownloads").innerText = "⬇️ " + downloads + " Downloads";
  document.getElementById("appLink").href = link;
}

function closeApp() {
  document.getElementById("popup").style.display = "none";
}
</script>

</body>
</html>
