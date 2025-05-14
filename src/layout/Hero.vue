<script setup>
import heroImage from '../assets/image/john-towner-3Kv48NS4WUU-unsplash.jpg'
import NavBar from './NavBar.vue'
</script>

<template>
  <section id="hero" class="relative w-full h-screen">
    <!-- Background -->
    <div class="absolute inset-0 bg-cover bg-center" :style="{backgroundImage:`url(${heroImage})`}"></div>
    <div class="absolute inset-0 bg-black/50"></div>

    <!-- Konten -->
    <div class="relative z-10 h-full text-white overflow-hidden">
      <NavBar />

      <div class="relative h-full flex flex-col items-center justify-center gap-6">
        <div class="w-60 h-60 rounded-full bg-red-500"></div>

        
      </div>
    </div>
  </section>
</template>
