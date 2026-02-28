<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Portfolio - Soleil Ankouma</title>

<style>
*{
  margin:0;
  padding:0;
  box-sizing:border-box;
  font-family: Arial, Helvetica, sans-serif;
}

body{
  background: linear-gradient(-45deg,#0f172a,#1e293b,#0ea5e9,#0f172a);
  background-size:400% 400%;
  animation:gradientBG 12s ease infinite;
  color:white;
  scroll-behavior:smooth;
  transition:0.4s;
}

@keyframes gradientBG{
  0%{background-position:0% 50%;}
  50%{background-position:100% 50%;}
  100%{background-position:0% 50%;}
}

body.light{
  background:#f1f5f9;
  color:#111;
}

/* NAVIGATION */
nav{
  display:flex;
  justify-content:space-between;
  align-items:center;
  padding:15px 30px;
  background:rgba(0,0,0,0.6);
  position:sticky;
  top:0;
  backdrop-filter:blur(10px);
  z-index:1000;
}

nav .logo{
  font-weight:bold;
  font-size:22px;
}

nav ul{
  display:flex;
  list-style:none;
}

nav ul li{
  margin-left:20px;
}

nav a{
  text-decoration:none;
  color:white;
  font-weight:bold;
}

nav .toggle{
  display:none;
  cursor:pointer;
  background:#38bdf8;
  padding:8px 15px;
  border-radius:20px;
  color:black;
  font-weight:bold;
}

/* HERO */
.hero{
  text-align:center;
  padding:100px 20px;
}

.profile-pic{
  width:150px;
  height:150px;
  border-radius:50%;
  border:4px solid #38bdf8;
  margin-bottom:20px;
}

.typing{
  font-size:22px;
  color:#38bdf8;
  min-height:28px;
}

.btn{
  padding:12px 25px;
  background:#38bdf8;
  color:black;
  text-decoration:none;
  font-weight:bold;
  border-radius:30px;
  display:inline-block;
  margin-top:20px;
  transition:0.3s;
}

.btn:hover{
  transform:scale(1.1);
}

/* SECTIONS */
section{
  padding:60px 20px;
  text-align:center;
}

/* CARDS */
.card{
  background:rgba(255,255,255,0.1);
  padding:20px;
  margin:20px auto;
  width:90%;
  max-width:300px;
  border-radius:15px;
  transition:0.3s;
}

.card:hover{
  transform:translateY(-10px);
}

/* SKILLS */
.skill{
  margin:20px auto;
  width:90%;
  max-width:400px;
  text-align:left;
}

.bar{
  background:#334155;
  border-radius:20px;
  overflow:hidden;
}

.progress{
  height:12px;
  background:#38bdf8;
  width:0;
  transition:1.5s;
}

/* FORM */
form{
  display:flex;
  flex-direction:column;
  width:90%;
  max-width:350px;
  margin:auto;
}

form input, form textarea{
  margin:10px 0;
  padding:10px;
  border:none;
  border-radius:8px;
}

form button{
  padding:10px;
  background:#38bdf8;
  border:none;
  border-radius:20px;
  cursor:pointer;
  font-weight:bold;
}

/* FOOTER */
footer{
  padding:20px;
  text-align:center;
  font-size:14px;
}

/* RESPONSIVE MOBILE */
@media (max-width:768px){
  nav ul{
    position:fixed;
    top:0;
    right:-100%;
    height:100%;
    width:200px;
    background:rgba(0,0,0,0.95);
    flex-direction:column;
    padding-top:60px;
    transition:0.3s;
  }
  nav ul li{
    margin:20px 0;
    text-align:center;
  }
  nav ul.active{
    right:0;
  }
  nav .toggle{
    display:block;
  }
}
</style>

</head>
<body>

<nav>
  <div class="logo">Soleil</div>
  <ul>
    <li><a href="#home">Accueil</a></li>
    <li><a href="#skills">Compétences</a></li>
    <li><a href="#services">Services</a></li>
    <li><a href="#projects">Projets</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <div class="toggle" onclick="toggleMenu()">☰</div>
</nav>

<section id="home" class="hero">
  <img src="photo.jpg" class="profile-pic">
  <h1>Bonjour 👋 Je suis Soleil</h1>
  <div class="typing"></div>
  <a href="cv.pdf" class="btn" download>Télécharger mon CV</a>
</section>

<section id="skills">
<h2>Mes Compétences</h2>

<div class="skill">
  <p>HTML</p>
  <div class="bar"><div class="progress" data-width="90%"></div></div>
</div>

<div class="skill">
  <p>CSS</p>
  <div class="bar"><div class="progress" data-width="80%"></div></div>
</div>

<div class="skill">
  <p>JavaScript</p>
  <div class="bar"><div class="progress" data-width="60%"></div></div>
</div>
</section>

<section id="services">
<h2>Mes Services</h2>

<div class="card">
  <h3>Création de site web</h3>
  <p>Je crée des sites web modernes et responsives.</p>
</div>

<div class="card">
  <h3>Design simple et propre</h3>
  <p>Création de design clair, moderne et professionnel.</p>
</div>

<div class="card">
  <h3>Maintenance</h3>
  <p>Mise à jour et amélioration de site existant.</p>
</div>
</section>

<section id="projects">
<h2>Mes Projets</h2>

<div class="card">
  <img src="projet1.jpg" style="width:100%; border-radius:10px;">
  <h3>Portfolio Personnel</h3>
  <p>Site moderne publié sur GitHub Pages.</p>
</div>

<div class="card">
  <img src="projet2.jpg" style="width:100%; border-radius:10px;">
  <h3>Mini Application</h3>
  <p>Projet interactif en JavaScript.</p>
</div>
</section>

<section id="contact">
<h2>Contact</h2>

<p>Email : <a href="mailto:ankoumasoleil09@gmail.com">ankoumasoleil09@gmail.com</a></p>
<p>WhatsApp : <a href="https://wa.me/23672584404" target="_blank">Me contacter sur WhatsApp</a></p>
<p>GitHub : <a href="https://github.com/ankoumasoleil09-ops" target="_blank">Mon GitHub</a></p>

<form>
  <input type="text" placeholder="Votre nom" required>
  <input type="email" placeholder="Votre email" required>
  <textarea rows="4" placeholder="Votre message"></textarea>
  <button type="submit">Envoyer</button>
</form>
</section>

<footer>
© 2026 Soleil Ankouma | Portfolio Professionnel
</footer>

<script>
// MODE CLAIR / SOMBRE
function toggleMode(){
  document.body.classList.toggle("light");
}

// MENU BURGER MOBILE
function toggleMenu(){
  document.querySelector("nav ul").classList.toggle("active");
}

// MACHINE À ÉCRIRE
const text = "Développeur Web en apprentissage 🚀";
let i = 0;
function typing(){
  if(i < text.length){
    document.querySelector(".typing").innerHTML += text.charAt(i);
    i++;
    setTimeout(typing,70);
  }
}
typing();

// BARRES DE COMPETENCES ANIMEES
window.addEventListener("scroll", ()=>{
  document.querySelectorAll(".progress").forEach(bar=>{
    const position = bar.getBoundingClientRect().top;
    if(position < window.innerHeight){
      bar.style.width = bar.dataset.width;
    }
  });
});
</script>

</body>
</html>
