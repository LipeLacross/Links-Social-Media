<template>
  <div id="app">
    <LoadingScreen :active="isLoading" />
    <SocialLinks />
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'
import SocialLinks from './components/SocialLinks.vue'
import LoadingScreen from './components/LoadingScreen.vue'

const isLoading = ref(true)

onMounted(() => {
  setTimeout(() => {
    isLoading.value = false
  }, 2000) // tempo de loading simulado (2 segundos)
})
</script>

<style src="./assets/main.css"></style>
