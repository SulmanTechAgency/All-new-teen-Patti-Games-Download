<!DOCTYPE html>
<html lang="en">
<head> 
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">

<title>3 Patti Apps</title>

<style>
body {
  margin: 0;
  padding: 0;
  font-family: Arial;
  background: white;
  height: 100vh;
  overflow: hidden; /* no scroll */
}

/* GRID FULL SCREEN */
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  height: 100vh;
  padding: 5px;
  gap: 5px;
}

/* APP ICON */
.app {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.app img {
  width: 55px;
  height: 55px;
  border-radius: 15px;
}

.app span {
  font-size: 10px;
  margin-top: 3px;
  text-align: center;
}

/* POPUP */
.popup {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: none;
  background: rgba(0,0,0,0.6);
  justify-content: center;
  align-items: center;
}

.box {
  background: white;
  padding: 15px;
  border-radius: 12px;
  width: 85%;
  text-align: center;
}

.box img {
  width: 70px;
  border-radius: 15px;
}

.btn {
  display: block;
  margin-top: 8px;
  padding: 8px;
  background: green;
  color: white;
  text-decoration: none;
  border-radius: 8px;
  font-size: 13px;
}

.close {
  margin-top: 8px;
  color: red;
  font-size: 12px;
}
</style>

</head>
<body>

<div class="container">

<div class="app" onclick="openApp('3Patti Pearl','images/pearl.png','4.8','150K','https://3pattipearl.com/?from_gameid=4457555&channelCode=4348309')">
<img src="images/pearl.png"><span>Pearl</span>
</div>

<div class="app" onclick="openApp('3Patti World','images/world.png','4.7','120K','https://3pattiworldpkk.com?from_gameid=5825951&channelCode=100000')">
<img src="images/world.png"><span>World</span>
</div>

<div class="app" onclick="openApp('3Patti Showy','images/showy.png','4.9','180K','https://teenpattishowy.com/?from_gameid=5545690&channelCode=100000')">
<img src="images/showy.png"><span>Showy</span>
</div>

<div class="app" onclick="openApp('3Patti Blue','images/blue.png','4.8','140K','https://3pattibluevip.com?from_gameid=9191920&channelCode=9131811')">
<img src="images/blue.png"><span>Blue</span>
</div>

<div class="app" onclick="openApp('3Patti Vages','images/vages.png','4.6','110K','https://ludovegas.com/?from_gameid=5076422&channelCode=4913682')">
<img src="images/vages.png"><span>Vages</span>
</div>

<div class="app" onclick="openApp('3Patti Boss','images/boss.png','4.7','130K','https://3pattiboss.club/?from_gameid=2969921&channelCode=2968974')">
<img src="images/boss.png"><span>Boss</span>
</div>

</div>

<!-- POPUP -->
<div class="popup" id="popup">
  <div class="box">
    <img id="img">
    <h3 id="name"></h3>
    <p id="rating"></p>
    <p id="downloads"></p>
    <a id="link" class="btn" target="_blank">Download</a>
    <div class="close" onclick="closeApp()">Close</div>
  </div>
</div>

<script>
function openApp(name,img,rating,downloads,link){
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
