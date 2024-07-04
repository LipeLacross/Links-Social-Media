<template>
  <div class="app">
    <div class="overlay">
      <img
          src="/src/assets/profile.png"
          alt="Foto de Felipe Moreira"
          class="profile-pic"
          @click="toggleAnimation"
          :class="{ animate: isAnimating }"
      />
      <p class="name">Felipe Moreira</p>
      <p class="role">Front-End Developer</p>
    </div>
    <social_links />
  </div>
</template>

<script setup>
import { ref } from 'vue';
import social_links from './components/social_links.vue';

const isAnimating = ref(false);

function toggleAnimation() {
  isAnimating.value = !isAnimating.value;
}
</script>

<style>
body, html {
  padding: 0;
  margin: 10px 40px 100px;
  height: 100%;
  width: 100%;
  font-family: Arial, sans-serif;
  overflow: hidden; /* Evita que elementos animados saiam da visualização */
  color: #333; /* Cor padrão para o texto */
}

.app {
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100%;
  text-align: center;
  z-index: 1; /* Garante que o conteúdo esteja acima do fundo animado */
}

.overlay {
  position: relative;
  z-index: 2; /* Garante que o conteúdo esteja acima do fundo animado */
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 1rem;
}

.profile-pic {
  width: 200px;
  height: 200px;
  border-radius: 50%;
  object-fit: cover;
  margin-bottom: 0rem;
  cursor: pointer; /* Adiciona cursor de ponteiro ao passar o mouse */
  transition: transform 0.3s ease; /* Transição suave no efeito de transformação */
  animation: fadeIn 2s forwards; /* Adiciona a animação de fade-in */
  animation-fill-mode: backwards; /* Mantém o estado final da animação */
}

.profile-pic:hover {
  transform: scale(1.2); /* Aumenta um pouco a escala ao passar o mouse */
}

.name {
  font-weight: 800;
  font-size: 1.8rem;
  margin: 0;
  color: #333; /* Garante que o texto do nome seja legível */
  opacity: 0;
  animation: fadeInText 1s forwards 1s; /* Adiciona um atraso para a animação do texto */
}

.role {
  font-weight: bold;
  font-size: 1.2rem;
  margin: 0;
  color: #333; /* Garante que o texto da função seja legível */
  opacity: 0;
  animation: fadeInText 1s forwards 1.2s; /* Adiciona um atraso para a animação do texto */
}

/* Animação de fundo */
body {
  background: linear-gradient(135deg, #FFDE59, #ffffff, #FFDE59);
  background-size: 900% 900%;
  animation: moveBackground 10s linear infinite;
}

@keyframes moveBackground {
  0% {
    background-position: 0% 0%;
  }
  100% {
    background-position: 100% 100%;
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
</style>
