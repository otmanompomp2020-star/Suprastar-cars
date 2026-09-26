<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Suprastar Cars | Luxury Car Rental</title>

<meta name="description" content="Suprastar Cars — Location de voitures premium à Salé, Maroc.">

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700;800&family=Playfair+Display:wght@500;600;700&display=swap" rel="stylesheet">

<style>

/* =========================================================
   RESET
========================================================= */

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

html{
    scroll-behavior:smooth;
}

body{
    font-family:'Montserrat',sans-serif;
    background:#050505;
    color:#fff;
    overflow-x:hidden;
}

a{
    color:inherit;
    text-decoration:none;
}

button{
    font-family:inherit;
}

img{
    max-width:100%;
    display:block;
}


/* =========================================================
   ANIMATED BACKGROUND
========================================================= */

body::before{
    content:"";
    position:fixed;
    inset:0;
    z-index:-5;

    background:
        radial-gradient(circle at 15% 20%, rgba(212,175,55,.15), transparent 25%),
        radial-gradient(circle at 85% 30%, rgba(255,255,255,.07), transparent 25%),
        radial-gradient(circle at 50% 90%, rgba(212,175,55,.08), transparent 30%),
        #050505;

    animation:bgMove 12s ease-in-out infinite alternate;
}

@keyframes bgMove{
    0%{
        transform:scale(1);
        background-position:0 0,100% 0,50% 100%;
    }

    100%{
        transform:scale(1.08);
        background-position:20% 10%,80% 30%,40% 80%;
    }
}


/* moving grid */

.grid-bg{
    position:fixed;
    inset:0;
    z-index:-4;
    pointer-events:none;

    background-image:
        linear-gradient(rgba(255,255,255,.025) 1px,transparent 1px),
        linear-gradient(90deg,rgba(255,255,255,.025) 1px,transparent 1px);

    background-size:60px 60px;

    mask-image:linear-gradient(to bottom,transparent,black 20%,black 80%,transparent);
}


/* light blobs */

.light{
    position:fixed;
    width:450px;
    height:450px;
    border-radius:50%;
    filter:blur(100px);
    opacity:.08;
    pointer-events:none;
    z-index:-3;
}

.light.one{
    background:#d4af37;
    top:5%;
    left:-200px;
    animation:floatOne 15s infinite alternate;
}

.light.two{
    background:#fff;
    right:-200px;
    top:40%;
    animation:floatTwo 18s infinite alternate;
}

@keyframes floatOne{
    to{
        transform:translate(400px,200px);
    }
}

@keyframes floatTwo{
    to{
        transform:translate(-350px,-150px);
    }
}


/* =========================================================
   HEADER
========================================================= */

header{
    position:fixed;
    top:0;
    left:0;
    right:0;
    height:78px;
    z-index:1000;

    display:flex;
    align-items:center;
    justify-content:space-between;

    padding:0 6%;

    background:rgba(5,5,5,.72);
    backdrop-filter:blur(18px);
    -webkit-backdrop-filter:blur(18px);

    border-bottom:1px solid rgba(255,255,255,.08);
}

.logo{
    display:flex;
    align-items:center;
    gap:10px;

    font-size:22px;
    font-weight:800;
    letter-spacing:2px;
}

.logo span{
    color:#d4af37;
}

.logo-dot{
    width:9px;
    height:9px;
    background:#d4af37;
    border-radius:50%;
    box-shadow:0 0 18px #d4af37;
    animation:pulse 2s infinite;
}

@keyframes pulse{
    50%{
        box-shadow:0 0 35px #d4af37;
    }
}

nav{
    display:flex;
    align-items:center;
    gap:32px;
}

nav a{
    position:relative;
    font-size:13px;
    text-transform:uppercase;
    letter-spacing:1.5px;
    color:#bbb;
    transition:.3s;
}

nav a::after{
    content:"";
    position:absolute;
    left:0;
    bottom:-8px;
    width:0;
    height:1px;
    background:#d4af37;
    transition:.3s;
}

nav a:hover{
    color:#fff;
}

nav a:hover::after{
    width:100%;
}

.menu-btn{
    display:none;
    background:none;
    border:0;
    color:#fff;
    font-size:27px;
    cursor:pointer;
}


/* =========================================================
   HERO
========================================================= */

.hero{
    min-height:100vh;
    position:relative;

    display:flex;
    align-items:center;
    justify-content:center;

    text-align:center;
    padding:120px 20px 70px;

    overflow:hidden;
}

.hero-content{
    max-width:1000px;
    position:relative;
    z-index:2;
}

.eyebrow{
    color:#d4af37;
    text-transform:uppercase;
    letter-spacing:6px;
    font-size:12px;
    font-weight:600;
    margin-bottom:25px;

    animation:fadeDown 1s ease forwards;
}

.hero h1{
    font-family:'Playfair Display',serif;
    font-size:clamp(55px,10vw,125px);
    line-height:.88;
    font-weight:600;
    letter-spacing:-5px;

    background:linear-gradient(
        120deg,
        #fff,
        #d4af37,
        #fff,
        #777,
        #fff
    );

    background-size:300% auto;
    -webkit-background-clip:text;
    color:transparent;

    animation:
        titleGradient 8s linear infinite,
        fadeUp 1s ease forwards;
}

@keyframes titleGradient{
    to{
        background-position:300% center;
    }
}

.hero h1 span{
    display:block;
}

.hero-sub{
    max-width:650px;
    margin:35px auto 0;

    color:#aaa;
    line-height:1.8;
    font-size:15px;

    animation:fadeUp 1.3s ease forwards;
}

.hero-buttons{
    margin-top:40px;

    display:flex;
    justify-content:center;
    gap:15px;

    animation:fadeUp 1.6s ease forwards;
}

.btn{
    border:1px solid #d4af37;
    padding:15px 28px;
    border-radius:40px;
    text-transform:uppercase;
    letter-spacing:1.5px;
    font-size:11px;
    font-weight:700;
    transition:.35s;
    cursor:pointer;
}

.btn.gold{
    background:#d4af37;
    color:#050505;
}

.btn.gold:hover{
    background:#fff;
    border-color:#fff;
    transform:translateY(-4px);
    box-shadow:0 15px 40px rgba(212,175,55,.25);
}

.btn.outline{
    color:#fff;
}

.btn.outline:hover{
    background:#fff;
    color:#000;
    border-color:#fff;
    transform:translateY(-4px);
}


/* floating car silhouette */

.hero-car{
    position:absolute;
    width:min(850px,90vw);
    height:300px;
    bottom:-90px;
    left:50%;
    transform:translateX(-50%);

    border-radius:50%;
    background:radial-gradient(
        ellipse,
        rgba(212,175,55,.20),
        transparent 65%
    );

    filter:blur(5px);
    animation:heroGlow 5s infinite alternate;
}

@keyframes heroGlow{
    to{
        transform:translateX(-50%) scale(1.15);
        opacity:.6;
    }
}


/* =========================================================
   STATS
========================================================= */

.stats{
    max-width:1000px;
    margin:-30px auto 0;

    display:grid;
    grid-template-columns:repeat(3,1fr);

    border-top:1px solid rgba(255,255,255,.1);
    border-bottom:1px solid rgba(255,255,255,.1);

    position:relative;
    z-index:5;
}

.stat{
    text-align:center;
    padding:28px 15px;
    border-right:1px solid rgba(255,255,255,.08);
}

.stat:last-child{
    border-right:0;
}

.stat strong{
    display:block;
    font-size:26px;
    color:#d4af37;
    margin-bottom:5px;
}

.stat span{
    font-size:10px;
    text-transform:uppercase;
    letter-spacing:2px;
    color:#888;
}


/* =========================================================
   SECTION
========================================================= */

section{
    padding:120px 6%;
}

.section-head{
    display:flex;
    justify-content:space-between;
    align-items:end;
    margin-bottom:50px;
}

.section-title small{
    color:#d4af37;
    text-transform:uppercase;
    letter-spacing:4px;
    font-size:10px;
}

.section-title h2{
    font-family:'Playfair Display',serif;
    font-size:clamp(38px,5vw,65px);
    font-weight:500;
    margin-top:10px;
}

.section-description{
    color:#777;
    max-width:360px;
    font-size:13px;
    line-height:1.7;
}


/* =========================================================
   FILTERS
========================================================= */

.filters{
    display:flex;
    gap:10px;
    flex-wrap:wrap;
    margin-bottom:35px;
}

.filter{
    border:1px solid rgba(255,255,255,.12);
    background:rgba(255,255,255,.03);
    color:#888;

    padding:10px 18px;
    border-radius:30px;

    cursor:pointer;

    text-transform:uppercase;
    letter-spacing:1px;
    font-size:10px;

    transition:.3s;
}

.filter:hover,
.filter.active{
    background:#d4af37;
    border-color:#d4af37;
    color:#000;
}


/* =========================================================
   CARS GRID
========================================================= */

.cars{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:20px;
}


/* =========================================================
   CAR CARD
========================================================= */

.car{
    position:relative;
    overflow:hidden;

    min-height:370px;

    border:1px solid rgba(255,255,255,.09);
    border-radius:20px;

    background:
        linear-gradient(
            145deg,
            rgba(255,255,255,.08),
            rgba(255,255,255,.025)
        );

    transform-style:preserve-3d;
    perspective:1000px;

    transition:
        transform .2s ease,
        border .4s ease,
        box-shadow .4s ease;

    cursor:pointer;

    opacity:0;
    transform:translateY(40px);
}

.car.visible{
    opacity:1;
    transform:translateY(0);
}

.car:hover{
    border-color:rgba(212,175,55,.55);

    box-shadow:
        0 30px 70px rgba(0,0,0,.5),
        0 0 35px rgba(212,175,55,.08);
}

.car::before{
    content:"";
    position:absolute;
    inset:0;

    background:
        radial-gradient(
            circle at var(--mouse-x,50%) var(--mouse-y,50%),
            rgba(255,255,255,.12),
            transparent 25%
        );

    opacity:0;
    transition:.2s;
    z-index:3;
    pointer-events:none;
}

.car:hover::before{
    opacity:1;
}

.car-image{
    height:220px;
    position:relative;
    overflow:hidden;
}

.car-image::after{
    content:"";
    position:absolute;
    inset:0;

    background:
        linear-gradient(
            to bottom,
            transparent 40%,
            rgba(5,5,5,.9)
        );
}

.car-image img{
    width:100%;
    height:100%;
    object-fit:cover;

    transition:
        transform .8s cubic-bezier(.2,.8,.2,1),
        filter .5s;
}

.car:hover .car-image img{
    transform:scale(1.12) translateZ(30px);
    filter:brightness(1.08) saturate(1.1);
}

.badge{
    position:absolute;
    top:15px;
    left:15px;
    z-index:5;

    padding:7px 10px;

    border:1px solid rgba(212,175,55,.5);
    border-radius:20px;

    color:#d4af37;
    background:rgba(0,0,0,.6);
    backdrop-filter:blur(10px);

    font-size:8px;
    font-weight:700;
    letter-spacing:1.5px;
}

.car-info{
    padding:18px;
    position:relative;
    z-index:5;
}

.car-category{
    color:#d4af37;
    font-size:9px;
    letter-spacing:2px;
    text-transform:uppercase;
}

.car-name{
    font-family:'Playfair Display',serif;
    font-size:24px;
    margin:5px 0 12px;
}

.car-specs{
    display:flex;
    gap:10px;
    flex-wrap:wrap;
}

.spec{
    color:#888;
    font-size:9px;
    border-right:1px solid rgba(255,255,255,.15);
    padding-right:10px;
}

.spec:last-child{
    border:0;
}

.car-footer{
    display:flex;
    justify-content:space-between;
    align-items:center;

    margin-top:18px;
}

.details{
    color:#fff;
    font-size:9px;
    letter-spacing:1px;
    text-transform:uppercase;
}

.arrow{
    width:30px;
    height:30px;

    border:1px solid rgba(255,255,255,.15);
    border-radius:50%;

    display:grid;
    place-items:center;

    transition:.3s;
}

.car:hover .arrow{
    background:#d4af37;
    color:#000;
    border-color:#d4af37;
    transform:rotate(-45deg);
}


/* =========================================================
   FEATURES
========================================================= */

.features{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:20px;
}

.feature{
    padding:35px;
    border:1px solid rgba(255,255,255,.08);
    border-radius:18px;

    background:rgba(255,255,255,.025);

    transition:.4s;
}

.feature:hover{
    transform:translateY(-8px);
    border-color:rgba(212,175,55,.4);
}

.feature-icon{
    width:50px;
    height:50px;

    display:grid;
    place-items:center;

    border-radius:50%;

    background:rgba(212,175,55,.08);
    color:#d4af37;

    font-size:20px;

    margin-bottom:25px;
}

.feature h3{
    font-size:17px;
    margin-bottom:12px;
}

.feature p{
    color:#777;
    font-size:12px;
    line-height:1.8;
}


/* =========================================================
   CTA
========================================================= */

.cta{
    margin:30px 6% 120px;

    position:relative;
    overflow:hidden;

    padding:80px 8%;

    border-radius:30px;
    border:1px solid rgba(212,175,55,.25);

    background:
        radial-gradient(
            circle at 80% 50%,
            rgba(212,175,55,.15),
            transparent 35%
        ),
        rgba(255,255,255,.025);
}

.cta::before{
    content:"SUPRASTAR";
    position:absolute;

    right:-30px;
    bottom:-60px;

    font-size:130px;
    font-weight:800;

    color:rgba(255,255,255,.025);

    pointer-events:none;
}

.cta h2{
    font-family:'Playfair Display',serif;
    font-size:clamp(35px,5vw,65px);
    max-width:650px;
}

.cta p{
    color:#888;
    margin:20px 0 30px;
    max-width:550px;
    line-height:1.8;
    font-size:13px;
}


/* =========================================================
   FOOTER
========================================================= */

footer{
    padding:50px 6% 30px;

    border-top:1px solid rgba(255,255,255,.08);

    display:flex;
    justify-content:space-between;
    align-items:center;

    color:#666;
    font-size:10px;
    letter-spacing:1px;
}

.footer-logo{
    color:#fff;
    font-weight:700;
    letter-spacing:2px;
}

.footer-logo span{
    color:#d4af37;
}


/* =========================================================
   MODAL
========================================================= */

.modal{
    position:fixed;
    inset:0;

    background:rgba(0,0,0,.82);
    backdrop-filter:blur(20px);
    -webkit-backdrop-filter:blur(20px);

    display:flex;
    align-items:center;
    justify-content:center;

    padding:25px;

    z-index:3000;

    opacity:0;
    visibility:hidden;

    transition:.4s;
}

.modal.active{
    opacity:1;
    visibility:visible;
}

.modal-box{
    width:min(1050px,100%);
    max-height:90vh;
    overflow:auto;

    position:relative;

    display:grid;
    grid-template-columns:1.2fr .8fr;

    border:1px solid rgba(212,175,55,.3);
    border-radius:28px;

    background:
        radial-gradient(
            circle at 20% 10%,
            rgba(212,175,55,.08),
            transparent 30%
        ),
        #090909;

    box-shadow:
        0 50px 150px rgba(0,0,0,.8),
        0 0 70px rgba(212,175,55,.08);

    transform:scale(.85) translateY(40px);
    transition:.5s cubic-bezier(.2,.8,.2,1);
}

.modal.active .modal-box{
    transform:scale(1) translateY(0);
}


/* close */

.close-modal{
    position:absolute;
    right:20px;
    top:20px;

    width:40px;
    height:40px;

    border-radius:50%;

    border:1px solid rgba(255,255,255,.15);
    background:rgba(0,0,0,.5);

    color:#fff;

    font-size:20px;
    cursor:pointer;

    z-index:20;

    transition:.3s;
}

.close-modal:hover{
    background:#d4af37;
    color:#000;
    transform:rotate(90deg);
}


/* modal visual */

.modal-visual{
    min-height:500px;
    position:relative;
    overflow:hidden;

    display:flex;
    align-items:center;
    justify-content:center;
}

.modal-visual::before{
    content:"";

    position:absolute;
    width:500px;
    height:500px;

    border-radius:50%;

    background:radial-gradient(
        circle,
        rgba(212,175,55,.16),
        transparent 65%
    );

    animation:modalGlow 4s infinite alternate;
}

@keyframes modalGlow{
    to{
        transform:scale(1.25);
    }
}

.modal-car{
    width:90%;
    max-height:420px;

    object-fit:contain;

    position:relative;
    z-index:5;

    filter:
        drop-shadow(0 30px 30px rgba(0,0,0,.8))
        drop-shadow(0 0 25px rgba(212,175,55,.08));

    transform:translateX(-80px) scale(.7) rotateY(18deg);

    opacity:0;
}

.modal.active .modal-car{
    animation:carReveal .9s cubic-bezier(.2,.8,.2,1) forwards;
}

@keyframes carReveal{
    to{
        transform:translateX(0) scale(1) rotateY(0);
        opacity:1;
    }
}


/* door effect */

.door{
    position:absolute;
    z-index:4;

    width:120px;
    height:220px;

    border:1px solid rgba(212,175,55,.5);

    background:
        linear-gradient(
            135deg,
            rgba(212,175,55,.15),
            rgba(255,255,255,.02)
        );

    opacity:0;

    transform:scaleX(.1);

    transition:.8s cubic-bezier(.2,.8,.2,1);
}

.door.left{
    left:10%;
    top:28%;
    transform-origin:right center;
}

.door.right{
    right:10%;
    top:28%;
    transform-origin:left center;
}

.modal.active .door.left{
    opacity:.55;
    transform:rotateY(55deg) scaleX(1);
}

.modal.active .door.right{
    opacity:.55;
    transform:rotateY(-55deg) scaleX(1);
}


/* modal content */

.modal-content{
    padding:70px 45px 45px;

    display:flex;
    flex-direction:column;
    justify-content:center;
}

.modal-category{
    color:#d4af37;
    text-transform:uppercase;
    letter-spacing:3px;
    font-size:10px;
    margin-bottom:10px;
}

.modal-title{
    font-family:'Playfair Display',serif;
    font-size:48px;
    line-height:1;

    margin-bottom:20px;
}

.modal-description{
    color:#888;
    font-size:12px;
    line-height:1.8;
    margin-bottom:25px;
}

.modal-specs{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:10px;

    margin-bottom:30px;
}

.modal-spec{
    padding:14px;

    border:1px solid rgba(255,255,255,.08);
    border-radius:10px;

    background:rgba(255,255,255,.025);
}

.modal-spec small{
    display:block;
    color:#666;
    text-transform:uppercase;
    letter-spacing:1px;
    font-size:8px;
    margin-bottom:5px;
}

.modal-spec strong{
    font-size:12px;
}

.whatsapp-btn{
    display:flex;
    justify-content:center;
    align-items:center;
    gap:10px;

    width:100%;

    padding:16px;

    border-radius:30px;

    background:#d4af37;
    color:#000;

    text-transform:uppercase;
    letter-spacing:1px;

    font-size:10px;
    font-weight:800;

    transition:.3s;
}

.whatsapp-btn:hover{
    background:#fff;
    transform:translateY(-3px);
    box-shadow:0 15px 30px rgba(212,175,55,.15);
}


/* =========================================================
   WHATSAPP FLOAT
========================================================= */

.whatsapp{
    position:fixed;
    right:22px;
    bottom:22px;

    width:58px;
    height:58px;

    border-radius:50%;

    background:#25D366;
    color:#fff;

    display:grid;
    place-items:center;

    font-size:25px;

    z-index:1500;

    box-shadow:
        0 10px 30px rgba(37,211,102,.3);

    animation:whatsappPulse 2.5s infinite;
}

@keyframes whatsappPulse{
    0%,100%{
        box-shadow:0 10px 30px rgba(37,211,102,.3);
    }

    50%{
        box-shadow:
            0 10px 40px rgba(37,211,102,.55),
            0 0 0 10px rgba(37,211,102,.05);
    }
}


/* =========================================================
   ANIMATIONS
========================================================= */

@keyframes fadeUp{
    from{
        opacity:0;
        transform:translateY(30px);
    }

    to{
        opacity:1;
        transform:translateY(0);
    }
}

@keyframes fadeDown{
    from{
        opacity:0;
        transform:translateY(-20px);
    }

    to{
        opacity:1;
        transform:translateY(0);
    }
}


/* =========================================================
   SCROLLBAR
========================================================= */

::-webkit-scrollbar{
    width:8px;
}

::-webkit-scrollbar-track{
    background:#050505;
}

::-webkit-scrollbar-thumb{
    background:#333;
    border-radius:10px;
}

::-webkit-scrollbar-thumb:hover{
    background:#d4af37;
}


/* =========================================================
   RESPONSIVE
========================================================= */

@media(max-width:1200px){

    .cars{
        grid-template-columns:repeat(3,1fr);
    }

}

@media(max-width:900px){

    nav{
        position:absolute;
        top:78px;
        left:0;
        right:0;

        background:rgba(5,5,5,.97);
        backdrop-filter:blur(20px);

        padding:25px;

        flex-direction:column;
        gap:22px;

        border-bottom:1px solid rgba(255,255,255,.08);

        transform:translateY(-150%);
        transition:.4s;
    }

    nav.active{
        transform:translateY(0);
    }

    .menu-btn{
        display:block;
    }

    .cars{
        grid-template-columns:repeat(2,1fr);
    }

    .features{
        grid-template-columns:1fr;
    }

    .modal-box{
        grid-template-columns:1fr;
        max-height:90vh;
    }

    .modal-visual{
        min-height:330px;
    }

    .modal-content{
        padding:35px;
    }

    .modal-title{
        font-size:38px;
    }

}

@media(max-width:600px){

    header{
        padding:0 20px;
    }

    section{
        padding:80px 20px;
    }

    .hero{
        padding-left:20px;
        padding-right:20px;
    }

    .hero h1{
        font-size:58px;
        letter-spacing:-3px;
    }

    .hero-sub{
        font-size:13px;
    }

    .hero-buttons{
        flex-direction:column;
        align-items:center;
    }

    .btn{
        width:220px;
    }

    .stats{
        margin:0 20px;
    }

    .stat{
        padding:20px 8px;
    }

    .stat strong{
        font-size:20px;
    }

    .stat span{
        font-size:7px;
    }

    .section-head{
        display:block;
    }

    .section-description{
        margin-top:20px;
    }

    .cars{
        grid-template-columns:1fr;
    }

    .car{
        min-height:390px;
    }

    .features{
        gap:15px;
    }

    .feature{
        padding:25px;
    }

    .cta{
        margin:0 20px 80px;
        padding:50px 25px;
    }

    .cta::before{
        font-size:60px;
    }

    footer{
        padding:35px 20px;
        flex-direction:column;
        gap:15px;
        text-align:center;
    }

    .modal{
        padding:10px;
    }

    .modal-visual{
        min-height:260px;
    }

    .modal-content{
        padding:25px 20px 30px;
    }

    .modal-title{
        font-size:34px;
    }

    .modal-specs{
        grid-template-columns:1fr 1fr;
    }

}


/* reduced motion */

@media(prefers-reduced-motion:reduce){

    *,
    *::before,
    *::after{
        animation-duration:.01ms !important;
        animation-iteration-count:1 !important;
        transition-duration:.01ms !important;
    }

}

</style>
</head>


<body>

<div class="grid-bg"></div>
<div class="light one"></div>
<div class="light two"></div>


<!-- =====================================================
     HEADER
===================================================== -->

<header>

    <a href="#" class="logo">
        <div class="logo-dot"></div>
        SUPRA<span>STAR</span>
    </a>

    <nav id="nav">

        <a href="#home">Accueil</a>
        <a href="#fleet">Flotte</a>
        <a href="#services">Services</a>
        <a href="#contact">Contact</a>

    </nav>

    <button class="menu-btn" id="menuBtn">
        ☰
    </button>

</header>


<!-- =====================================================
     HERO
===================================================== -->

<main>

<section class="hero" id="home">

    <div class="hero-content">

        <div class="eyebrow">
            Luxury Car Rental · Salé · Morocco
        </div>

        <h1>
            DRIVE
            <span>YOUR STYLE.</span>
        </h1>

        <p class="hero-sub">
            Découvrez une expérience automobile premium.
            Des véhicules élégants, sportifs et prestigieux
            pour transformer chaque trajet en expérience.
        </p>

        <div class="hero-buttons">

            <a href="#fleet" class="btn gold">
                Explorer la flotte
            </a>

            <a href="#contact" class="btn outline">
                Nous contacter
            </a>

        </div>

    </div>

    <div class="hero-car"></div>

</section>


<!-- =====================================================
     STATS
===================================================== -->

<div class="stats">

    <div class="stat">
        <strong>24/7</strong>
        <span>Disponibilité</span>
    </div>

    <div class="stat">
        <strong>SALE</strong>
        <span>Maroc</span>
    </div>

    <div class="stat">
        <strong>VIP</strong>
        <span>Expérience Premium</span>
    </div>

</div>


<!-- =====================================================
     FLEET
===================================================== -->

<section id="fleet">

    <div class="section-head">

        <div class="section-title">

            <small>Notre sélection</small>

            <h2>La Flotte.</h2>

        </div>

        <p class="section-description">
            Une sélection de véhicules premium pour tous les styles,
            du SUV familial à la sportive.
        </p>

    </div>


    <!-- FILTERS -->

    <div class="filters">

        <button class="filter active" data-filter="all">
            Toutes
        </button>

        <button class="filter" data-filter="luxury">
            Luxe
        </button>

        <button class="filter" data-filter="suv">
            SUV
        </button>

        <button class="filter" data-filter="sport">
            Sport
        </button>

        <button class="filter" data-filter="compact">
            Compact
        </button>

        <button class="filter" data-filter="cabriolet">
            Cabriolet
        </button>

        <button class="filter" data-filter="supercar">
            Supercar
        </button>

    </div>


    <!-- CARS -->

    <div class="cars">


        <!-- 01 -->

        <article class="car reveal"
            data-category="luxury"
            data-name="BMW 7 Series"
            data-category-name="Luxury"
            data-description="Une berline premium pensée pour offrir confort, élégance et technologie."
            data-seats="5 places"
            data-transmission="Automatique"
            data-fuel="Essence"
            data-ac="Climatisation"
            data-image="https://images.unsplash.com/photo-1555215695-3004980ad54e?auto=format&fit=crop&w=1200&q=85">

            <span class="badge">DEMO</span>

            <div class="car-image">
                <img src="https://images.unsplash.com/photo-1555215695-3004980ad54e?auto=format&fit=crop&w=1200&q=85" alt="BMW 7 Series">
            </div>

            <div class="car-info">

                <div class="car-category">Luxury</div>

                <h3 class="car-name">BMW 7 Series</h3>

                <div class="car-specs">
                    <span class="spec">5 Places</span>
                    <span class="spec">Auto</span>
                    <span class="spec">Premium</span>
                </div>

                <div class="car-footer">
                    <span class="details">Voir détails</span>
                    <span class="arrow">↗</span>
                </div>

            </div>

        </article>


        <!-- 02 -->

        <article class="car reveal"
            data-category="luxury"
            data-name="Mercedes-Benz S-Class"
            data-category-name="Luxury"
            data-description="Une référence dans le monde des berlines haut de gamme."
            data-seats="5 places"
            data-transmission="Automatique"
            data-fuel="Essence"
            data-ac="Climatisation"
            data-image="https://images.unsplash.com/photo-1618843479313-40f8afb4b4d8?auto=format&fit=crop&w=1200&q=85">

            <span class="badge">DEMO</span>

            <div class="car-image">
                <img src="https://images.unsplash.com/photo-1618843479313-40f8afb4b4d8?auto=format&fit=crop&w=1200&q=85" alt="Mercedes S Class">
            </div>

            <div class="car-info">

                <div class="car-category">Luxury</div>

                <h3 class="car-name">Mercedes S-Class</h3>

                <div class="car-specs">
                    <span class="spec">5 Places</span>
                    <span class="spec">Auto</span>
                    <span class="spec">VIP</span>
                </div>

                <div class="car-footer">
                    <span class="details">Voir détails</span>
                    <span class="arrow">↗</span>
                </div>

            </div>

        </article>


        <!-- 03 -->

        <article class="car reveal"
            data-category="luxury"
            data-name="Mercedes E-Class"
            data-category-name="Luxury"
            data-description="Élégance moderne et confort premium pour vos déplacements."
            data-seats="5 places"
            data-transmission="Automatique"
            data-fuel="Essence"
            data-ac="Climatisation"
            data-image="https://images.unsplash.com/photo-1563720223185-11003d516935?auto=format&fit=crop&w=1200&q=85">

            <span class="badge">DEMO</span>

            <div class="car-image">
                <img src="https://images.unsplash.com/photo-1563720223185-11003d516935?auto=format&fit=crop&w=1200&q=85" alt="Mercedes E Class">
            </div>

            <div class="car-info">

                <div class="car-category">Luxury</div>

                <h3 class="car-name">Mercedes E-Class</h3>

                <div class="car-specs">
                    <span class="spec">5 Places</span>
                    <span class="spec">Auto</span>
                    <span class="spec">Comfort</span>
                </div>

                <div class="car-footer">
                    <span class="details">Voir détails</span>
                    <span class="arrow">↗</span>
                </div>

            </div>

        </article>


        <!-- 04 -->

        <article class="car reveal"
            data-category="luxury"
            data-name="BMW 5 Series"
            data-category-name="Luxury"
            data-description="Une berline sportive et élégante adaptée aux trajets urbains et professionnels."
            data-seats="5 places"
            data-transmission="Automatique"
            data-fuel="Essence"
            data-ac="Climatisation"
            data-image="https://images.unsplash.com/photo-1523983254938-9d5f3e1f8f6f?auto=format&fit=crop&w=1200&q=85">

            <span class="badge">DEMO</span>

            <div class="car-image">
                <img src="https://images.unsplash.com/photo-1523983254938-9d5f3e1f8f6f?auto=format&fit=crop&w=1200&q=85" alt="BMW 5 Series">
            </div>

            <div class="car-info">

                <div class="car-category">Luxury</div>

                <h3 class="car-name">BMW 5 Series</h3>

                <div class="car-specs">
                    <span class="spec">5 Places</span>
                    <span class="spec">Auto</span>
                    <span class="spec">Premium</span>
                </div>

                <div class="car-footer">
                    <span class="details">Voir détails</span>
                    <span class="arrow">↗</span>
                </div>

            </div>

        </article>


        <!-- 05 -->

        <article class="car reveal"
            data-category="suv"
            data-name="Range Rover"
            data-category-name="Luxury SUV"
            data-description="Le SUV premium iconique pour voyager avec style et confort."
            data-seats="5 places"
            data-transmission="Automatique"
            data-fuel="Diesel"
            data-ac="Climatisation"
            data-image="https://images.unsplash.com/photo-1606664515524-ed2f786a0bd6?auto=format&fit=crop&w=1200&q=85">

            <span class="badge">DEMO</span>

            <div class="car-image">
                <img src="https://images.unsplash.com/photo-1606664515524-ed2f786a0bd6?auto=format&fit=crop&w=1200&q=85" alt="Range Rover">
            </div>

            <div class="car-info">

                <div class="car-category">Luxury SUV</div>

                <h3 class="car-name">Range Rover</h3>

                <div class="car-specs">
                    <span class="spec">5 Places</span>
                    <span class="spec">Auto</span>
                    <span class="spec">4x4</span>
                </div>

                <div class="car-footer">
                    <span class="details">Voir détails</span>
                    <span class="arrow">↗</span>
                </div>

            </div>

        </article>


        <!-- 06 -->

        <article class="car reveal"
            data-category="suv"
            data-name="Range Rover Sport"
            data-category-name="Sport SUV"
            data-description="Un SUV dynamique combinant performances, présence et confort."
            data-seats="5 places"
            data-transmission="Automatique"
            data-fuel="Essence"
            data-ac="Climatisation"
            data-image="https://images.unsplash.com/photo-1533473359331-0135ef1b58bf?auto=format&fit=crop&w=1200&q=85">

            <span class="badge">DEMO</span>

            <div class="car-image">
                <img src="https://images.unsplash.com/photo-1533473359331-0135ef1b58bf?auto=format&fit=crop&w=1200&q=85" alt="Range Rover Sport">
            </div>

            <div class="car-info">

                <div class="car-category">Sport SUV</div>

                <h3 class="car-name">Range Rover Sport</h3>

                <div class="car-specs">
                    <span class="spec">5 Places</span>
                    <span class="spec">Auto</span>
                    <span class="spec">4x4</span>
                </div>

                <div class="car-footer">
                    <span class="details">Voir détails</span>
                    <span class="arrow">↗</span>
                </div>

            </div>

        </article>


        <!-- 07 -->

        <article class="car reveal"
            data-category="suv"
            data-name="BMW X5"
            data-category-name="SUV"
            data-description="Un SUV premium polyvalent, confortable et puissant."
            data-seats="5 places"
            data-transmission="Automatique"
            data-fuel="Diesel"
            data-ac="Climatisation"
            data-image="https://images.unsplash.com/photo-1556189250-72ba954cfc2b?auto=format&fit=crop&w=1200&q=85">

            <span class="badge">DEMO</span>

            <div class="car-image">
                <img src="https://images.unsplash.com/photo-1556189250-72ba954cfc2b?auto=format&fit=crop&w=1200&q=85" alt="BMW X5">
            </div>

            <div class="car-info">

                <div class="car-category">SUV</div>

                <h3 class="car-name">BMW X5</h3>

                <div class="car-specs">
                    <span class="spec">5 Places</span>
                    <span class="spec">Auto</span>
                    <span class="spec">SUV</span>
                </div>

                <div class="car-footer">
                    <span class="details">Voir détails</span>
                    <span class="arrow">↗</span>
                </div>

            </div>

        </article>


        <!-- 08 -->

        <article class="car reveal"
            data-category="suv"
            data-name="BMW X7"
            data-category-name="Luxury SUV"
            data-description="Grand SUV premium conçu pour les voyages confortables."
            data-seats="7 places"
            data-transmission="Automatique"
            data-fuel="Essence"
            data-ac="Climatisation"
            data-image="https://images.unsplash.com/photo-1519641471654-76ce0107ad1b?auto=format&fit=crop&w=1200&q=85">

            <span class="badge">DEMO</span>

            <div class="car-image">
                <img src="https://images.unsplash.com/photo-1519641471654-76ce0107ad1b?auto=format&fit=crop&w=1200&q=85" alt="BMW X7">
            </div>

            <div class="car-info">

                <div class="car-category">Luxury SUV</div>

                <h3 class="car-name">BMW X7</h3>

                <div class="car-specs">
                    <span class="spec">7 Places</span>
                    <span class="spec">Auto</span>
                    <span class="spec">4x4</span>
                </div>

                <div class="car-footer">
                    <span class="details">Voir détails</span>
                    <span class="arrow">↗</span>
                </div>

            </div>

        </article>


        <!-- 09 -->

        <article class="car reveal"
            data-category="suv"
            data-name="Mercedes GLE"
            data-category-name="Luxury SUV"
            data-description="SUV premium Mercedes offrant confort et technologie."
            data-seats="5 places"
            data-transmission="Automatique"
            data-fuel="Diesel"
            data-ac="Climatisation"
            data-image="https://images.unsplash.com/photo-1606664515524-ed2f786a0bd6?auto=format&fit=crop&w=1200&q=85">

            <span class="badge">DEMO</span>

            <div class="car-image">
                <img src="https://images.unsplash.com/photo-1606664515524-ed2f786a0bd6?auto=format&fit=crop&w=1200&q=85" alt="Mercedes GLE">
            </div>

            <div class="car-info">

                <div class="car-category">Luxury SUV</div>

                <h3 class="car-name">Mercedes GLE</h3>

                <div class="car-specs">
                    <span class="spec">5 Places</span>
                    <span class="spec">Auto</span>
                    <span class="spec">4x4</span>
                </div>

                <div class="car-footer">
                    <span class="details">Voir détails</span>
                    <span class="arrow">↗</span>
                </div>

            </div>

        </article>


        <!-- 10 -->

        <article class="car reveal"
            data-category="suv"
            data-name="Mercedes G-Class"
            data-category-name="Iconic SUV"
            data-description="Une silhouette légendaire avec une présence incomparable."
            data-seats="5 places"
            data-transmission="Automatique"
            data-fuel="Essence"
            data-ac="Climatisation"
            data-image="https://images.unsplash.com/photo-1520031441872-265e4ff70366?auto=format&fit=crop&w=1200&q=85">

            <span class="badge">DEMO</span>

            <div class="car-image">
                <img src="https://images.unsplash.com/photo-1520031441872-265e4ff70366?auto=format&fit=crop&w=1200&q=85" alt="Mercedes G Class">
            </div>

            <div class="car-info">

                <div class="car-category">Iconic SUV</div>

                <h3 class="car-name">Mercedes G-Class</h3>

                <div class="car-specs">
                    <span class="spec">5 Places</span>
                    <span class="spec">Auto</span>
                    <span class="spec">4x4</span>
                </div>

                <div class="car-footer">
                    <span class="details">Voir détails</span>
                    <span class="arrow">↗</span>
                </div>

            </div>

        </article>


        <!-- 11 -->

        <article class="car reveal"
            data-category="sport"
            data-name="Porsche 911"
            data-category-name="Sport"
            data-description="Une sportive emblématique conçue pour une expérience de conduite exceptionnelle."
            data-seats="2 places"
            data-transmission="Automatique"
            data-fuel="Essence"
            data-ac="Climatisation"
            data-image="https://images.unsplash.com/photo-1503376780353-7e6692767b70?auto=format&fit=crop&w=1200&q=85">

            <span class="badge">DEMO</span>

            <div class="car-image">
                <img src="https://images.unsplash.com/photo-1503376780353-7e6692767b70?auto=format&fit=crop&w=1200&q=85" alt="Porsche 911">
            </div>

            <div class="car-info">

                <div class="car-category">Sport</div>

                <h3 class="car-name">Porsche 911</h3>

                <div class="car-specs">
                    <span class="spec">2 Places</span>
                    <span class="spec">Auto</span>
                    <span class="spec">Sport</span>
                </div>

                <div class="car-footer">
                    <span class="details">Voir détails</span>
                    <span class="arrow">↗</span>
                </div>

            </div>

        </article>


        <!-- 12 -->

        <article class="car reveal"
            data-category="suv"
            data-name="Porsche Cayenne"
            data-category-name="Sport SUV"
            data-description="Un SUV Porsche combinant performance sportive et polyvalence."
            data-seats="5 places"
            data-transmission="Automatique"
            data-fuel="Essence"
            data-ac="Climatisation"
            data-image="https://images.unsplash.com/photo-1544829099-b9a0c07fad1a?auto=format&fit=crop&w=1200&q=85">

            <span class="badge">DEMO</span>

            <div class="car-image">
                <img src="https://images.unsplash.com/photo-1544829099-b9a0c07fad1a?auto=format&fit=crop&w=1200&q=85" alt="Porsche Cayenne">
            </div>

            <div class="car-info">

                <div class="car-category">Sport SUV</div>

                <h3 class="car-name">Porsche Cayenne</h3>

                <div class="car-specs">
                    <span class="spec">5 Places</span>
                    <span class="spec">Auto</span>
                    <span class="spec">Sport</span>
                </div>

                <div class="car-footer">
                    <span class="details">Voir détails</span>
                    <span class="arrow">↗</span>
                </div>

            </div>

        </article>


        <!-- 13 -->

        <article class="car reveal"
            data-category="sport"
            data-name="Audi RS"
            data-category-name="Sport"
            data-description="Performance allemande et design agressif pour les passionnés."
            data-seats="5 places"
            data-transmission="Automatique"
            data-fuel="Essence"
            data-ac="Climatisation"
            data-image="https://images.unsplash.com/photo-1606664515524-ed2f786a0bd6?auto=format&fit=crop&w=1200&q=85">

            <span class="badge">DEMO</span>

            <div class="car-image">
                <img src="https://images.unsplash.com/photo-1606664515524-ed2f786a0bd6?auto=format&fit=crop&w=1200&q=85" alt="Audi RS">
            </div>

            <div class="car-info">

                <div class="car-category">Sport</div>

                <h3 class="car-name">Audi RS</h3>

                <div class="car-specs">
                    <span class="spec">5 Places</span>
                    <span class="spec">Auto</span>
                    <span class="spec">Sport</span>
                </div>

                <div class="car-footer">
                    <span class="details">Voir détails</span>
                    <span class="arrow">↗</span>
                </div>

            </div>

        </article>


        <!-- 14 -->

        <article class="car reveal"
            data-category="sport"
            data-name="BMW M4"
            data-category-name="Sport"
            data-description="Coupé sportif BMW combinant design agressif et sensations."
            data-seats="4 places"
            data-transmission="Automatique"
            data-fuel="Essence"
            data-ac="Climatisation"
            data-image="https://images.unsplash.com/photo-1556189250-72ba954cfc2b?auto=format&fit=crop&w=1200&q=85">

            <span class="badge">DEMO</span>

            <div class="car-image">
                <img src="https://images.unsplash.com/photo-1556189250-72ba954cfc2b?auto=format&fit=crop&w=1200&q=85" alt="BMW M4">
            </div>

            <div class="car-info">

                <div class="car-category">Sport</div>

                <h3 class="car-name">BMW M4</h3>

                <div class="car-specs">
                    <span class="spec">4 Places</span>
                    <span class="spec">Auto</span>
                    <span class="spec">M Power</span>
                </div>

                <div class="car-footer">
                    <span class="details">Voir détails</span>
                    <span class="arrow">↗</span>
                </div>

            </div>

        </article>


        <!-- 15 -->

        <article class="car reveal"
            data-category="sport"
            data-name="Mercedes AMG"
            data-category-name="Sport"
            data-description="Mercedes AMG : puissance, luxe et caractère sportif."
            data-seats="5 places"
            data-transmission="Automatique"
            data-fuel="Essence"
            data-ac="Climatisation"
            data-image="https://images.unsplash.com/photo-1618843479313-40f8afb4b4d8?auto=format&fit=crop&w=1200&q=85">

            <span class="badge">DEMO</span>

            <div class="car-image">
                <img src="https://images.unsplash.com/photo-1618843479313-40f8afb4b4d8?auto=format&fit=crop&w=1200&q=85" alt="Mercedes AMG">
            </div>

            <div class="car-info">

                <div class="car-category">Sport</div>

                <h3 class="car-name">Mercedes AMG</h3>

                <div class="car-specs">
                    <span class="spec">5 Places</span>
                    <span class="spec">Auto</span>
                    <span class="spec">AMG</span>
                </div>

                <div class="car-footer">
                    <span class="details">Voir détails</span>
                    <span class="arrow">↗</span>
                </div>

            </div>

        </article>


        <!-- 16 -->

        <article class="car reveal"
            data-category="sport"
            data-name="Ford Mustang"
            data-category-name="Sport"
            data-description="Une icône américaine au caractère sportif et au design intemporel."
            data-seats="4 places"
            data-transmission="Automatique"
            data-fuel="Essence"
            data-ac="Climatisation"
            data-image="https://images.unsplash.com/photo-1584345604476-8ec5e12e42dd?auto=format&fit=crop&w=1200&q=85">

            <span class="badge">DEMO</span>

            <div class="car-image">
                <img src="https://images.unsplash.com/photo-1584345604476-8ec5e12e42dd?auto=format&fit=crop&w=1200&q=85" alt="Ford Mustang">
            </div>

            <div class="car-info">

                <div class="car-category">Sport</div>

                <h3 class="car-name">Ford Mustang</h3>

                <div class="car-specs">
                    <span class="spec">4 Places</span>
                    <span class="spec">Auto</span>
                    <span class="spec">V8</span>
                </div>

                <div class="car-footer">
                    <span class="details">Voir détails</span>
                    <span class="arrow">↗</span>
                </div>

            </div>

        </article>


        <!-- 17 -->

        <article class="car reveal"
            data-category="sport"
            data-name="Chevrolet Camaro"
            data-category-name="Sport"
            data-description="Muscle car américaine au style puissant et sportif."
            data-seats="4 places"
            data-transmission="Automatique"
            data-fuel="Essence"
            data-ac="Climatisation"
            data-image="https://images.unsplash.com/photo-1606664515524-ed2f786a0bd6?auto=format&fit=crop&w=1200&q=85">

            <span class="badge">DEMO</span>

            <div class="car-image">
                <img src="https://images.unsplash.com/photo-1606664515524-ed2f786a0bd6?auto=format&fit=crop&w=1200&q=85" alt="Chevrolet Camaro">
            </div>

            <div class="car-info">

                <div class="car-category">Sport</div>

                <h3 class="car-name">Chevrolet Camaro</h3>

                <div class="car-specs">
                    <span class="spec">4 Places</span>
                    <span class="spec">Auto</span>
                    <span class="spec">Sport</span>
                </div>

                <div class="car-footer">
                    <span class="details">Voir détails</span>
                    <span class="arrow">↗</span>
                </div>

            </div>

        </article>


        <!-- 18 -->

        <article class="car reveal"
            data-category="compact"
            data-name="Premium Compact"
            data-category-name="Compact"
            data-description="Un véhicule compact et élégant pour les déplacements urbains."
            data-seats="5 places"
            data-transmission="Automatique"
            data-fuel="Essence"
            data-ac="Climatisation"
            data-image="https://images.unsplash.com/photo-1502877338535-766e1452684a?auto=format&fit=crop&w=1200&q=85">

            <span class="badge">DEMO</span>

            <div class="car-image">
                <img src="https://images.unsplash.com/photo-1502877338535-766e1452684a?auto=format&fit=crop&w=1200&q=85" alt="Premium Compact">
            </div>

            <div class="car-info">

                <div class="car-category">Compact</div>

                <h3 class="car-name">Premium Compact</h3>

                <div class="car-specs">
                    <span class="spec">5 Places</span>
                    <span class="spec">Auto</span>
                    <span class="spec">City</span>
                </div>

                <div class="car-footer">
                    <span class="details">Voir détails</span>
                    <span class="arrow">↗</span>
                </div>

            </div>

        </article>


        <!-- 19 -->

        <article class="car reveal"
            data-category="cabriolet"
            data-name="Premium Cabrio"
            data-category-name="Cabriolet"
            data-description="Profitez de vos trajets avec une expérience cabriolet premium."
            data-seats="4 places"
            data-transmission="Automatique"
            data-fuel="Essence"
            data-ac="Climatisation"
            data-image="https://images.unsplash.com/photo-1511919884226-fd3cad34687c?auto=format&fit=crop&w=1200&q=85">

            <span class="badge">DEMO</span>

            <div class="car-image">
                <img src="https://images.unsplash.com/photo-1511919884226-fd3cad34687c?auto=format&fit=crop&w=1200&q=85" alt="Premium Cabrio">
            </div>

            <div class="car-info">

                <div class="car-category">Cabriolet</div>

                <h3 class="car-name">Premium Cabrio</h3>

                <div class="car-specs">
                    <span class="spec">4 Places</span>
                    <span class="spec">Auto</span>
                    <span class="spec">Open Top</span>
                </div>

                <div class="car-footer">
                    <span class="details">Voir détails</span>
                    <span class="arrow">↗</span>
                </div>

            </div>

        </article>


        <!-- 20 -->

        <article class="car reveal"
            data-category="supercar"
            data-name="Supercar"
            data-category-name="Supercar"
            data-description="Une expérience automobile spectaculaire pour les occasions spéciales."
            data-seats="2 places"
            data-transmission="Automatique"
            data-fuel="Essence"
            data-ac="Climatisation"
            data-image="https://images.unsplash.com/photo-1544829099-b9a0c07fad1a?auto=format&fit=crop&w=1200&q=85">

            <span class="badge">DEMO</span>

            <div class="car-image">
                <img src="https://images.unsplash.com/photo-1544829099-b9a0c07fad1a?auto=format&fit=crop&w=1200&q=85" alt="Supercar">
            </div>

            <div class="car-info">

                <div class="car-category">Supercar</div>

                <h3 class="car-name">Supercar</h3>

                <div class="car-specs">
                    <span class="spec">2 Places</span>
                    <span class="spec">Auto</span>
                    <span class="spec">Performance</span>
                </div>

                <div class="car-footer">
                    <span class="details">Voir détails</span>
                    <span class="arrow">↗</span>
                </div>

            </div>

        </article>


    </div>

</section>


<!-- =====================================================
     SERVICES
===================================================== -->

<section id="services">

    <div class="section-head">

        <div class="section-title">

            <small>Pourquoi nous</small>

            <h2>Service Premium.</h2>

        </div>

    </div>


    <div class="features">


        <div class="feature">

            <div class="feature-icon">
                ✦
            </div>

            <h3>Véhicules Premium</h3>

            <p>
                Une sélection pensée pour les clients qui recherchent
                confort, élégance et style.
            </p>

        </div>


        <div class="feature">

            <div class="feature-icon">
                ◉
            </div>

            <h3>Disponibilité</h3>

            <p>
                Un service flexible pour organiser votre location
                selon vos besoins.
            </p>

        </div>


        <div class="feature">

            <div class="feature-icon">
                ◆
            </div>

            <h3>Expérience VIP</h3>

            <p>
                Une expérience orientée vers le confort et la simplicité
                dès votre première demande.
            </p>

        </div>


    </div>

</section>


<!-- =====================================================
     CTA
===================================================== -->

<section id="contact" class="cta">

    <h2>
        Votre prochaine voiture
        vous attend.
    </h2>

    <p>
        Contactez Suprastar Cars pour connaître les véhicules
        disponibles et organiser votre réservation.
    </p>

    <a
        class="btn gold"
        href="https://wa.me/212661931760?text=Bonjour%20Suprastar%20Cars%2C%20je%20souhaite%20avoir%20des%20informations%20sur%20une%20location."
        target="_blank"
    >
        WhatsApp
    </a>

</section>


</main>


<!-- =====================================================
     FOOTER
===================================================== -->

<footer>

    <div class="footer-logo">
        SUPRA<span>STAR</span> CARS
    </div>

    <div>
        © 2026 Suprastar Cars · Salé, Maroc
    </div>

</footer>


<!-- =====================================================
     CAR MODAL
===================================================== -->

<div class="modal" id="carModal">

    <div class="modal-box">

        <button class="close-modal" id="closeModal">
            ×
        </button>


        <div class="modal-visual">

            <div class="door left"></div>
            <div class="door right"></div>

            <img
                id="modalCarImage"
                class="modal-car"
                src=""
                alt=""
            >

        </div>


        <div class="modal-content">

            <div
                id="modalCategory"
                class="modal-category"
            >
                Luxury
            </div>

            <h2
                id="modalTitle"
                class="modal-title"
            >
                BMW 7 Series
            </h2>

            <p
                id="modalDescription"
                class="modal-description"
            >
                Description.
            </p>


            <div class="modal-specs">

                <div class="modal-spec">

                    <small>Places</small>

                    <strong id="modalSeats">
                        5 places
                    </strong>

                </div>


                <div class="modal-spec">

                    <small>Transmission</small>

                    <strong id="modalTransmission">
                        Automatique
                    </strong>

                </div>


                <div class="modal-spec">

                    <small>Carburant</small>

                    <strong id="modalFuel">
                        Essence
                    </strong>

                </div>


                <div class="modal-spec">

                    <small>Confort</small>

                    <strong id="modalAc">
                        Climatisation
                    </strong>

                </div>

            </div>


            <a
                id="modalWhatsapp"
                class="whatsapp-btn"
                href="#"
                target="_blank"
            >
                Réserver sur WhatsApp
            </a>

        </div>

    </div>

</div>


<!-- =====================================================
     FLOATING WHATSAPP
===================================================== -->

<a
    class="whatsapp"
    href="https://wa.me/212661931760"
    target="_blank"
    aria-label="WhatsApp"
>
    ☎
</a>


<!-- =====================================================
     JAVASCRIPT
===================================================== -->

<script>

/* =========================================================
   MOBILE MENU
========================================================= */

const menuBtn = document.getElementById("menuBtn");
const nav = document.getElementById("nav");

menuBtn.addEventListener("click", () => {

    nav.classList.toggle("active");

});

document.querySelectorAll("nav a").forEach(link => {

    link.addEventListener("click", () => {

        nav.classList.remove("active");

    });

});


/* =========================================================
   SCROLL REVEAL
========================================================= */

const observer = new IntersectionObserver(

    entries => {

        entries.forEach(entry => {

            if(entry.isIntersecting){

                entry.target.classList.add("visible");

                observer.unobserve(entry.target);

            }

        });

    },

    {
        threshold:.08
    }

);

document.querySelectorAll(".reveal").forEach((card,index) => {

    card.style.transitionDelay = `${(index % 4) * 80}ms`;

    observer.observe(card);

});


/* =========================================================
   FILTER SYSTEM
========================================================= */

const filters = document.querySelectorAll(".filter");
const cars = document.querySelectorAll(".car");

filters.forEach(button => {

    button.addEventListener("click", () => {

        filters.forEach(btn => {
            btn.classList.remove("active");
        });

        button.classList.add("active");

        const selected = button.dataset.filter;

        cars.forEach((car,index) => {

            const category = car.dataset.category;

            if(
                selected === "all" ||
                category === selected
            ){

                car.style.display = "block";

                setTimeout(() => {
                    car.classList.add("visible");
                }, index * 40);

            }else{

                car.style.display = "none";

            }

        });

    });

});


/* =========================================================
   3D CARD TILT
========================================================= */

cars.forEach(card => {

    card.addEventListener("mousemove", event => {

        if(window.innerWidth < 800) return;

        const rect = card.getBoundingClientRect();

        const x =
            event.clientX - rect.left;

        const y =
            event.clientY - rect.top;

        const centerX =
            rect.width / 2;

        const centerY =
            rect.height / 2;

        const rotateX =
            ((y - centerY) / centerY) * -5;

        const rotateY =
            ((x - centerX) / centerX) * 5;

        card.style.setProperty(
            "--mouse-x",
            `${x}px`
        );

        card.style.setProperty(
            "--mouse-y",
            `${y}px`
        );

        card.style.transform =
            `perspective(1000px)
             rotateX(${rotateX}deg)
             rotateY(${rotateY}deg)
             translateY(-5px)`;

    });


    card.addEventListener("mouseleave", () => {

        card.style.transform =
            "perspective(1000px) rotateX(0) rotateY(0) translateY(0)";

    });

});


/* =========================================================
   MODAL
========================================================= */

const modal =
    document.getElementById("carModal");

const closeModal =
    document.getElementById("closeModal");

const modalImage =
    document.getElementById("modalCarImage");

const modalTitle =
    document.getElementById("modalTitle");

const modalCategory =
    document.getElementById("modalCategory");

const modalDescription =
    document.getElementById("modalDescription");

const modalSeats =
    document.getElementById("modalSeats");

const modalTransmission =
    document.getElementById("modalTransmission");

const modalFuel =
    document.getElementById("modalFuel");

const modalAc =
    document.getElementById("modalAc");

const modalWhatsapp =
    document.getElementById("modalWhatsapp");


/* OPEN MODAL */

cars.forEach(card => {

    card.addEventListener("click", () => {

        const name =
            card.dataset.name;

        const category =
            card.dataset.categoryName;

        const description =
            card.dataset.description;

        const seats =
            card.dataset.seats;

        const transmission =
            card.dataset.transmission;

        const fuel =
            card.dataset.fuel;

        const ac =
            card.dataset.ac;

        const image =
            card.dataset.image;


        modalTitle.textContent =
            name;

        modalCategory.textContent =
            category;

        modalDescription.textContent =
            description;

        modalSeats.textContent =
            seats;

        modalTransmission.textContent =
            transmission;

        modalFuel.textContent =
            fuel;

        modalAc.textContent =
            ac;

        modalImage.src =
            image;

        modalImage.alt =
            name;


        const message =
            `Bonjour Suprastar Cars, je suis intéressé par la ${name}. Je souhaite connaître la disponibilité et le tarif.`;

        modalWhatsapp.href =
            `https://wa.me/212661931760?text=${encodeURIComponent(message)}`;


        modal.classList.add("active");

        document.body.style.overflow =
            "hidden";

    });

});


/* CLOSE */

function closeCarModal(){

    modal.classList.remove("active");

    document.body.style.overflow =
        "";

}


closeModal.addEventListener(
    "click",
    closeCarModal
);


/* click outside */

modal.addEventListener("click", event => {

    if(event.target === modal){

        closeCarModal();

    }

});


/* ESC */

document.addEventListener("keydown", event => {

    if(event.key === "Escape"){

        closeCarModal();

    }

});


/* =========================================================
   PARALLAX HERO
========================================================= */

document.addEventListener("mousemove", event => {

    if(window.innerWidth < 800) return;

    const x =
        (event.clientX / window.innerWidth - .5);

    const y =
        (event.clientY / window.innerHeight - .5);


    const heroGlow =
        document.querySelector(".hero-car");

    if(heroGlow){

        heroGlow.style.transform =
            `translateX(-50%)
             translate(${x * 30}px,${y * 20}px)`;

    }

});


/* =========================================================
   DYNAMIC YEAR
========================================================= */

const yearElements =
    document.querySelectorAll("[data-year]");

yearElements.forEach(element => {

    element.textContent =
        new Date().getFullYear();

});


/* =========================================================
   PREVENT IMAGE DRAG
========================================================= */

document.querySelectorAll("img").forEach(img => {

    img.addEventListener(
        "dragstart",
        event => event.preventDefault()
    );

});

</script>

</body>
</html>
