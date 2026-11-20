# doritos
<!DOCTYPE html>
<html lang="nl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>DORITOS SUPER DEAL</title>

<style>

body{
    margin:0;
    font-family:Arial,sans-serif;
    background:linear-gradient(135deg,#fff200,#ff9800);
    overflow-x:hidden;
    text-align:center;
}

.banner{
    background:red;
    color:white;
    font-size:32px;
    font-weight:900;
    padding:20px;
    animation:blink 1s infinite;
}

@keyframes blink{
    50%{opacity:.6;}
}

.container{
    padding:30px;
}

.korting{
    display:inline-block;
    margin:20px;
    padding:20px 40px;
    background:#ff0000;
    color:white;
    border-radius:20px;
    font-size:38px;
    font-weight:bold;
    box-shadow:0 0 30px red;
    animation:shake .4s infinite;
}

@keyframes shake{
    25%{transform:rotate(2deg);}
    75%{transform:rotate(-2deg);}
}

.product-wrapper{
    position:relative;
    display:inline-block;
}

.product{
    max-width:400px;
    width:90%;
    transition:.3s;
    filter:drop-shadow(0 20px 20px rgba(0,0,0,.4));
}

.product:hover{
    transform:scale(1.05) rotate(-2deg);
}

.glans{
    position:absolute;
    top:0;
    left:-100%;
    width:50%;
    height:100%;
    background:rgba(255,255,255,.4);
    transform:skewX(-25deg);
    animation:shine 3s infinite;
}

@keyframes shine{
    100%{
        left:150%;
    }
}

.oude-prijs{
    margin-top:20px;
    font-size:40px;
    text-decoration:line-through;
    color:#555;
}

.nieuwe-prijs{
    color:red;
    font-size:90px;
    font-weight:900;
    animation:pulse 1s infinite;
}

@keyframes pulse{
    50%{
        transform:scale(1.1);
    }
}

.timer{
    margin:20px auto;
    width:fit-content;
    background:white;
    padding:15px 30px;
    border-radius:15px;
    font-size:38px;
    box-shadow:0 5px 15px rgba(0,0,0,.2);
}

.buy-btn{
    display:inline-block;
    margin-top:20px;
    padding:20px 40px;
    background:red;
    color:white;
    text-decoration:none;
    border-radius:15px;
    font-size:30px;
    font-weight:bold;
    transition:.3s;
}

.buy-btn:hover{
    transform:scale(1.1);
    background:#c00000;
}

.live{
    margin-top:20px;
    font-size:28px;
    font-weight:bold;
}

.stock{
    background:white;
    max-width:500px;
    margin:30px auto;
    padding:20px;
    border-radius:20px;
}

.bar{
    width:100%;
    height:30px;
    background:#ddd;
    border-radius:20px;
    overflow:hidden;
}

.fill{
    width:85%;
    height:100%;
    background:linear-gradient(to right,#ff0000,#ff9800);
}

.reviews{
    background:white;
    padding:20px;
    border-radius:20px;
    max-width:700px;
    margin:30px auto;
}

.popup{
    position:fixed;
    right:20px;
    bottom:20px;
    background:#00c853;
    color:white;
    padding:15px;
    border-radius:15px;
    font-weight:bold;
    box-shadow:0 0 20px rgba(0,0,0,.3);
}

.floating{
    position:fixed;
    font-size:50px;
    animation:fall 10s linear infinite;
}

@keyframes fall{
    from{
        transform:translateY(-100px) rotate(0deg);
    }

    to{
        transform:translateY(120vh) rotate(360deg);
    }
}

.c1{left:10%;animation-delay:0s;}
.c2{left:30%;animation-delay:2s;}
.c3{left:50%;animation-delay:4s;}
.c4{left:70%;animation-delay:6s;}
.c5{left:90%;animation-delay:8s;}

</style>
</head>

<body>

<div class="floating c1">🔺</div>
<div class="floating c2">🔺</div>
<div class="floating c3">🔺</div>
<div class="floating c4">🔺</div>
<div class="floating c5">🔺</div>

<div class="banner">
🔥 OP = OP | DORITOS MEGA DEAL 🔥
</div>

<div class="container">

<div class="korting">
💥 55% KORTING 💥
</div>

<h1>DORITOS SWEET CHILI PEPPER</h1>

<div class="product-wrapper">
    <img src="doritos.png" class="product">
    <div class="glans"></div>
</div>

<div class="oude-prijs">
€10,99
</div>

<div class="nieuwe-prijs">
€4,99
</div>

<h2>⏰ Aanbieding eindigt over</h2>

<div class="timer" id="timer">
02:00:00
</div>

<br>

<a href="#" class="buy-btn">
🛒 NU KOPEN
</a>

<div class="live">
👀 <span id="viewers">23</span> mensen bekijken dit product nu
</div>

<div class="stock">
<h2>⚠️ Nog maar 17 zakken op voorraad!</h2>

<div class="bar">
<div class="fill"></div>
</div>

</div>

<div class="reviews">

<h2>⭐⭐⭐⭐⭐ 4.9/5</h2>

<p>“Beste smaak ooit!”</p>

<p>“Voor €4,99 direct besteld.”</p>

<p>“Geweldige aanbieding.”</p>

<p>“Veel lekkerder dan verwacht.”</p>

</div>

</div>

<div class="popup" id="popup">
🛒 Iemand uit Houten heeft net gekocht!
</div>

<script>

let tijd = 7200;

function updateTimer(){

let uren = Math.floor(tijd/3600);
let minuten = Math.floor((tijd%3600)/60);
let seconden = tijd%60;

document.getElementById("timer").innerHTML=
String(uren).padStart(2,'0')+":"+
String(minuten).padStart(2,'0')+":"+
String(seconden).padStart(2,'0');

if(tijd>0){
tijd--;
}

}

setInterval(updateTimer,1000);

setInterval(()=>{

document.getElementById("viewers").innerText =
Math.floor(Math.random()*20)+15;

},3000);

const steden = [
"Houten",
"Utrecht",
"Amsterdam",
"Rotterdam",
"Eindhoven",
"Den Haag"
];

setInterval(()=>{

document.getElementById("popup").innerHTML=
"🛒 Iemand uit "+
steden[Math.floor(Math.random()*steden.length)] +
" heeft zojuist gekocht!";

},5000);

window.onload=function(){

for(let i=0;i<75;i++){

let c=document.createElement("div");

c.innerHTML="🎉";

c.style.position="fixed";
c.style.left=Math.random()*100+"vw";
c.style.top=Math.random()*100+"vh";
c.style.fontSize="30px";

document.body.appendChild(c);

setTimeout(()=>{
c.remove();
},5000);

}

};

</script>

</body>
</html>
