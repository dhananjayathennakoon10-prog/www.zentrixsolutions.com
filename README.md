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

.site-footer{
  margin:120px auto 40px;
  max-width:1100px;
  padding:60px 40px;
  text-align:center;
  background:rgba(255,255,255,.45);
  backdrop-filter:blur(14px);
  border-radius:28px;
  border:1px solid rgba(255,255,255,.35);
  box-shadow:0 20px 45px rgba(0,0,0,.08);
}

body.dark .site-footer{
  background:rgba(2,6,23,.55);
}

.site-footer h3{
  font-size:26px;
  letter-spacing:2px;
  margin-bottom:16px;
}

.footer-text{
  color:#64748b;
  font-size:16px;
  max-width:800px;
  margin:0 auto 24px;
  line-height:1.7;
}

.footer-details p{
  margin:6px 0;
  font-size:15px;
}

.footer-tagline{
  margin-top:24px;
  font-weight:600;
  color:#38bdf8;
}

.footer-bottom{
  margin-top:30px;
  font-size:14px;
  color:#64748b;
}

/* MOBILE */
@media(max-width:768px){
  .site-footer{
    padding:40px 24px;
  }
}

  /* ================= TEAM SECTION ================= */
.team-section{
  max-width:1100px;
  margin:140px auto 80px;
  padding:70px 30px;
  background:rgba(255,255,255,.45);
  backdrop-filter:blur(14px);
  border-radius:30px;
  border:1px solid rgba(255,255,255,.35);
  text-align:center;
}

body.dark .team-section{
  background:rgba(2,6,23,.6);
}

.team-title{
  font-size:36px;
  margin-bottom:12px;
}

.team-sub{
  font-size:16px;
  color:#64748b;
  max-width:650px;
  margin:0 auto 50px;
}

/* GRID */
.team-grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(160px,1fr));
  gap:35px;
}

/* CARD */
.team-card{
  padding:25px 15px;
  border-radius:22px;
  background:rgba(255,255,255,.35);
  backdrop-filter:blur(12px);
  transition:.35s;
}

body.dark .team-card{
  background:rgba(2,6,23,.55);
}

.team-card:hover{
  transform:translateY(-12px);
  box-shadow:0 18px 40px rgba(56,189,248,.35);
}

/* IMAGE */
.team-card img{
  width:120px;
  height:120px;
  object-fit:cover;
  border-radius:50%;
  margin-bottom:15px;
  border:4px solid #38bdf8;
}

/* TEXT */
.team-card h4{
  font-size:16px;
  margin-bottom:6px;
}

.team-card span{
  font-size:13px;
  color:#64748b;
}

/* ================= FOOTER ================= */
.site-footer{
  padding:60px 20px;
  text-align:center;
  background:rgba(255,255,255,.35);
  backdrop-filter:blur(12px);
  border-top:1px solid rgba(255,255,255,.3);
}

body.dark .site-footer{
  background:rgba(2,6,23,.65);
}

.footer-content h3{
  font-size:22px;
  margin-bottom:10px;
}

.footer-content p{
  font-size:14px;
  color:#64748b;
  margin-bottom:10px;
}

.footer-content span{
  font-size:13px;
  color:#64748b;
}

/* ================= MOBILE FIX ================= */
@media(max-width:768px){
  .team-title{font-size:28px;}
  .team-card img{
    width:95px;
    height:95px;
  }
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
    <a href="#contact">Contact</a>
  </nav>

  <div class="actions">
    <div class="toggle" onclick="toggleDark()">🌙</div>
    <div class="menu-btn" onclick="toggleMenu()">☰</div>
  </div>
</header>



<section class="hero show">
  <h1>Your Digital Growth Partner</h1>
  <p></p>
  <a href="#contact" class="btn">Get Started</a>
  <a href="previos works.html" class="btn">Previous Works</a>
</section>

<section id="about">
  <h2>About Us</h2>
  <p>We provide modern web development and AI-powered solutions designed to help businesses grow in the digital world.

Our work focuses on building fast, secure, and visually clean websites, along with intelligent AI systems that improve efficiency and automation. We believe in using the latest technologies to create smart, reliable, and user-friendly digital products.

At Zentrix Solutions, our goal is to deliver high-quality solutions, strong performance, and long-term value for our clients.</p>
</section>

<!-- ================= STATS COUNTER SECTION ================= -->
<section class="stats-section">

  <div class="stats-box">

    <div class="stat">
      <h2 class="count" data-target="1">0</h2>
      <p>Years of Operation</p>
    </div>

    <div class="stat">
      <h2 class="count" data-target="5">0</h2>
      <p>Worldwide Clients</p>
    </div>

    <div class="stat">
      <h2 class="count" data-target="20">0</h2>
      <p>Successful Projects</p>
    </div>

    <div class="stat">
      <h2 class="count" data-target="6">0</h2>
      <p>Developing Team</p>
    </div>

  </div>

</section>

<style>
/* ================= STATS SECTION ================= */
.stats-section{
  max-width:1100px;
  margin:120px auto;
  padding:20px;
}

.stats-box{
  background:#0f172a;
  border-radius:40px;
  padding:55px 30px;
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
  gap:20px;
  text-align:center;
  color:#fff;
}

/* STAT ITEM */
.stat h2{
  font-size:44px;
  font-weight:700;
  color:#38bdf8;
}

.stat p{
  margin-top:8px;
  font-size:14px;
  opacity:.8;
}

/* MOBILE */
@media(max-width:768px){
  .stats-box{
    border-radius:25px;
    padding:40px 20px;
  }
  .stat h2{
    font-size:34px;
  }
}
</style>

<script>
const counters = document.querySelectorAll('.count');
let started = false;

function startCounter(){
  if(started) return;
  counters.forEach(counter=>{
    const target = +counter.dataset.target;
    let current = 0;
    const step = target / 80;

    const update = () => {
      current += step;
      if(current < target){
        counter.innerText = Math.ceil(current);
        requestAnimationFrame(update);
      }else{
        counter.innerText = target + "+";
      }
    };
    update();
  });
  started = true;
}

/* START ON SCROLL */
const statsSection = document.querySelector('.stats-section');

const observer = new IntersectionObserver(entries=>{
  if(entries[0].isIntersecting){
    startCounter();
  }
},{threshold:0.4});

observer.observe(statsSection);
</script>





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


<!-- TEAM SECTION -->
<section class="team-section show">
  <h2 class="team-title">The Team Behind the Innovation</h2>
  <p class="team-sub">
    We are a hands-on team of designers, developers, and AI engineers
    building modern digital solutions.
  </p>

  <div class="team-grid">

    <div class="team-card">
      <img src="WhatsApp Image 2026-01-07 at 12.27.31 AM.jpeg">
      <h4>Dhananjaya Thennakoon</h4>
      <span>Founder</span>
    </div>

    <div class="team-card">
      <img src="1767770931976.jpg" alt="Senior Consultant">
      <h4>Adheesha Bandara</h4>
      <span>Senior Consultant</span>
    </div>

   <div class="team-card">
      <img src="WhatsApp Image 2026-01-08 at 1.52.27 PM.jpeg" alt="Web Designer/App Developer">
      <h4>Oshada Dilshan</h4>
      <span>Web Designer/App Developer</span>
    </div>

  <div class="team-card">
      <img src="WhatsApp Image 2026-01-08 at 2.22.03 PM.jpeg" alt="Project Manager">
      <h4>Nishitha Heshara</h4>
      <span>Project Manager</span>
    </div>

    <div class="team-card">
      <img src="WhatsApp Image 2026-01-08 at 3.24.48 PM.jpeg" alt="Graphic Designer"> 
      <h4>Vimukthi Lakruwan</h4>
      <span>Graphic Designer</span>
    </div>

  <div class="team-card">
      <img src="WhatsApp Image 2026-01-08 at 3.50.46 PM.jpeg" alt="Web Developer"> 
      <h4>Dishen Anjana</h4>
      <span>Web Developer</span>
    </div>
  
  </div>
</section>




<footer class="site-footer">
  <div class="footer-content">
    <h3>ZENTRIX SOLUTIONS</h3>

    <p class="footer-text">
      Co-founded by a passionate leadership team and supported by skilled web developers
      and AI specialists, Zentrix Solutions delivers modern, reliable, and high-quality
      digital solutions for businesses.
    </p>

    <div class="footer-details">
      <p><strong>Co-Founder:</strong> Dhananjaya Thennakoon</p>
      <p><strong>Team:</strong> Web Developers · UI/UX Designers · AI Engineers</p>
    </div>

    <p class="footer-tagline">
      Creating smart digital experiences for the future.
    </p>

    <div class="footer-bottom">
      © 2026 Zentrix Solutions. All rights reserved.
    </div>
  </div>
</footer>


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
