<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Shop Bom</title>

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial,sans-serif;
}

html{
scroll-behavior:smooth;
}

body{
background:linear-gradient(135deg,#f7f9ff,#eef3ff,#ffffff);
padding-top:65px;
overflow-x:hidden;
}

/* ===========================
   TOP NAVIGATION
=========================== */

.top-nav{
position:fixed;
top:0;
left:0;
width:100%;
height:60px;
background:rgba(255,255,255,.85);
backdrop-filter:blur(18px);
-webkit-backdrop-filter:blur(18px);
display:flex;
align-items:center;
padding:0 12px;
z-index:9999;
border-bottom:1px solid rgba(255,255,255,.4);
box-shadow:0 5px 18px rgba(0,0,0,.08);
}

.nav-btn{
width:42px;
height:42px;
border:none;
border-radius:50%;
cursor:pointer;
font-size:22px;
background:#fff;
box-shadow:0 4px 12px rgba(0,0,0,.15);
transition:.3s;
}

.nav-btn:hover{
transform:rotate(90deg) scale(1.08);
}

.logo{
margin-left:12px;
font-size:23px;
font-weight:bold;
background:linear-gradient(90deg,#2874F0,#00BCD4);
-webkit-background-clip:text;
-webkit-text-fill-color:transparent;
}

.search-box{
flex:1;
margin-left:12px;
display:flex;
align-items:center;
background:#fff;
border-radius:30px;
overflow:hidden;
box-shadow:0 4px 12px rgba(0,0,0,.08);
}

.search-box input{
flex:1;
padding:11px 15px;
border:none;
outline:none;
font-size:15px;
}

.search-box button{
border:none;
background:transparent;
padding:0 15px;
font-size:18px;
cursor:pointer;
}

/* ===========================
   PAGE TITLE
=========================== */

.folder{
margin-top:30px;
text-align:center;
}

.folder h1{
font-size:34px;
font-weight:bold;
background:linear-gradient(90deg,#2196F3,#9C27B0,#FF9800);
-webkit-background-clip:text;
-webkit-text-fill-color:transparent;
margin-bottom:30px;
}

/* ===========================
   APP GRID
=========================== */

.apps{
display:grid;
grid-template-columns:repeat(4,1fr);
gap:18px;
padding:0 10px 25px;
}

.app{
text-align:center;
position:relative;
}

/* ===========================
   PREMIUM 3D GLASS ICON
=========================== */

.icon{
width:72px;
height:72px;
margin:auto;
border-radius:22px;
overflow:hidden;
position:relative;

display:flex;
justify-content:center;
align-items:center;

background:rgba(255,255,255,.20);

backdrop-filter:blur(15px);
-webkit-backdrop-filter:blur(15px);

border:2px solid rgba(255,255,255,.25);

transition:.35s;

animation:float 3s ease-in-out infinite;
}

/* Shine */

.icon::before{

content:"";

position:absolute;

top:-40%;
left:-70%;

width:60%;
height:180%;

background:linear-gradient(
120deg,
transparent,
rgba(255,255,255,.8),
transparent
);

transform:rotate(25deg);

transition:.7s;

}

.icon:hover::before{

left:130%;

}

.icon:hover{

transform:translateY(-10px) scale(1.08);

}

.icon img{

width:100%;
height:100%;
object-fit:cover;

border-radius:20px;

}

/* Floating */

@keyframes float{

0%{
transform:translateY(0);
}

50%{
transform:translateY(-8px);
}

100%{
transform:translateY(0);
}

}


/* ===========================
   NEON COLOR CLASSES
=========================== */

.blue{
border:2px solid #2196F3;
box-shadow:0 0 10px #2196F3,
0 0 20px #2196F3,
0 0 35px #2196F3;
}

.orange{
border:2px solid #FF9800;
box-shadow:0 0 10px #FF9800,
0 0 20px #FF9800,
0 0 35px #FF9800;
}

.green{
border:2px solid #00E676;
box-shadow:0 0 10px #00E676,
0 0 20px #00E676,
0 0 35px #00E676;
}

.purple{
border:2px solid #C511FF;
box-shadow:0 0 10px #C511FF,
0 0 20px #C511FF,
0 0 35px #C511FF;
}

.red{
border:2px solid #FF1744;
box-shadow:0 0 10px #FF1744,
0 0 20px #FF1744,
0 0 35px #FF1744;
}

.yellow{
border:2px solid #FFD600;
box-shadow:0 0 10px #FFD600,
0 0 20px #FFD600,
0 0 35px #FFD600;
}

.pink{
border:2px solid #FF4081;
box-shadow:0 0 10px #FF4081,
0 0 20px #FF4081,
0 0 35px #FF4081;
}

.cyan{
border:2px solid #00E5FF;
box-shadow:0 0 10px #00E5FF,
0 0 20px #00E5FF,
0 0 35px #00E5FF;
}

.lime{
border:2px solid #76FF03;
box-shadow:0 0 10px #76FF03,
0 0 20px #76FF03,
0 0 35px #76FF03;
}

.gold{
border:2px solid #FFC107;
box-shadow:0 0 10px #FFC107,
0 0 20px #FFC107,
0 0 35px #FFC107;
}

.silver{
border:2px solid #CFD8DC;
box-shadow:0 0 10px #CFD8DC,
0 0 20px #CFD8DC,
0 0 35px #CFD8DC;
}

.obsidian{
border:2px solid #212121;
box-shadow:0 0 10px #212121,
0 0 20px #212121,
0 0 35px #212121;
}

.online{
display:inline-block;
width:8px;
height:8px;
background:#00E676;
border-radius:50%;
margin-right:5px;
box-shadow:0 0 8px #00E676;
}

.notify{
position:absolute;
top:-5px;
right:8px;
width:16px;
height:16px;
background:#FF1744;
border-radius:50%;
border:2px solid #fff;
box-shadow:0 0 10px #FF1744;
}

.app p{
margin-top:8px;
font-size:13px;
font-weight:bold;
color:#333;
}

/* ===========================
   SIDE MENU
=========================== */

.side-menu{
position:fixed;
top:0;
left:-270px;
width:260px;
height:100%;
background:rgba(255,255,255,.95);
backdrop-filter:blur(18px);
-webkit-backdrop-filter:blur(18px);
transition:.35s;
z-index:99999;
box-shadow:5px 0 20px rgba(0,0,0,.15);
}

.side-menu.active{
left:0;
}

.menu-header{
display:flex;
justify-content:space-between;
align-items:center;
padding:18px;
font-size:20px;
font-weight:bold;
border-bottom:1px solid #eee;
}

.menu-header span{
font-size:28px;
cursor:pointer;
}

.side-menu a{
display:block;
padding:16px 20px;
text-decoration:none;
color:#333;
font-size:16px;
transition:.3s;
border-bottom:1px solid #f2f2f2;
}

.side-menu a:hover{
background:#2874F0;
color:#fff;
padding-left:28px;
}

/* ===========================
   OVERLAY
=========================== */

.overlay{
display:none;
position:fixed;
top:0;
left:0;
width:100%;
height:100%;
background:rgba(0,0,0,.35);
backdrop-filter:blur(3px);
z-index:9999;
}

.overlay.active{
display:block;
}

</style>

</head>

<body>

<div class="top-nav">

<button class="nav-btn" onclick="openMenu()">☰</button>

<div class="logo">Shop Bom</div>

<div class="search-box">
<input type="text" placeholder="Search apps...">
<button>🔍</button>
</div>

</div>

<div id="sideMenu" class="side-menu">

<div class="menu-header">
Shop Bom
<span onclick="closeMenu()">✕</span>
</div>

<a href="https://sites.google.com/view/shopbom/information">ℹ️ Information</a>

<a href="https://sites.google.com/view/shopbom/information/privacy-policy">🔒 Privacy Policy</a>

<a href="https://sites.google.com/view/shopbom/information/help">❓ Help</a>

</div>

<div id="overlay" class="overlay" onclick="closeMenu()"></div>

<div class="folder">

<h1>APPS +8</h1>

<div class="apps">
  
  <!-- Flipkart -->
<div class="app">
<a href="https://fktr.in/qnCIKJu" target="_self">
<div class="icon blue">
<img src="https://i.ibb.co/BHk8C7p8/ANI-20250422062444.jpg" alt="Flipkart">
</div>
</a>
<p><span class="online"></span>Flipkart</p>
</div>

<!-- Honeygain -->
<div class="app">
<a href="https://bitli.in/uVcGTye" target="_self">
<div class="icon orange">
<img src="https://i.ibb.co/1YFrQJBr/unnamed-4.png" alt="Amazon">
</div>
</a>
<p><span class="online"></span>Amazon</p>
</div>

<!-- Meesho -->
<div class="app">
<a href="https://bitli.in/J5sxa0i" target="_self">
<div class="icon purple">
<img src="https://i.ibb.co/Tq1C2Wnq/IMG-20260718-173813.jpg" alt="Meesho">
</div>
</a>
<p><span class="online"></span>Meesho</p>
</div>

<!-- Meesho -->
<div class="app">
<a href="https://myntr.it/rmowj4H" target="_self">
<div class="icon cyan">
<img src="https://i.ibb.co/VpgqpRWp/IMG-20260718-175728.jpg" alt="Meesho">
</div>
</a>
<p><span class="online"></span>Meesho</p>
</div>

<!-- Ajio -->
<div class="app">
<a href="https://ajiio.in/AocU3im" target="_self">
<div class="icon blue">
<img src="https://i.ibb.co/JRNZHJVD/ajio-logo.webp" alt="Ajio">
</div>
</a>
<p><span class="online"></span>Ajio</p>
</div>

<!-- YouTube -->
<div class="app">
<a href="https://bitli.in/VzgG5pf" target="_self">
<div class="icon red">
<img src="https://i.ibb.co/hRbLSXzr/IMG-20260718-181015.png" alt="Dermaco">
</div>
</a>
<p><span class="online"></span>Dermaco</p>
</div>

<!-- Instagram -->
<div class="app">
<a href="https://bitli.in/HUs2n17" target="_self">
<div class="icon yellow">
<img src="https://i.ibb.co/M5xZ5Qsy/1db7bb231363215-Y3-Jvc-Cwx-Mzgw-LDEw-ODAs-Mjcw-LDA.jpg" alt="Muscleblaze">
</div>
</a>
<p><span class="online"></span>Muscleb..</p>
</div>

<!-- THE MAN COMPANY -->
<div class="app">
<a href="https://bitli.in/IKA0ppb" target="_self">
<div class="icon red">
<img src="https://i.ibb.co/WvYhHyL6/the-man-company-logo.jpg" alt="THE MAN COMPANY">
</div>
</a>
<p><span class="online"></span>THE MAN COMPANY</p>
</div>

</div>
</div>

<script>

/* ==========================
   Side Menu
========================== */

function openMenu(){
    document.getElementById("sideMenu").classList.add("active");
    document.getElementById("overlay").classList.add("active");
}

function closeMenu(){
    document.getElementById("sideMenu").classList.remove("active");
    document.getElementById("overlay").classList.remove("active");
}

/* ==========================
   Search Apps
========================== */

const searchInput = document.querySelector(".search-box input");
const apps = document.querySelectorAll(".app");

searchInput.addEventListener("keyup", function(){

    const filter = this.value.toLowerCase();

    apps.forEach(app=>{

        const appName = app.querySelector("p").innerText.toLowerCase();

        if(appName.includes(filter)){
            app.style.display = "block";
        }else{
            app.style.display = "none";
        }

    });

});

/* ==========================
   Ripple Effect
========================== */

document.querySelectorAll(".icon").forEach(icon=>{

    icon.addEventListener("click",function(e){

        const ripple=document.createElement("span");

        const size=Math.max(this.clientWidth,this.clientHeight);

        ripple.style.width=size+"px";
        ripple.style.height=size+"px";

        ripple.style.left=(e.offsetX-size/2)+"px";
        ripple.style.top=(e.offsetY-size/2)+"px";

        ripple.className="ripple";

        this.appendChild(ripple);

        setTimeout(()=>{
            ripple.remove();
        },600);

    });

});

/* ==========================
   Auto Fade Animation
========================== */

const observer=new IntersectionObserver((entries)=>{

    entries.forEach(entry=>{

        if(entry.isIntersecting){

            entry.target.style.opacity="1";
            entry.target.style.transform="translateY(0)";

        }

    });

});

document.querySelectorAll(".app").forEach(app=>{

    app.style.opacity="0";
    app.style.transform="translateY(40px)";
    app.style.transition=".5s ease";

    observer.observe(app);

});

/* ==========================
   Online Status Blink
========================== */

setInterval(()=>{

document.querySelectorAll(".online").forEach(dot=>{

dot.style.opacity = dot.style.opacity=="0.3" ? "1" : "0.3";

});

},700);

</script>






 
