<template>
  <div class="app">
    <div class="overlay">
      <img
          src="@/assets/profile.png"
          alt="Foto de Felipe Moreira"
          class="profile-pic"
          @click="toggleAnimation"
          :class="{ animate: isAnimating }"
      />
      <div class="info-container">
        <p class="name">Felipe Moreira</p>
        <p class="role">Developer</p>
        <SocialLinks />
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import SocialLinks from './components/social_links.vue';

const isAnimating = ref(false);

function toggleAnimation() {
  isAnimating.value = !isAnimating.value;
}
</script>

<style>
/* Estilos gerais */
body, html {
  padding: 0;
  margin: 0;
  height: 100%;
  width: 100%;
  font-family: Arial, sans-serif;
  overflow: hidden;
  color: #333;
  display: flex;
  justify-content: center;
  align-items: center;
}

/* Estilo do componente principal */
.app {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
  width: 100%;
  text-align: center;
  z-index: 1;
}

.overlay {
  position: relative;
  z-index: 2;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.profile-pic {
  width: 200px;
  height: 200px;
  border-radius: 50%;
  object-fit: cover;
  cursor: pointer;
  transition: transform 0.3s ease;
  animation: fadeIn 2s forwards;
  animation-fill-mode: backwards;
}

.profile-pic:hover {
  transform: scale(1.2);
}

.info-container {
  background-color: white;
  padding: 20px;
  border-radius: 35px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  text-align: center;
  width: 100%;
  box-sizing: border-box;
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
