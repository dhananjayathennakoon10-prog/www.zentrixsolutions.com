<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Zentrix Solutions</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>
/* ================= RESET ================= */
*{margin:0;padding:0;box-sizing:border-box;}
html{scroll-behavior:smooth;}
body{
  font-family:'Poppins',sans-serif;
  background:#f8fafc;
  color:#0f172a;
  overflow-x:hidden;
  transition:0.3s;
}
body.dark{
  background:#020617;
  color:#e5e7eb;
}

/* ================= BLUR ANIMATION ================= */
.blur-bg{position:fixed;inset:0;z-index:-1;overflow:hidden;}
.blur-bg span{
  position:absolute;
  width:420px;height:420px;
  border-radius:50%;
  filter:blur(120px);
  opacity:.9;
  background:radial-gradient(circle,rgba(56,189,248,1),rgba(59,130,246,.9),transparent);
  animation:drift 12s linear infinite;
}
.blur-bg span:nth-child(1){top:10%;left:-15%;}
.blur-bg span:nth-child(2){top:50%;right:-20%;animation-duration:14s;}
.blur-bg span:nth-child(3){bottom:-20%;left:35%;animation-duration:16s;}
@keyframes drift{from{transform:translate(0,0);}to{transform:translate(650px,350px);}}

/* ================= HEADER ================= */
header{
  position:fixed;
  top:18px;left:50%;
  transform:translateX(-50%);
  width:92%;max-width:1200px;
  padding:14px 28px;
  display:flex;align-items:center;
  border-radius:22px;
  background:rgba(255,255,255,.45);
  backdrop-filter:blur(14px);
  border:1px solid rgba(255,255,255,.35);
  z-index:1000;
}
body.dark header{background:rgba(2,6,23,.55);}

.logo{
  cursor:pointer;
}
.logo .big{
  font-size:30px;font-weight:700;letter-spacing:2px;
  transition:.3s;
}
.logo:hover .big{
  text-shadow:0 0 25px #38bdf8;
}
.logo .small{
  font-size:13px;letter-spacing:4px;color:#64748b;
}

/* NAV */
nav{margin:0 auto;}
nav a{
  margin:0 16px;text-decoration:none;
  color:inherit;font-weight:500;
  position:relative;
}
nav a::after{
  content:"";position:absolute;left:0;bottom:-6px;
  width:0;height:2px;background:#38bdf8;transition:.3s;
}
nav a:hover::after{width:100%;}

/* TOGGLES */
.actions{display:flex;gap:14px;}
.toggle, .menu-btn{
  cursor:pointer;
  font-size:20px;
}

/* MOBILE MENU */
.mobile-menu{
  position:fixed;top:90px;left:50%;
  transform:translateX(-50%) scale(.9);
  width:90%;
  background:rgba(255,255,255,.55);
  backdrop-filter:blur(14px);
  border-radius:20px;
  text-align:center;
  padding:30px;
  display:none;
}
body.dark .mobile-menu{background:rgba(2,6,23,.65);}
.mobile-menu a{
  display:block;
  margin:18px 0;
  font-size:18px;
  text-decoration:none;
  color:inherit;
}

/* ================= SECTIONS ================= */
section{
  max-width:1000px;
  margin:160px auto;
  padding:80px 40px;
  background:rgba(255,255,255,.45);
  backdrop-filter:blur(14px);
  border-radius:28px;
  border:1px solid rgba(255,255,255,.35);
  box-shadow:0 20px 45px rgba(0,0,0,.08);
  text-align:center;
  opacity:0;
  transform:translateY(40px);
  transition:1s;
}
section.show{opacity:1;transform:none;}
body.dark section{background:rgba(2,6,23,.55);}

/* HERO */
.hero h1{font-size:48px;margin-bottom:15px;}
.hero p{font-size:18px;color:#64748b;}

/* BUTTON */
.btn{
  display:inline-block;margin-top:25px;
  padding:14px 40px;
  background:#38bdf8;color:#fff;
  border-radius:30px;
  text-decoration:none;font-weight:600;
  transition:.3s;
}
.btn:hover{transform:translateY(-6px);box-shadow:0 16px 40px rgba(56,189,248,.6);}

/* SERVICES */
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:30px;margin-top:40px;}
.card{
  padding:30px;border-radius:22px;
  background:rgba(255,255,255,.35);
  backdrop-filter:blur(12px);
  transition:.3s;
}
.card:hover{transform:translateY(-10px);box-shadow:0 18px 45px rgba(56,189,248,.35);}

/* CONTACT */
form input, form textarea{
  width:100%;padding:14px;
  margin:10px 0;border-radius:14px;
  border:none;font-family:inherit;
}
form button{
  margin-top:15px;
  padding:14px 36px;
  border:none;border-radius:30px;
  background:#38bdf8;color:#fff;
  font-weight:600;cursor:pointer;
}

/* FOOTER */
footer{text-align:center;padding:40px;color:#64748b;}

@media(max-width:768px){
  nav{display:none;}
  .menu-btn{display:block;}
  .hero h1{font-size:34px;}
}
</style>
</head>

<body>

<div class="blur-bg"><span></span><span></span><span></span></div>

<header>
  <div class="logo">
    <div class="big">ZENTRIX</div>
    <div class="small">SOLUTIONS</div>
  </div>

  <nav>
    <a href="#about">About</a>
    <a href="#services">Services</a>
    <a href="previos works.html">Previous Works</a>
    <a href="#contact">Contact</a>
  </nav>

  <div class="actions">
    <div class="toggle" onclick="toggleDark()">🌙</div>
    <div class="menu-btn" onclick="toggleMenu()">☰</div>
  </div>
</header>



<section class="hero show">
  <h1>Modern Web Development</h1>
  <p>Clean, glassy & animated websites</p>
  <a href="#contact" class="btn">Get Started</a>
</section>

<section id="about">
  <h2>About Us</h2>
  <p>Zentrix Solutions builds premium modern websites with smooth UI and animations.</p>
</section>

<section id="services">
  <h2>Our Services</h2>
  <div class="grid">
    <div class="card">Website Development</div>
    <div class="card">Landing Pages</div>
    <div class="card">E-Commerce</div>
    <div class="card">Redesign</div>
  </div>
</section>

<section id="contact">
  <h2>Contact Us</h2>
  <form onsubmit="sendWhatsApp(event)">
    <input type="text" id="name" placeholder="Your Name" required>
    <textarea id="msg" placeholder="Your Message" required></textarea>
    <button>Send via WhatsApp</button>
  </form>
</section>

<footer>© 2026 Zentrix Solutions</footer>

<script>
function toggleDark(){document.body.classList.toggle("dark");}
function toggleMenu(){
  const m=document.getElementById("menu");
  m.style.display=m.style.display==="block"?"none":"block";
}

/* section reveal */
const sections=document.querySelectorAll("section");
const obs=new IntersectionObserver(e=>{
  e.forEach(x=>x.isIntersecting&&x.target.classList.add("show"));
},{threshold:.2});
sections.forEach(s=>obs.observe(s));

/* WhatsApp */
function sendWhatsApp(e){
  e.preventDefault();
  const n=document.getElementById("name").value;
  const m=document.getElementById("msg").value;
  window.open(`https://wa.me/94704845611?text=Name:%20${n}%0A${m}`,"_blank");
}
</script>

</body>
</html>
