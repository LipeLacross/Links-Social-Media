<template>
  <div class="social-links">
    <img
        src="@/assets/profile.png"
        alt="Foto de Felipe Moreira"
        class="profile-pic"
        @click="toggleAnimation"
        :class="{ animate: isAnimating }"
    />
    <div class="content-container">
      <div class="info-container">
        <p class="name">Felipe Moreira</p>
        <p class="role">Developer</p>
      </div>
      <div class="links-container">
        <a href="https://www.instagram.com/lipelacross/" class="social-link instagram" title="Instagram">
          <img src="@/assets/instagram.png" alt="Instagram" class="social-icon" />
          <span>Instagram</span>
        </a>
        <a href="https://www.linkedin.com/in/lipelacross-developer" class="social-link linkedin" title="LinkedIn">
          <img src="@/assets/linkedin.png" alt="LinkedIn" class="social-icon" />
          <span>LinkedIn</span>
        </a>
        <a href="https://www.youtube.com/@DevLipeLacross" class="social-link youtube" title="YouTube">
          <img src="@/assets/youtube.png" alt="YouTube" class="social-icon" />
          <span>YouTube</span>
        </a>
        <a href="https://github.com/lipelacross" class="social-link github" title="GitHub">
          <img src="@/assets/github.png" alt="GitHub" class="social-icon" />
          <span>GitHub</span>
        </a>
        <a href="https://lipelacrossplus.netlify.app/" class="social-link portfolio" title="Em breve">
          <img src="@/assets/curriculum.png" alt="Portfolio" class="social-icon" />
          <span>Portfólio</span>
        </a>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const isAnimating = ref(false);

function toggleAnimation() {
  isAnimating.value = !isAnimating.value;
}
</script>

<style scoped>
/* Estilo do componente principal */
.social-links {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 100vh; /* Garante que o componente ocupe toda a altura da tela */
  width: 100%;
  background: transparent; /* Deixa o fundo degradê do body visível */
  position: relative; /* Necessário para posicionar corretamente o conteúdo */
  z-index: 1; /* Garante que o conteúdo fique acima do fundo degradê */
}

/* Imagem do perfil */
.profile-pic {
  width: 200px;
  height: 200px;
  border-radius: 50%;
  object-fit: cover;
  cursor: pointer;
  transition: transform 0.3s ease;
  animation: fadeIn 2s forwards;
  animation-fill-mode: backwards;
  margin-bottom: 20px; /* Espaço entre a imagem e o bloco branco */
}

/* Container com todos os elementos combinados */
.content-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  background-color: white;
  padding: 20px;
  border-radius: 35px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  width: 90%;
  max-width: 300px; /* Aumente a largura máxima se necessário */
  box-sizing: border-box;
  position: relative; /* Garante que o conteúdo tenha o fundo branco */
  z-index: 2; /* Garante que o conteúdo branco fique acima do fundo degradê */
  opacity: 0; /* Inicialmente invisível */
  animation: fadeInSlideUp 1s forwards; /* Animação para o bloco branco */
}

/* Informações do perfil */
.info-container {
  margin-bottom: 20px;
}

.name {
  font-weight: 800;
  font-size: 1.8rem;
  margin: 0;
  color: #333;
  opacity: 0;
  animation: fadeInText 1s forwards 1s;
}

.role {
  font-weight: bold;
  font-size: 1.2rem;
  margin: 0;
  color: #333;
  opacity: 0;
  animation: fadeInText 1s forwards 1.2s;
}

/* Animação de fundo */
@keyframes gradientShift {
  0% {
    background-position: 0% 0%;
  }
  50% {
    background-position: 100% 100%;
  }
  100% {
    background-position: 0% 0%;
  }
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(-20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes fadeInText {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Animação de fade-in e slide-up para o bloco branco */
@keyframes fadeInSlideUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Animação de zoom para os links */
@keyframes zoomIn {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.1);
  }
  100% {
    transform: scale(1);
  }
}

/* Animação de flash para a página */
@keyframes flash {
  0% {
    opacity: 1;
  }
  50% {
    opacity: 0.5;
  }
  100% {
    opacity: 1;
  }
}

/* Estilos dos links sociais */
.links-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
}

.social-link {
  width: 150px;
  height: 50px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 25px;
  text-decoration: none;
  color: #fff;
  font-weight: bold;
  cursor: pointer;
  transition: transform 0.3s ease, background-color 0.3s ease;
  animation: buttonHover 3s infinite, zoomIn 2s infinite; /* Adiciona animação de zoom */
  opacity: 0; /* Inicialmente invisível */
  animation: fadeInSlideUp 1s forwards, zoomIn 2s infinite; /* Animação para os links */
}

/* Atraso para a animação de cada link */
.social-link:nth-child(1) {
  animation-delay: 1s;
}

.social-link:nth-child(2) {
  animation-delay: 1.2s;
}

.social-link:nth-child(3) {
  animation-delay: 1.4s;
}

.social-link:nth-child(4) {
  animation-delay: 1.6s;
}

.social-link:nth-child(5) {
  animation-delay: 1.8s;
}

.social-icon {
  width: 30px;
  height: auto;
  margin-right: 10px;
}

.social-link:hover {
  background-color: #FFDE59;
}

.instagram {
  background-color: #833ab4;
}

.linkedin {
  background-color: #0a66c2;
}

.youtube {
  background-color: #c4302b;
}

.github {
  background-color: #333;
}

.portfolio {
  background-color: #000000;
}

/* Animação de flash para o fundo da página */
body {
  animation: flash 1s ease-out; /* Adiciona a animação de flash */
}

@keyframes buttonHover {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.1);
  }
  100% {
    transform: scale(1);
  }
}

</style>
