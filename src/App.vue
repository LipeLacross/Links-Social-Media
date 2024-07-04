<template>
  <div class="app">
    <div class="overlay">
      <img src="/src/assets/profile.png" alt="Foto de Felipe Moreira" class="profile-pic" />
      <p class="name">Felipe Moreira</p>
      <p class="role">Front-End Developer</p>
    </div>
    <social_links />
  </div>
</template>

<script setup>
import social_links from './components/social_links.vue'
</script>

<style>
body, html {
  padding: 0;
  margin: 10px 40px 100px;
  height: 100%;
  width: 100%;
  font-family: Arial, sans-serif;
  overflow: hidden; /* Evita que elementos animados saiam da visualização */
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
}

.name {
  font-weight: 800;
  font-size: 1.8rem;
  margin: 0;
}

.role {
  font-weight: bold;
  font-size: 1.2rem;
  margin: 0;
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
</style>
