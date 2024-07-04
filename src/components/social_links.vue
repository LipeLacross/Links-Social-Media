<template>
  <div class="social-links">
    <a href="https://www.instagram.com/lipelacross/" class="social-link instagram" title="Instagram">
      <span>Instagram</span>
    </a>
    <a href="https://www.linkedin.com/in/lipelacross-developer/" class="social-link linkedin" title="LinkedIn">
      <span>LinkedIn</span>
    </a>
    <a href="https://www.youtube.com/@DevLipeLacross" class="social-link youtube" title="YouTube">
      <span>YouTube</span>
    </a>
    <div class="social-link portfolio" title="Em breve">
      <span>Em breve</span>
    </div>
  </div>
</template>

<script setup>
// Pode adicionar scripts para animações aqui, se necessário
</script>

<style scoped>
.social-links {
  display: flex;
  flex-direction: column; /* Empilhamento vertical */
  align-items: center;
  gap: 1rem; /* Espaçamento entre as caixas */
  margin-top: 2rem;
}

.social-link {
  width: 150px;
  height: 50px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 25px;
  color: #fff;
  font-weight: bold;
  cursor: pointer;
  transition: transform 0.3s ease, background-color 0.3s ease;
}

.social-link:hover {
  transform: scale(1.1);
}

.instagram {
  background-color: #833ab4; /* Cor roxa para o Instagram */
}

.linkedin {
  background-color: #0a66c2; /* Cor do LinkedIn */
}

.youtube {
  background-color: #c4302b; /* Cor do YouTube */
}

.portfolio {
  background-color: #333;
}
</style>
