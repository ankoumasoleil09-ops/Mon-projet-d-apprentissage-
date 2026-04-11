<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mon Portfolio</title>

<style>
/* ===== BASE ===== */
body{
  margin:0;
  font-family:Arial;
  transition:0.3s;
}

.dark{
  background:#0f172a;
  color:white;
}

.light{
  background:white;
  color:black;
}

/* ===== HEADER ===== */
header{
  display:flex;
  justify-content:space-between;
  align-items:center;
  padding:15px;
  background:#020617;
  position:sticky;
  top:0;
}

nav a{
  margin:0 10px;
  text-decoration:none;
  color:white;
}

nav a:hover{
  color:#38bdf8;
}

/* ===== HERO ===== */
.hero{
  text-align:center;
  padding:80px 20px;
}

.hero img{
  width:120px;
  border-radius:50%;
  margin-bottom:10px;
}

/* ===== BUTTON ===== */
.btn{
  padding:10px 15px;
  background:#38bdf8;
  border:none;
  cursor:pointer;
  border-radius:8px;
  margin-top:10px;
}

.btn:hover{
  background:#0ea5e9;
}

/* ===== SECTIONS ===== */
.section{
  padding:60px 20px;
  text-align:center;
}

/* ===== CARDS ===== */
.cards{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
  gap:15px;
  margin-top:20px;
}

.card{
  background:#1e293b;
  padding:20px;
  border-radius:10px;
  transition:0.3s;
  opacity:0;
  transform:translateY(20px);
}

.card.show{
  opacity:1;
  transform:translateY(0);
}

.card:hover{
  transform:scale(1.05);
}

/* ===== WHATSAPP ===== */
.whatsapp{
  position:fixed;
  bottom:20px;
  right:20px;
  background:#25D366;
  padding:12px;
  border-radius:50px;
  color:white;
  text-decoration:none;
  font-weight:bold;
}

/* ===== TOGGLE ===== */
.toggle{
  cursor:pointer;
  background:#38bdf8;
  border:none;
  padding:8px;
  border-radius:5px;
}
</style>
</head>

<body class="dark">

<!-- HEADER -->
<header>
  <h2>Soleil</h2>

  <nav>
    <a href="#home">Accueil</a>
    <a href="#about">À propos</a>
    <a href="#projects">Projets</a>
    <a href="#contact">Contact</a>
  </nav>

  <button class="toggle" onclick="toggleMode()">🌙/☀️</button>
</header>

<!-- HERO -->
<section class="hero" id="home">
  <img src="photo.jpg" alt="photo">
  <h1>Salut 👋 je suis Soleil</h1>
  <p>Développeur web débutant</p>

  <a href="#projects">
    <button class="btn">Voir mes projets</button>
  </a>
</section>

<!-- ABOUT -->
<section class="section" id="about">
  <h2>À propos</h2>
  <p>
    Je suis en apprentissage du développement web (HTML, CSS, JavaScript).
    Ce site est mon portfolio 🚀
  </p>

  <a href="cv.pdf" download>
    <button class="btn">Télécharger mon CV</button>
  </a>
</section>

<!-- PROJECTS -->
<section class="section" id="projects">
  <h2>Mes Projets</h2>

  <div class="cards">
    <div class="card">Projet 1 - Site personnel</div>
    <div class="card">Projet 2 - HTML/CSS</div>
    <div class="card">Projet 3 - En cours</div>
  </div>
</section>

<!-- CONTACT -->
<section class="section" id="contact">
  <h2>Contact</h2>
  <p>Contacte-moi directement 📱</p>

  <a href="https://wa.me/000000000" target="_blank">
    <button class="btn">WhatsApp</button>
  </a>
</section>

<!-- WHATSAPP FLOAT -->
<a class="whatsapp" href="https://wa.me/000000000" target="_blank">
📱
</a>

<!-- SCRIPT -->
<script>
function toggleMode(){
  document.body.classList.toggle("light");
  document.body.classList.toggle("dark");
}

// animation scroll
window.addEventListener("scroll", () => {
  document.querySelectorAll(".card").forEach(card => {
    const top = card.getBoundingClientRect().top;
    if(top < window.innerHeight - 80){
      card.classList.add("show");
    }
  });
});
</script>

</body>
</html>
