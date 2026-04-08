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
  background: #ffffff;
}

/* HEADER */
header {
  text-align: center;
  padding: 10px;
  font-weight: bold;
  font-size: 18px;
  background: #f1f1f1;
}

/* GRID - PERFECT MOBILE */
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 10px;
  padding: 10px;
}

/* APP ICON */
.app {
  text-align: center;
}

.app img {
  width: 65px;
  height: 65px;
  border-radius: 18px;
}

.app p {
  font-size: 11px;
  margin: 5px 0;
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

.popup-box {
  background: white;
  padding: 20px;
  border-radius: 15px;
  width: 90%;
  text-align: center;
}

.popup-box img {
  width: 80px;
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
}
</style>

</head>
<body>

<header>📱 3 Patti Apps</header>

<div class="container">

<div class="app" onclick="openApp('3Patti Pearl','images/pearl.png','4.8','150K','https://3pattipearl.com/?from_gameid=4457555&channelCode=4348309')">
<img src="images/pearl.png">
<p>3Patti Pearl</p>
</div>

<div class="app" onclick="openApp('3Patti World','images/world.png','4.7','120K','https://3pattiworldpkk.com?from_gameid=5825951&channelCode=100000')">
<img src="images/world.png">
<p>3Patti World</p>
</div>

<div class="app" onclick="openApp('3Patti Showy','images/showy.png','4.9','180K','https://teenpattishowy.com/?from_gameid=5545690&channelCode=100000')">
<img src="images/showy.png">
<p>3Patti Showy</p>
</div>

<div class="app" onclick="openApp('3Patti Blue','images/blue.png','4.8','140K','https://3pattibluevip.com?from_gameid=9191920&channelCode=9131811')">
<img src="images/blue.png">
<p>3Patti Blue</p>
</div>

<div class="app" onclick="openApp('3Patti Vages','images/vages.png','4.6','110K','https://ludovegas.com/?from_gameid=5076422&channelCode=4913682')">
<img src="images/vages.png">
<p>3Patti Vages</p>
</div>

<div class="app" onclick="openApp('3Patti Boss','images/boss.png','4.7','130K','https://3pattiboss.club/?from_gameid=2969921&channelCode=2968974')">
<img src="images/boss.png">
<p>3Patti Boss</p>
</div>

</div>

<!-- POPUP -->
<div class="popup" id="popup">
  <div class="popup-box">
    <img id="img">
    <h2 id="name"></h2>
    <p id="rating"></p>
    <p id="downloads"></p>
    <a id="link" class="btn" target="_blank">Download</a>
    <p class="close" onclick="closeApp()">Close</p>
  </div>
</div>

<script>
function openApp(name, img, rating, downloads, link){
document.getElementById("popup").style.display="flex";
document.getElementById("name").innerText=name;
document.getElementById("img").src=img;
document.getElementById("rating").innerText="⭐ "+rating;
document.getElementById("downloads").innerText="⬇️ "+downloads+" Downloads";
document.getElementById("link").href=link;
}

function closeApp(){
document.getElementById("popup").style.display="none";
}
</script>

</body>
</html>
