# doritos
<!DOCTYPE html>
<html lang="nl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Doritos Sweet Chili Pepper | Mega Deal</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700;900&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Poppins',sans-serif;
}

body{
background:linear-gradient(180deg,#071a3c,#0d2c63,#ff6a00);
color:white;
overflow-x:hidden;
}

.particles{
position:fixed;
width:100%;
height:100%;
top:0;
left:0;
pointer-events:none;
z-index:0;
}

.particle{
position:absolute;
font-size:25px;
animation:fall linear infinite;
}

@keyframes fall{
from{
transform:translateY(-100vh) rotate(0deg);
}
to{
transform:translateY(120vh) rotate(360deg);
}
}

.topbar{
background:#ff0000;
text-align:center;
padding:12px;
font-weight:700;
font-size:18px;
}

.hero{
min-height:100vh;
display:flex;
align-items:center;
justify-content:center;
padding:40px;
position:relative;
z-index:1;
}

.container{
max-width:1300px;
display:flex;
flex-wrap:wrap;
align-items:center;
justify-content:center;
gap:50px;
}

.image-box{
position:relative;
}

.product{
width:420px;
max-width:90vw;
filter:drop-shadow(0 20px 30px rgba(0,0,0,.5));
transition:.4s;
}

.product:hover{
transform:rotate(-4deg) scale(1.05);
}

.glow{
position:absolute;
width:450px;
height:450px;
background:radial-gradient(circle,rgba(255,136,0,.7),transparent 70%);
top:50%;
left:50%;
transform:translate(-50%,-50%);
z-index:-1;
}

.discount{
position:absolute;
top:0;
right:-20px;
background:red;
padding:15px 25px;
font-weight:900;
border-radius:20px;
font-size:24px;
box-shadow:0 0 25px red;
animation:shake .4s infinite;
}

@keyframes shake{
25%{transform:rotate(2deg);}
75%{transform:rotate(-2deg);}
}

.content{
max-width:600px;
}

h1{
font-size:60px;
line-height:1.1;
margin-bottom:15px;
}

.subtitle{
font-size:22px;
opacity:.9;
margin-bottom:20px;
}

.old-price{
font-size:40px;
text-decoration:line-through;
color:#ccc;
}

.new-price{
font-size:90px;
font-weight:900;
color:#ffeb3b;
text-shadow:0 0 20px #ffeb3b;
animation:pulse 1s infinite;
}

@keyframes pulse{
50%{
transform:scale(1.07);
}
}

.timer{
margin-top:20px;
background:white;
color:black;
padding:15px 25px;
border-radius:15px;
display:inline-block;
font-size:32px;
font-weight:700;
}

.buttons{
margin-top:30px;
display:flex;
gap:15px;
flex-wrap:wrap;
}

.btn{
padding:18px 35px;
border-radius:15px;
text-decoration:none;
font-weight:700;
font-size:22px;
}

.buy{
background:#ff0000;
color:white;
}

.buy:hover{
background:#c50000;
}

.cart{
background:white;
color:black;
}

.stats{
display:flex;
gap:20px;
flex-wrap:wrap;
margin-top:25px;
}

.stat{
background:rgba(255,255,255,.15);
backdrop-filter:blur(10px);
padding:15px;
border-radius:15px;
}

.section{
padding:80px 20px;
position:relative;
z-index:1;
}

.card{
max-width:1100px;
margin:auto;
background:white;
color:black;
padding:40px;
border-radius:30px;
}

.section h2{
text-align:center;
font-size:45px;
margin-bottom:30px;
}

.stock-bar{
width:100%;
height:35px;
background:#ddd;
border-radius:30px;
overflow:hidden;
margin-top:15px;
}

.stock-fill{
width:82%;
height:100%;
background:linear-gradient(90deg,red,orange);
}

.reviews{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:20px;
}

.review{
background:#f4f4f4;
padding:20px;
border-radius:20px;
}

.faq{
margin-top:20px;
}

.faq-item{
background:#f4f4f4;
margin-bottom:15px;
padding:20px;
border-radius:15px;
}

.popup{
position:fixed;
bottom:20px;
right:20px;
background:#00c853;
padding:15px 20px;
border-radius:15px;
font-weight:700;
z-index:999;
box-shadow:0 10px 30px rgba(0,0,0,.35);
}

footer{
padding:40px;
text-align:center;
background:#06152f;
}

@media(max-width:900px){

h1{
font-size:42px;
}

.new-price{
font-size:70px;
}

.timer{
font-size:24px;
}

}

</style>
</head>
<body>

<div class="particles" id="particles"></div>

<div class="topbar">
🚚 GRATIS VERZENDING VANAF €25 | 🔥 OP = OP
</div>

<section class="hero">

<div class="container">

<div class="image-box">

<div class="glow"></div>

<div class="discount">
55% KORTING
</div>

<img src="doritos.png" class="product">

</div>

<div class="content">

<h1>DORITOS SWEET CHILI PEPPER</h1>

<div class="subtitle">
Krokante tortilla chips met een pittige sweet chili smaak.
</div>

<div class="old-price">€10,99</div>

<div class="new-price">€4,99</div>

<div class="timer" id="timer">
02:00:00
</div>

<div class="buttons">
<a href="#" class="btn buy">🛒 NU KOPEN</a>
<a href="#" class="btn cart">❤️ Favoriet</a>
</div>

<div class="stats">
<div class="stat">👀 <span id="viewers">23</span> bekijken nu</div>
<div class="stat">📦 Nog maar 17 op voorraad</div>
<div class="stat">⭐ 4.9 / 5</div>
</div>

</div>

</div>

</section>

<section class="section">

<div class="card">

<h2>Voorraadniveau</h2>

<p>Nog slechts 17 verpakkingen beschikbaar.</p>

<div class="stock-bar">
<div class="stock-fill"></div>
</div>

</div>

</section>

<section class="section">

<div class="card">

<h2>Klantervaringen ⭐⭐⭐⭐⭐</h2>

<div class="reviews">

<div class="review">
<strong>Jan</strong><br><br>
Beste chipssmaak die ik ooit heb geproefd.
</div>

<div class="review">
<strong>Lisa</strong><br><br>
Voor €4,99 direct besteld.
</div>

<div class="review">
<strong>Mike</strong><br><br>
Geweldige aanbieding.
</div>

</div>

</div>

</section>

<section class="section">

<div class="card">

<h2>Waarom kiezen voor Doritos?</h2>

✅ Knapperige tortilla chips<br><br>
✅ Sweet Chili Pepper smaak<br><br>
✅ Ideaal voor feestjes<br><br>
✅ Perfect bij frisdrank en snacks<br><br>
✅ Tijdelijke aanbieding

</div>

</section>

<section class="section">

<div class="card">

<h2>Veelgestelde vragen</h2>

<div class="faq">

<div class="faq-item">
<b>Hoe lang duurt de aanbieding?</b><br>
Tot de timer afloopt of de voorraad op is.
</div>

<div class="faq-item">
<b>Kan ik meerdere zakken bestellen?</b><br>
Ja, zolang de voorraad strekt.
</div>

<div class="faq-item">
<b>Is dit een tijdelijke actie?</b><br>
Ja.
</div>

</div>

</div>

</section>

<footer>

© 2026 Doritos Mega Deal

</footer>

<div id="popup" class="popup">
🛒 Iemand uit Houten heeft zojuist gekocht!
</div>

<script>

for(let i=0;i<30;i++){

let p=document.createElement("div");

p.className="particle";
p.innerHTML="🔺";

p.style.left=Math.random()*100+"%";
p.style.animationDuration=(8+Math.random()*8)+"s";

document.getElementById("particles").appendChild(p);

}

let tijd=7200;

function updateTimer(){

let h=Math.floor(tijd/3600);
let m=Math.floor((tijd%3600)/60);
let s=tijd%60;

document.getElementById("timer").innerHTML=
String(h).padStart(2,'0')+":"+
String(m).padStart(2,'0')+":"+
String(s).padStart(2,'0');

if(tijd>0){
tijd--;
}

}

setInterval(updateTimer,1000);

setInterval(()=>{

document.getElementById("viewers").textContent=
Math.floor(Math.random()*25)+15;

},3000);

const steden=[
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

},6000);

window.onload=function(){

for(let i=0;i<80;i++){

let c=document.createElement("div");

c.innerHTML="🎉";

c.style.position="fixed";
c.style.left=Math.random()*100+"vw";
c.style.top=Math.random()*100+"vh";
c.style.fontSize="28px";
c.style.pointerEvents="none";

document.body.appendChild(c);

setTimeout(()=>{
c.remove();
},5000);

}

};

</script>

</body>
</html>
