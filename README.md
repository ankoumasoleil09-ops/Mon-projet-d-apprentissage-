<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mon Portfolio Pro</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
<script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    font-family:'Poppins', sans-serif;
    scroll-behavior:smooth;
    background:#f5f7fa;
    color:#333;
}

header{
    position:fixed;
    width:100%;
    top:0;
    background:white;
    box-shadow:0 2px 10px rgba(0,0,0,0.1);
    padding:15px 50px;
    display:flex;
    justify-content:space-between;
    align-items:center;
    z-index:1000;
}

header h1{
    font-size:22px;
    color:#00bcd4;
}

nav ul{
    list-style:none;
    display:flex;
}

nav ul li{
    margin-left:20px;
}

nav ul li a{
    text-decoration:none;
    color:#333;
    font-weight:500;
    transition:0.3s;
}

nav ul li a:hover{
    color:#00bcd4;
}

.hero{
    height:100vh;
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    text-align:center;
    background:linear-gradient(135deg,#00bcd4,#2196f3);
    color:white;
    padding:20px;
}

.hero h2{
    font-size:40px;
    margin-bottom:15px;
}

.hero p{
    max-width:600px;
    margin-bottom:20px;
}

button{
    padding:12px 25px;
    border:none;
    border-radius:30px;
    background:white;
    color:#2196f3;
    font-weight:bold;
    cursor:pointer;
    transition:0.3s;
}

button:hover{
    transform:scale(1.05);
}

section{
    padding:100px 50px;
    text-align:center;
}

section h2{
    margin-bottom:30px;
    font-size:30px;
    color:#2196f3;
}

.card-container{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:20px;
}

.card{
    background:white;
    padding:25px;
    border-radius:15px;
    box-shadow:0 5px 20px rgba(0,0,0,0.1);
    transition:0.3s;
}

.card:hover{
    transform:translateY(-10px);
}

.image-grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:20px;
    margin-top:20px;
}

.image-card{
    background:white;
    border-radius:15px;
    box-shadow:0 5px 20px rgba(0,0,0,0.1);
    overflow:hidden;
    transition:0.3s;
}

.image-card img{
    width:100%;
    display:block;
    border-bottom:1px solid #ddd;
}

.image-card p{
    padding:15px;
    font-weight:500;
    color:#333;
    text-align:center;
}

.image-card:hover{
    transform:translateY(-10px);
}

.social-icons{
    margin-top:20px;
}

.social-icons a{
    margin:0 10px;
    font-size:24px;
    color:#2196f3;
    transition:0.3s;
}

.social-icons a:hover{
    color:#00bcd4;
}

footer{
    background:#111;
    color:white;
    padding:20px;
    text-align:center;
}

.dark{
    background:#121212;
    color:white;
}

.dark header{
    background:#1e1e1e;
}

.dark .card, .dark .image-card{
    background:#1e1e1e;
    color:white;
}
</style>
</head>

<body>

<header>
    <h1>Mon Portfolio</h1>
    <nav>
        <ul>
            <li><a href="#home">Accueil</a></li>
            <li><a href="#services">Compétences</a></li>
            <li><a href="#portfolio">Projets</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>
</header>

<section class="hero" id="home">
    <h2>Bienvenue sur mon site 🚀</h2>
    <p>Je suis débutant dans la création de sites web et je continue d'apprendre HTML, CSS et JavaScript.</p>
    <button onclick="theme()">Changer le thème</button>
</section>

<section id="services">
    <h2>Mes Compétences</h2>
    <div class="card-container">
        <div class="card">
            <h3>HTML & CSS</h3>
            <p>Création de sites modernes et responsives.</p>
        </div>
        <div class="card">
            <h3>JavaScript</h3>
            <p>Fonctionnalités interactives et dynamiques.</p>
        </div>
        <div class="card">
            <h3>Design Web</h3>
            <p>Interfaces propres et professionnelles.</p>
        </div>
    </div>
</section>

<section id="portfolio">
    <h2>Mes Projets</h2>
    <div class="image-grid">
        <div class="image-card">
            <img src="https://via.placeholder.com/400x250" alt="Projet 1">
            <p>Projet 1 - Site vitrine</p>
        </div>
        <div class="image-card">
            <img src="https://via.placeholder.com/400x250" alt="Projet 2">
            <p>Projet 2 - Application web</p>
        </div>
        <div class="image-card">
            <img src="https://via.placeholder.com/400x250" alt="Projet 3">
            <p>Projet 3 - Portfolio interactif</p>
        </div>
    </div>
</section>

<section id="contact">
    <h2>Contact</h2>
    <p>Email : exemple@email.com</p>
    <div class="social-icons">
        <a href="#"><i class="fab fa-github"></i></a>
        <a href="#"><i class="fab fa-linkedin"></i></a>
        <a href="#"><i class="fas fa-envelope"></i></a>
    </div>
</section>

<footer>
    © 2026 Mon Portfolio | Développé avec passion 💻
</footer>

<script>
function theme(){
    document.body.classList.toggle("dark");
}
</script>

</body>
</html>
