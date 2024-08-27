<template>
  <div class="social-links">
    <a href="https://www.instagram.com/lipelacross/" class="social-link instagram" title="Instagram">
      <img src="@/assets/instagram.png" alt="Instagram" class="social-icon" />
      <span>Instagram</span>
    </a>
    <a href="https://www.linkedin.com/in/lipelacross-developer?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app" class="social-link linkedin" title="LinkedIn">
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
    <a href="https://lipelacross.netlify.app/" class="social-link portfolio" title="Em breve">
      <img src="@/assets/curriculum.png" alt="Portfolio" class="social-icon" />
      <span>Portfólio</span>
    </a>
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
  text-decoration: none;
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
</style>
