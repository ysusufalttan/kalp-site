# kalp-site
<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<title>Kalp</title>
<style>
body{
margin:0;
height:100vh;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
background:#111;
color:white;
font-family:sans-serif;
overflow:hidden;
}

.pixel-heart{
font-size:90px;
text-align:center;
}

button{
padding:12px 25px;
margin:10px;
font-size:18px;
border:none;
border-radius:10px;
cursor:pointer;
transition:0.3s;
}

#yes{
background:#4CAF50;
color:white;
}

#no{
background:#f44336;
color:white;
transition:1s;
}
</style>
</head>
<body>

<div class="pixel-heart">
❤️
<div>beni seviyormusun</div>
</div>

<div>
<button id="yes">Evet</button>
<button id="no">Hayır</button>
</div>

<script>
let count = 0;
let yesBtn = document.getElementById("yes");
let noBtn = document.getElementById("no");

noBtn.addEventListener("click", function(){
count++;
yesBtn.style.transform = "scale(" + (1 + count * 0.3) + ")";

if(count >= 4){
noBtn.style.opacity = "0";
setTimeout(function(){
noBtn.style.display = "none";
},1000);
}
});

yesBtn.addEventListener("click", function(){
document.body.innerHTML = "<h1 style='font-size:50px;'>yaa şapşik</h1>";
});
</script>

</body>
</html>
