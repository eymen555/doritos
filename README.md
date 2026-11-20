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
    background:linear-gradient(135deg,#ffeb3b,#ffa000);
    overflow-x:hidden;
}

.container{
    text-align:center;
    padding:30px;
}

.banner{
    background:red;
    color:white;
    font-size:32px;
    font-weight:bold;
    padding:15px;
    animation:flash 1s infinite;
}

@keyframes flash{
    50%{opacity:0.5;}
}

.product{
    max-width:400px;
    width:100%;
    transition:0.3s;
}

.product:hover{
    transform:scale(1.05);
}

.oude-prijs{
    font-size:40px;
    text-decoration:line-through;
    color:#444;
    margin:10px;
}

.nieuwe-prijs{
    color:red;
    font-size:90px;
    font-weight:bold;
    animation:pulse 1s infinite;
}

@keyframes pulse{
    50%{
        transform:scale(1.1);
    }
}

.timer{
    font-size:40px;
    background:white;
    display:inline-block;
    padding:15px 30px;
    border-radius:12px;
    margin:20px;
    box-shadow:0 0 20px rgba(0,0,0,0.3);
}

.buy-btn{
    display:inline-block;
    background:red;
    color:white;
    padding:20px 40px;
    border-radius:15px;
    text-decoration:none;
    font-size:30px;
    font-weight:bold;
    transition:.3s;
}

.buy-btn:hover{
    background:#c40000;
    transform:scale(1.1);
}

.floating{
    position:fixed;
    font-size:40px;
    animation:fall 10s linear infinite;
}

@keyframes fall{
    from{
        transform:translateY(-100px) rotate(0deg);
    }
    to{
        transform:translateY(110vh) rotate(360deg);
    }
}

.chip1{left:10%;animation-delay:0s;}
.chip2{left:30%;animation-delay:2s;}
.chip3{left:50%;animation-delay:4s;}
.chip4{left:70%;animation-delay:6s;}
.chip5{left:90%;animation-delay:8s;}

</style>
</head>

<body>

<div class="floating chip1">🔺</div>
<div class="floating chip2">🔺</div>
<div class="floating chip3">🔺</div>
<div class="floating chip4">🔺</div>
<div class="floating chip5">🔺</div>

<div class="banner">
🔥 OP = OP | DORITOS ACTIE 🔥
</div>

<div class="container">

<h1>DORITOS SWEET CHILI PEPPER</h1>

<img src="doritos.png" class="product">

<div class="oude-prijs">€10,99</div>

<div class="nieuwe-prijs">€4,99</div>

<h2>Aanbieding eindigt over:</h2>

<div class="timer" id="timer">
02:00:00
</div>

<br>

<a href="#" class="buy-btn">
🛒 NU KOPEN
</a>

</div>

<script>

let tijd = 7200;

function updateTimer(){

let uren = Math.floor(tijd/3600);
let minuten = Math.floor((tijd%3600)/60);
let seconden = tijd%60;

document.getElementById("timer").innerHTML =
String(uren).padStart(2,'0') + ":" +
String(minuten).padStart(2,'0') + ":" +
String(seconden).padStart(2,'0');

if(tijd>0){
tijd--;
}
}

setInterval(updateTimer,1000);

window.onload = function(){

for(let i=0;i<50;i++){

let confetti = document.createElement("div");

confetti.innerHTML="🎉";

confetti.style.position="fixed";
confetti.style.left=Math.random()*100+"vw";
confetti.style.top=Math.random()*100+"vh";
confetti.style.fontSize="30px";

document.body.appendChild(confetti);

setTimeout(()=>{
confetti.remove();
},5000);

}

};

</script>

</body>
</html>
