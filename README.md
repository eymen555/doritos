# doritos
<!DOCTYPE html>
<html lang="nl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Doritos Sweet Chili Pepper</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700;900&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Poppins',sans-serif;
}

body{
background:
radial-gradient(circle at top,
#ff6a00 0%,
#10264f 35%,
#08162d 100%);
color:white;
overflow-x:hidden;
}

/* NAVBAR */

nav{
display:flex;
justify-content:space-between;
align-items:center;
padding:20px 8%;
position:fixed;
width:100%;
top:0;
backdrop-filter:blur(20px);
background:rgba(0,0,0,.2);
z-index:999;
}

.logo{
font-size:32px;
font-weight:900;
color:#ffd000;
}

.nav-btn{
padding:12px 24px;
border-radius:12px;
border:none;
background:#ff5e00;
color:white;
font-weight:bold;
cursor:pointer;
}

/* HERO */

.hero{
min-height:100vh;
display:flex;
align-items:center;
justify-content:center;
padding:120px 8%;
gap:100px;
flex-wrap:wrap;
}

.left{
max-width:600px;
}

.badge{
display:inline-block;
padding:10px 18px;
background:red;
border-radius:30px;
font-weight:700;
margin-bottom:20px;
animation:pulse 1s infinite;
}

h1{
font-size:72px;
line-height:1;
margin-bottom:20px;
}

.subtitle{
font-size:22px;
opacity:.9;
margin-bottom:25px;
}

/* PRIJS */

.price{
display:flex;
align-items:center;
gap:20px;
margin-bottom:25px;
}

.old{
font-size:38px;
text-decoration:line-through;
opacity:.6;
}

.new{
font-size:90px;
font-weight:900;
background:
linear-gradient(
45deg,
#ffd000,
#ff5e00
);

-webkit-background-clip:text;
-webkit-text-fill-color:transparent;
}

/* BUTTONS */

.buttons{
display:flex;
gap:15px;
flex-wrap:wrap;
margin-top:20px;
}

.buy{
padding:18px 35px;
border:none;
border-radius:15px;

background:
linear-gradient(
45deg,
#ff0000,
#ff7000
);

color:white;
font-size:20px;
font-weight:700;
cursor:pointer;

box-shadow:
0 0 30px rgba(255,0,0,.4);
}

.wishlist{
padding:18px 35px;
border:none;
border-radius:15px;
background:white;
color:black;
font-size:20px;
font-weight:700;
cursor:pointer;
}

/* COUNTDOWN */

.countdown{
display:flex;
gap:15px;
margin-top:30px;
}

.box{
background:white;
color:black;
padding:20px;
border-radius:20px;
min-width:100px;
text-align:center;
}

.box h2{
font-size:40px;
}

/* PRODUCT */

.right{
position:relative;
}

.glow{
position:absolute;

width:500px;
height:500px;

background:
radial-gradient(
circle,
rgba(255,136,0,.9),
transparent 70%
);

top:50%;
left:50%;
transform:translate(-50%,-50%);

filter:blur(40px);

z-index:-1;
}

.product{
width:450px;
max-width:90vw;
transition:.3s;
filter:
drop-shadow(
0 25px 35px rgba(0,0,0,.45)
);
}

.product:hover{
transform:
rotate(-3deg)
scale(1.05);
}

/* FEATURES */

.features{
padding:100px 8%;
display:grid;

grid-template-columns:
repeat(auto-fit,minmax(250px,1fr));

gap:25px;
}

.feature{
background:
rgba(255,255,255,.08);

backdrop-filter:blur(15px);

border:
1px solid rgba(255,255,255,.15);

padding:30px;
border-radius:25px;

font-size:20px;
font-weight:600;
}

/* RESPONSIVE */

@media(max-width:900px){

h1{
font-size:50px;
}

.new{
font-size:70px;
}

.hero{
text-align:center;
}

.price{
justify-content:center;
}

.buttons{
justify-content:center;
}

.countdown{
justify-content:center;
}

}

</style>
</head>

<body>

<nav>

<div class="logo">
DORITOS
</div>

<button class="nav-btn">
🛒 Kopen
</button>

</nav>

<section class="hero">

<div class="left">

<div class="badge">
🔥 55% KORTING
</div>

<h1>
Doritos<br>
Sweet Chili Pepper
</h1>

<p class="subtitle">
Knapperige tortilla chips met de perfecte combinatie van zoet en pittig.
</p>

<div class="price">

<span class="old">
€10,99
</span>

<span class="new">
€4,99
</span>

</div>

<div class="buttons">

<button class="buy">
🛒 NU KOPEN
</button>

<button class="wishlist">
❤️ FAVORIET
</button>

</div>

<div class="countdown">

<div class="box">
<h2 id="hours">02</h2>
<span>Uren</span>
</div>

<div class="box">
<h2 id="minutes">00</h2>
<span>Minuten</span>
</div>

<div class="box">
<h2 id="seconds">00</h2>
<span>Seconden</span>
</div>

</div>

</div>

<div class="right">

<div class="glow"></div>

<img
src="doritos.png"
class="product"
alt="Doritos">

</div>

</section>

<section class="features">

<div class="feature">
🌶️ Sweet Chili Pepper smaak
</div>

<div class="feature">
⭐ Bestseller
</div>

<div class="feature">
🔥 Tijdelijke korting
</div>

<div class="feature">
🎉 Perfect voor feestjes
</div>

</section>

<script>

let total = 7200;

setInterval(()=>{

let h=Math.floor(total/3600);
let m=Math.floor((total%3600)/60);
let s=total%60;

document.getElementById("hours").innerText=
String(h).padStart(2,'0');

document.getElementById("minutes").innerText=
String(m).padStart(2,'0');

document.getElementById("seconds").innerText=
String(s).padStart(2,'0');

if(total>0){
total--;
}

},1000);

const product =
document.querySelector('.product');

document.addEventListener('mousemove',(e)=>{

let x =
(e.clientX/window.innerWidth-.5)*20;

let y =
(e.clientY/window.innerHeight-.5)*20;

product.style.transform =
`rotateY(${x}deg)
 rotateX(${-y}deg)
 scale(1.03)`;

});

</script>

</body>
</html>
