<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>BL&A Transportes SPA</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Poppins',sans-serif;
}

html{
    scroll-behavior:smooth;
}

body{
    background:#0b0b0b;
    color:white;
    overflow-x:hidden;
}

/* SCROLLBAR */

::-webkit-scrollbar{
    width:10px;
}

::-webkit-scrollbar-thumb{
    background:#39d12f;
    border-radius:10px;
}

/* NAVBAR */

header{
    position:fixed;
    width:100%;
    top:0;
    z-index:1000;
    background:rgba(0,0,0,0.55);
    backdrop-filter:blur(14px);
    border-bottom:1px solid rgba(255,255,255,0.08);
}

.navbar{
    width:90%;
    margin:auto;
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:20px 0;
}

.logo{
    font-size:34px;
    font-weight:800;
    letter-spacing:1px;
}

.logo span{
    color:#39d12f;
}

.nav-links{
    display:flex;
    gap:35px;
}

.nav-links a{
    color:white;
    text-decoration:none;
    transition:.3s;
    font-size:15px;
    position:relative;
}

.nav-links a::after{
    content:'';
    position:absolute;
    width:0%;
    height:2px;
    background:#39d12f;
    left:0;
    bottom:-6px;
    transition:.3s;
}

.nav-links a:hover::after{
    width:100%;
}

.nav-links a:hover{
    color:#39d12f;
}

/* HERO */

.hero{
    height:100vh;
    background:
    linear-gradient(rgba(0,0,0,.72), rgba(0,0,0,.86)),
    url('https://cdn.pixabay.com/photo/2019/03/03/21/44/cars-4032928_1280.jpg');

    background-size:cover;
    background-position:center;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
    position:relative;
    overflow:hidden;
}

.hero::before{
    content:'';
    position:absolute;
    width:500px;
    height:500px;
    background:#39d12f;
    filter:blur(180px);
    opacity:.15;
    border-radius:50%;
    top:-150px;
    right:-100px;
}

.hero::after{
    content:'';
    position:absolute;
    width:400px;
    height:400px;
    background:#39d12f;
    filter:blur(180px);
    opacity:.1;
    border-radius:50%;
    bottom:-150px;
    left:-100px;
}

.hero-content{
    max-width:950px;
    z-index:10;
    padding:20px;
}

.hero h1{
    font-size:60px;
    line-height:1.1;
    margin-bottom:25px;
    font-weight:800;
}

.hero h1 span{
    color:#39d12f;
}

.hero p{
    font-size:22px;
    color:#d0d0d0;
    line-height:1.8;
    margin-bottom:45px;
}

.hero-buttons{
    display:flex;
    justify-content:center;
    gap:20px;
    flex-wrap:wrap;
}

.btn{
    padding:17px 38px;
    border-radius:12px;
    text-decoration:none;
    font-weight:600;
    transition:.3s;
}

.btn-primary{
    background:#39d12f;
    color:white;
    box-shadow:0 0 30px rgba(57,209,47,.35);
}

.btn-primary:hover{
    transform:translateY(-4px);
    background:#2fac26;
}

.btn-secondary{
    border:1px solid rgba(255,255,255,0.25);
    color:white;
    background:rgba(255,255,255,0.05);
    backdrop-filter:blur(10px);
}

.btn-secondary:hover{
    background:white;
    color:black;
}

/* SECTION */

.section{
    padding:120px 8%;
}

.section-title{
    text-align:center;
    margin-bottom:70px;
}

.section-title h2{
    font-size:52px;
    margin-bottom:15px;
    color:#39d12f;
}

.section-title p{
    color:#a9a9a9;
    max-width:700px;
    margin:auto;
    line-height:1.8;
}

/* SERVICES */

.services-grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
    gap:30px;
}

.service-card{
    background:rgba(255,255,255,0.03);
    border:1px solid rgba(255,255,255,0.08);
    backdrop-filter:blur(10px);
    padding:40px;
    border-radius:24px;
    transition:.4s;
    position:relative;
    overflow:hidden;
}

.service-card::before{
    content:'';
    position:absolute;
    width:180px;
    height:180px;
    background:#39d12f;
    border-radius:50%;
    filter:blur(90px);
    opacity:0;
    top:-60px;
    right:-60px;
    transition:.4s;
}

.service-card:hover::before{
    opacity:.15;
}

.service-card:hover{
    transform:translateY(-12px);
    border-color:#39d12f;
}

.service-card h3{
    font-size:26px;
    margin-bottom:20px;
    color:#39d12f;
}

.service-card p{
    color:#d5d5d5;
    line-height:1.8;
}

/* STATS */

.stats{
    background:#111;
}

.stats-grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
    gap:30px;
}

.stat-card{
    text-align:center;
    background:#181818;
    padding:45px;
    border-radius:22px;
}

.stat-card h2{
    font-size:55px;
    color:#39d12f;
    margin-bottom:10px;
}

.stat-card p{
    color:#c5c5c5;
}

/* ABOUT */

.about{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:70px;
    align-items:center;
}

.about img{
    width:100%;
    border-radius:24px;
}

.about-text h2{
    font-size:50px;
    color:#39d12f;
    margin-bottom:25px;
}

.about-text p{
    color:#d0d0d0;
    line-height:2;
    margin-bottom:20px;
}

/* CONTACT */

.contact{
    background:#101010;
}

.contact-container{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:50px;
}

.contact-info{
    background:#181818;
    padding:45px;
    border-radius:24px;
}

.contact-info h3{
    color:#39d12f;
    margin-bottom:25px;
    font-size:32px;
}

.contact-info p{
    color:#d3d3d3;
    margin-bottom:18px;
}

form{
    display:flex;
    flex-direction:column;
    gap:20px;
}

input, textarea{
    padding:18px;
    background:#1a1a1a;
    border:1px solid rgba(255,255,255,0.08);
    border-radius:14px;
    color:white;
    font-size:15px;
}

textarea{
    min-height:160px;
    resize:none;
}

button{
    background:#39d12f;
    border:none;
    padding:18px;
    color:white;
    border-radius:14px;
    cursor:pointer;
    font-weight:600;
    transition:.3s;
    font-size:16px;
}

button:hover{
    background:#2fac26;
}

/* FOOTER */

footer{
    padding:35px;
    text-align:center;
    background:black;
    color:#888;
}

/* WHATSAPP */

.whatsapp{
    position:fixed;
    right:25px;
    bottom:25px;
    width:70px;
    height:70px;
    border-radius:50%;
    background:#25D366;
    color:white;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:32px;
    text-decoration:none;
    box-shadow:0 0 30px rgba(0,0,0,.4);
    z-index:1000;
}

/* RESPONSIVE */

@media(max-width:950px){

    .hero h1{
        font-size:52px;
    }

    .hero p{
        font-size:18px;
    }

    .about,
    .contact-container{
        grid-template-columns:1fr;
    }

    .nav-links{
        display:none;
    }
}

</style>
</head>

<body>

<header>

<div class="navbar">

<div class="logo">
BL&<span>A</span>
</div>

<div class="nav-links">
<a href="#inicio">Inicio</a>
<a href="#servicios">Servicios</a>
<a href="#nosotros">Nosotros</a>
<a href="#contacto">Contacto</a>
</div>

</div>

</header>

<!-- HERO -->

<section class="hero" id="inicio">

<div class="hero-content">

<h1>
Transportamos <span>Confianza</span><br>
Conectamos Personas
</h1>

<p>
Servicios de transporte corporativo y logística operacional
con altos estándares de seguridad, puntualidad y profesionalismo.
</p>

<div class="hero-buttons">

<a href="#contacto" class="btn btn-primary">
Solicitar Cotización
</a>

<a href="https://wa.me/56936387748" class="btn btn-secondary">
WhatsApp
</a>

</div>

</div>

</section>

<!-- SERVICIOS -->

<section class="section" id="servicios">

<div class="section-title">

<h2>Nuestros Servicios</h2>

<p>
Soluciones integrales de transporte y logística
adaptadas a empresas modernas.
</p>

</div>

<div class="services-grid">

<div class="service-card">
<h3>Transporte de Personal</h3>
<p>
Traslado eficiente y seguro para trabajadores,
empresas, oficinas y operaciones.
</p>
</div>

<div class="service-card">
<h3>Servicios Ejecutivos</h3>
<p>
Movilización privada para gerencias,
eventos y clientes corporativos.
</p>
</div>

<div class="service-card">
<h3>Logística Operacional</h3>
<p>
Coordinación de rutas, conductores
y planificación operacional.
</p>
</div>

</div>

</section>

<!-- STATS -->

<section class="section stats">

<div class="stats-grid">

<div class="stat-card">
<h2>24/7</h2>
<p>Soporte Operacional</p>
</div>

<div class="stat-card">
<h2>100%</h2>
<p>Compromiso y Seguridad</p>
</div>

<div class="stat-card">
<h2>+500</h2>
<p>Servicios Realizados</p>
</div>

<div class="stat-card">
<h2>+100</h2>
<p>Clientes Satisfechos</p>
</div>

</div>

</section>

<!-- NOSOTROS -->

<section class="section" id="nosotros">

<div class="about">

<img src="https://cdn.pixabay.com/photo/2013/03/22/16/38/auto-95824_1280.jpg">

<div class="about-text">

<h2>BL&A Transportes SPA</h2>

<p>
Somos una empresa enfocada en entregar soluciones
de transporte corporativo y logística empresarial
con un enfoque moderno, seguro y eficiente.
</p>

<p>
Nuestro compromiso es brindar un servicio profesional,
puntual y confiable para empresas y personas
en todo Chile.
</p>

<a href="#contacto" class="btn btn-primary">
Contactar Empresa
</a>

</div>

</div>

</section>

<!-- CONTACTO -->

<section class="section contact" id="contacto">

<div class="section-title">

<h2>Contáctanos</h2>

<p>
Solicita información o una cotización personalizada.
</p>

</div>

<div class="contact-container">

<div class="contact-info">

<h3>BL&A Transportes SPA</h3>

<p>📍 Todo Chile Chile</p>
<p>📞 +56 9 3638 7748</p>
<p>✉ blatransportesspa@gmail.cl</p>
<p>🕒 Atención 24/7</p>

</div>

<form action="https://formsubmit.co/blatransportesspa@gmail.com" method="POST">

    <input type="text" name="nombre" placeholder="Tu nombre" required>
    <input type="text" name="Empresa" placeholder="Tu Empresa" required>
    <input type="email" name="email" placeholder="Tu correo" required>

    <textarea name="mensaje" placeholder="Escribe tu solicitud" required></textarea>

    <!-- Evita spam -->
    <input type="hidden" name="_captcha" value="false">

    <!-- Redirección después de enviar -->
    <input type="hidden" name="_next" value="https://tupagina.cl/gracias.html">

    <button type="submit">
        Enviar Solicitud
    </button>

</form>

</div>

</section>

<footer>

© 2026 BL&A Transportes SPA | Todos los derechos reservados.

</footer>

<a class="whatsapp" href="https://wa.me/56936387748">
☎
</a>

</body>
</html>
