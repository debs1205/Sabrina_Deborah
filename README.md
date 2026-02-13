<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sabrina e Déborah</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600&family=Poppins:wght@300;400;500&display=swap" rel="stylesheet">
<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
}

body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: linear-gradient(180deg, #3b000c, #120005);
  color: #fff;
  overflow-x: hidden;

  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

/* ---------- SEÇÃO PRINCIPAL ---------- */
section {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 32px;
}

.hero {
  text-align: center;
}

.pedido-final {
  text-align: center;
  margin-top: 50px;
}

.pergunta {
  font-size: 1.4rem;
  color: #ffd1dc;
  margin-bottom: 25px;
  font-weight: 500;
}
.hero h1 {
  font-family: 'Playfair Display', serif;
  font-size: 2.4rem;
  color: #ffd1dc;
  margin-bottom: 12px;
}

.hero p {
  font-size: 1.1rem;
  opacity: 0.9;
}

/* ---------- CARROSSEL ---------- */
.carousel {
  width: 100%;
  max-width: 320px;
  overflow: hidden;
  border-radius: 24px;
  box-shadow: 0 20px 40px rgba(0,0,0,0.5);
  margin: 32px auto;
}

.carousel-track {
  display: flex;
  animation: slide 70s ease-in-out infinite;
}

.carousel img {
  width: 320px;
  height: 420px;
  object-fit: cover;
}

@keyframes slide {
  0% { transform: translateX(0); }
  100% { transform: translateX(-7040px); } /* 22 fotos */
}

/* ---------- FRASES ---------- */
.phrases {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 24px;
  max-width: 900px;
  margin: 0 auto;
}

.phrase-card {
  background: rgba(255,255,255,0.08);
  backdrop-filter: blur(10px);
  border-radius: 20px;
  padding: 20px;
  text-align: center;
  box-shadow: 0 20px 40px rgba(0,0,0,0.35);
}

.phrase-card img {
  width: 100%;
  border-radius: 16px;
  margin-bottom: 12px;
}

.phrase-card p {
  font-size: 1.05rem;
}

/* ---------- BOTÕES ---------- */
.buttons {
  margin-top: 32px;
  display: flex;
  gap: 20px;
  justify-content: center;
}

button {
  padding: 14px 28px;
  border: none;
  border-radius: 30px;
  font-size: 1rem;
  cursor: pointer;
}

#yes {
  background: #e60026;
  color: #fff;
}

#no {
  background: #fff;
  color: #e60026;
  position: relative;
}

/* ---------- TELA FINAL ---------- */
.final-screen {
  position: fixed;
  inset: 0;
  background: radial-gradient(circle at top, #7a0c1d, #2b020a);
  display: none;
  align-items: center;
  justify-content: center;
  z-index: 999;
}

.final-card {
  background: rgba(255,255,255,0.08);
  backdrop-filter: blur(14px);
  border-radius: 24px;
  padding: 48px 36px;
  max-width: 520px;
  text-align: center;
  box-shadow: 0 30px 60px rgba(0,0,0,0.35);
}

.final-card h1 {
  font-family: 'Playfair Display', serif;
  font-size: 2.2rem;
  color: #ffe6ec;
  margin-bottom: 12px;
}

.final-card p {
  font-size: 1.25rem;
  line-height: 1.6;
  margin-bottom: 12px;
}

.signature {
  margin-top: 20px;
  font-size: 1.1rem;
  color: #ffd1dc;
}

/* ---------- ANIMAÇÕES ---------- */
.fade-text {
  opacity: 0;
  transform: translateY(10px);
  animation: fadeInUp 1.4s forwards;
}

.delay-1 { animation-delay: 0.6s; }
.delay-2 { animation-delay: 1.2s; }
.delay-3 { animation-delay: 1.8s; }

@keyframes fadeInUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ---------- CORAÇÕES ---------- */
.heart {
  position: fixed;
  width: 16px;
  height: 16px;
  background: red;
  transform: rotate(45deg);
  animation: float 4s linear forwards;
}

.heart::before,
.heart::after {
  content: "";
  position: absolute;
  width: 16px;
  height: 16px;
  background: red;
  border-radius: 50%;
}

.heart::before { top: -8px; left: 0; }
.heart::after { left: -8px; top: 0; }

@keyframes float {
  from {
    opacity: 1;
    transform: translateY(0) rotate(45deg);
  }
  to {
    opacity: 0;
    transform: translateY(-600px) rotate(45deg);
  }
}
/* ---------- AJUSTES PARA CELULAR ---------- */
@media (max-width: 768px) {

  .hero h1 {
    font-size: 1.9rem;
  }

  .hero p {
    font-size: 1rem;
  }

  .carousel {
    max-width: 260px;
  }

  .carousel img {
    width: 260px;
    height: 360px;
  }

  .phrases {
    grid-template-columns: 1fr;
    gap: 18px;
  }

  .phrase-card p {
    font-size: 1rem;
  }

  .buttons {
    flex-direction: column;
  }

  button {
    width: 100%;
    max-width: 260px;
    margin: 0 auto;
    font-size: 1.1rem;
  }

  .final-card {
    padding: 32px 22px;
    margin: 0 16px;
  }

  .final-card h1 {
    font-size: 1.8rem;
  }

  .final-card p {
    font-size: 1.05rem;
  }

/* RODAPÉ */
 .rodape {
  background: #8b0000; /* vermelho mais claro que o fundo */
  text-align: center;
  padding: 15px;
  font-size: 0.8rem;
  color: #ffd6de;
  margin-top: 80px;

}

}

</style>
</head>

<body>

<!-- 🎶 Música -->
<audio id="bgMusic" loop>
  <source src="iris-goo-goo-dolls.mp3" type="audio/mpeg">
</audio>

<button onclick="document.getElementById('musica').play()">
  💖 Tocar nossa música
</button>
<section class="hero">
  <div>
    <h1>Sabrina e Deborah</h1>
    <p>Feliz 8 meses de noivado, de muito amor e companheirismo</p>
    <!-- 📸 Carrossel -->
    <div class="carousel">
      <div class="carousel-track">
        <!-- TROQUE PELOS NOMES DAS SUAS 22 FOTOS -->
        <img src="foto1.jpeg"><img src="foto2.jpeg"><img src="foto3.jpeg">
        <img src="foto4.jpeg"><img src="foto5.jpeg"><img src="foto6.jpeg">
        <img src="foto7.jpeg"><img src="foto8.jpeg"><img src="foto9.jpeg">
        <img src="foto10.jpeg"><img src="foto11.jpeg"><img src="foto12.jpeg">
        <img src="foto13.jpeg"><img src="foto14.jpeg"><img src="foto15.jpeg">
        <img src="foto16.jpeg"><img src="foto17.jpeg"><img src="foto18.jpeg">
        <img src="foto19.jpeg"><img src="foto20.jpeg"><img src="foto21.jpeg">
        <img src="foto22.jpeg">
      </div>
    </div>
    <!-- Frases -->
    <div class="phrases">
      <div class="phrase-card"><img src="postit1.jpeg"><p>Você é tudo que sempre sonhei</p></div>
      <div class="phrase-card"><img src="postit2.jpeg"><p>Eu amo tanto seu sorriso</p></div>
      <div class="phrase-card"><img src="postit3.jpeg"><p>Você é a mulher mais incrível do mundo</p></div>
      <div class="phrase-card"><img src="postit4.jpeg"><p>Meu coração escolhe você todos os dias</p></div>
      <div class="phrase-card"><img src="postit5.jpeg"><p>Eu te admiro em tantos detalhes</p></div>
      <div class="phrase-card"><img src="postit6.jpeg"><p>Obrigada por tantos momentos inesquecíveis</p></div>
      <div class="phrase-card"><img src="postit7.jpeg"><p>Eu amo nossa pequena e linda família</p></div>
      <div class="phrase-card"><img src="postit8.jpeg"><p>Eu amo tudo que envolva estar com você</p></div>
      <div class="phrase-card"><img src="postit9.jpeg"><p>Você é minha melhor decisão</p></div>
    </div>

    <!-- Botões -->
   <div class="pedido-final">

  <p class="pergunta">
    Você poderia passar todos os dias da sua vida comigo?
  </p>

  <div class="buttons">
    <button id="yes" onclick="showFinal()">SIM 💍</button>
    <button id="no" onmouseover="runAway()">Não</button>
  </div>
  </section>


<!-- TELA FINAL -->
<div class="final-screen" id="final">
  <div class="final-card">
    <h1 class="fade-text">Sabrina Emanuelle,</h1>
    <p class="fade-text delay-1">
      Meu bem querer, quis escrever isso só pra te lembrar (mais uma vez) do quanto eu sou louca por você. Quero que você nunca, em momento nenhum (pfvr), duvide do que sinto por você.
      Eu escolho você todos os dias da minha vida, nos detalhes bestas e nos momentos de caos.
      Fico pensando em tudo que a gente já viveu... naquelas noites de filmes/séries que a gente perde a hora (mesmo tendo que acordar cedo), nos nossos joguinhos e em cada date nosso. Cada janta, cada toque seu e cada vez que eu te vejo sorrir com o olinho meio fechado, eu sinto que me apaixono todos os dias de um jeito novo por você. 
    </p>
    <p class="fade-text delay-2">
      Obrigada por tantos momentos especiais, por ser minha parceira, por dividir a vida comigo e por dizer <strong>SIM</strong> pra nossa linda história.
      Eu amo você hoje, amanhã e sempre.
    </p>
    <p class="signature fade-text delay-3">
      — Com todo meu amor, sua noiva, Déborah. 
    </p>
  </div>
</div>

<!-- RODAPÉ -->
 
<footer class="rodape">
  Desenvolvido por quem tanto te ama e te admira, Déborah Viana 🤍
</footer>

<script>
function showFinal() {
  document.getElementById('final').style.display = 'flex';
  for (let i = 0; i < 40; i++) {
    setTimeout(createHeart, i * 120);
  }
}

function createHeart() {
  const h = document.createElement('div');
  h.className = 'heart';
  h.style.left = Math.random() * window.innerWidth + 'px';
  h.style.bottom = '0';
  h.style.background = Math.random() > 0.2 ? '#e60026' : '#fff';
  document.body.appendChild(h);
  setTimeout(() => h.remove(), 4000);
}

function runAway() {
  const b = document.getElementById('no');
  b.style.left = Math.random() * 200 - 100 + 'px';
  b.style.top = Math.random() * 200 - 100 + 'px';
}

</script>

</body>
</html>
