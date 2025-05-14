<template>
  <div id="landing-page" class="container">
    <header class="hero">
      <h1>{{ title }}</h1>
      <p>{{ subtitle }}</p>
      <button @click="goToCTA">{{ ctaText }}</button>
    </header>

    <section class="features">
      <div class="feature" v-for="(feature, index) in features" :key="index">
        <h2>{{ feature.title }}</h2>
        <p>{{ feature.description }}</p>
      </div>
    </section>

  
    <footer class="cta" ref="ctaSection">
      <h2>Ready to Get Started?</h2>
      <button @click="contactUs">Contact Us</button>
    </footer>
  </div>

  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="#00cba9" fill-opacity="1" d="M0,160L80,186.7C160,213,320,267,480,250.7C640,235,800,149,960,128C1120,107,1280,149,1360,170.7L1440,192L1440,320L1360,320C1280,320,1120,320,960,320C800,320,640,320,480,320C320,320,160,320,80,320L0,320Z"></path></svg>


</template>

<script setup>
import { ref } from 'vue'


const title = 'Welcome to VueLanding'
const subtitle = 'Build modern apps faster with Vue.js'
const ctaText = 'Learn More'

const features = [
  { title: 'Fast Development', description: 'Build and iterate quickly using Vue’s intuitive API.' },
  { title: 'Reactive Core', description: 'Data-driven interface updates with minimal effort.' },
  { title: 'Component-Based', description: 'Encapsulate logic and UI into reusable components.' }
]

const ctaSection = ref(null)

function goToCTA() {
  ctaSection.value.scrollIntoView({ behavior: 'smooth' })
}

function contactUs() {
  alert('Thank you for your interest. We will contact you shortly.')
}
</script>

<style scoped>
.container {
  font-family: Arial, sans-serif;
  max-width: 960px;
  margin: 0 auto;
  padding: 20px;
  text-align: center;
}

.hero {
  padding: 60px 20px;
  background-color: #42b983;
  color: white;
}

.hero button {
  background-color: white;
  color: #42b983;
  border: none;
  padding: 10px 20px;
  font-size: 1rem;
  cursor: pointer;
}

.features {
  display: flex;
  justify-content: space-around;
  padding: 40px 0;
}

.feature {
  max-width: 250px;
}

.cta {
  padding: 40px 0;
  background-color: #35495e;
  color: white;
}
</style>
