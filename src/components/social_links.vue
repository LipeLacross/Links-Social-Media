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
    <a href="https://github.com/LipeLacross" class="social-link github" title="GitHub">
      <span>GitHub</span>
    </a>
    <div class="social-link portfolio" title="Em breve">
      <span>Em breve</span>
    </div>
  </div>
</template>

<script setup>
</script>

<style scoped>
.social-links {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
  margin-top: 1rem;
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
  animation: buttonHover 3s infinite;
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
  background-color: #333; /* Cor para GitHub */
}

.portfolio {
  background-color: #000000
}
</style>
