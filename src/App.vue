<template>
  <div class="app">
    <div class="overlay">
      <img src="/src/assets/profile.png" alt="Foto de Felipe Moreira" class="profile-pic" />
      <p class="name">Felipe Moreira</p>
      <p class="role">Desenvolvedor</p>
    </div>
    <social_links />
  </div>
</template>

<script setup>
import social_links from './components/social_links.vue'
</script>

<style>
body, html {
  margin: 0;
  padding: 0;
  height: 100%;
  width: 100%;
  background: linear-gradient(180deg, #ffffff 0%, #FFDE59 100%); /* Degradê do branco ao amarelo */
  font-family: Arial, sans-serif;
}

.app {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100%;
  text-align: center;
}

.overlay {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 0rem;
}

.profile-pic {
  width: 200px;
  height: 200px;
  border-radius: 50%;
  object-fit: cover; /* Corrige a distorção da imagem */
  margin-bottom: 0rem;
}

.name {
  font-weight: bold;
  font-size: 1.5rem;
  margin: 0;
}

.role {
  font-weight: bold;
  font-size: 1.2rem;
  margin: 0;
}
</style>
