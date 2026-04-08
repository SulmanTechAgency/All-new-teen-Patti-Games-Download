<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>3 Patti Apps</title>

<style>
body{
margin:0;
background:white;
font-family:Arial;
overflow:hidden;
}

.container{
display:grid;
grid-template-columns:repeat(3,1fr);
height:100vh;
gap:5px;
padding:5px;
}

.app{
text-align:center;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
}

.app img{
width:60px;
height:60px;
border-radius:15px;
}

.app span{
font-size:11px;
margin-top:3px;
}

/* popup */
.popup{
position:fixed;
top:0;
left:0;
width:100%;
height:100%;
display:none;
background:rgba(0,0,0,0.6);
justify-content:center;
align-items:center;
}

.box{
background:white;
padding:15px;
border-radius:12px;
width:85%;
text-align:center;
}

.box img{
width:70px;
border-radius:15px;
}

.btn{
display:block;
margin-top:8px;
padding:8px;
background:green;
color:white;
text-decoration:none;
border-radius:8px;
}

.close{
margin-top:8px;
color:red;
}
</style>

</head>
<body>

<div class="container">

<div class="app" onclick="openApp('3Patti Pearl','https://i.imgur.com/8Km9tLL.png','4.8','150K','https://3pattipearl.com/?from_gameid=4457555&channelCode=4348309')">
<img src="https://i.imgur.com/8Km9tLL.png"><span>Pearl</span>
</div>

<div class="app" onclick="openApp('3Patti World','https://i.imgur.com/2nCt3Sbl.png','4.7','120K','https://3pattiworldpkk.com?from_gameid=5825951&channelCode=100000')">
<img src="https://i.imgur.com/2nCt3Sbl.png"><span>World</span>
</div>

<div class="app" onclick="openApp('3Patti Showy','https://i.imgur.com/9yG3XQpl.png','4.9','180K','https://teenpattishowy.com/?from_gameid=5545690&channelCode=100000')">
<img src="https://i.imgur.com/9yG3XQpl.png"><span>Showy</span>
</div>

<div class="app" onclick="openApp('3Patti Blue','https://i.imgur.com/5dYfN1pl.png','4.8','140K','https://3pattibluevip.com?from_gameid=9191920&channelCode=9131811')">
<img src="https://i.imgur.com/5dYfN1pl.png"><span>Blue</span>
</div>

<div class="app" onclick="openApp('3Patti Vages','https://i.imgur.com/0rVeh4Fl.png','4.6','110K','https://ludovegas.com/?from_gameid=5076422&channelCode=4913682')">
<img src="https://i.imgur.com/0rVeh4Fl.png"><span>Vages</span>
</div>

<div class="app" onclick="openApp('3Patti Boss','https://i.imgur.com/eYpH2pOl.png','4.7','130K','https://3pattiboss.club/?from_gameid=2969921&channelCode=2968974')">
<img src="https://i.imgur.com/eYpH2pOl.png"><span>Boss</span>
</div>

</div>

<!-- popup -->
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
function openApp(n,i,r,d,l){
popup.style.display="flex";
img.src=i;
name.innerText=n;
rating.innerText="⭐ "+r;
downloads.innerText="⬇️ "+d+" Downloads";
link.href=l;
}
function closeApp(){
popup.style.display="none";
}
</script>

</body>
</html>
