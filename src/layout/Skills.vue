<template>
    <div id="skill" class="flex flex-col lg:flex-row min-h-screen p-6 gap-6 bg-gray-50">

      <!-- Left - Skills -->
      <motion.div
        class="flex-1 bg-white p-6 rounded-xl shadow-md"
        :initial="{ opacity: 0, x: 30 }"
        :animate="{ opacity: 1, x: 0 }"
        :transition="{ duration: 0.4 }"
        :key="selectedIndex"
      >
        <h2 class="text-2xl font-bold mb-4">{{ categories[selectedIndex].title }}</h2>
        <div class="mt-6">
          <img :src="categories[selectedIndex].image" alt="Panel Image" class="rounded-xl w-full max-h-96 object-cover" />
        </div>
      </motion.div>
        <!-- Left - Skills -->

        <!-- Right - Category List -->
      <div class="flex flex-col gap-4 w-full lg:w-1/3">
        <button
          v-for="(category, index) in categories"
          :key="index"
          @click="selectedIndex = index"
          class="flex items-center gap-4 p-4 rounded-xl transition-all shadow-sm hover:shadow-md"
          :class="{
            'bg-white border border-gray-500 shadow-md': selectedIndex === index,
            'bg-white': selectedIndex !== index
          }"
        >
          <div class="`w-12 h-12 flex items-center justify-center rounded-full">
              <component :is="category.icon" class="w-6 h-6" />
          </div>
          <div>
            <h3 class="font-semibold text-md">{{ category.title }}</h3>
            <p class="text-sm text-gray-500">{{ category.description }}</p>
          </div>
        </button>
      </div>
      <!-- Right - Category List -->

    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  import { motion } from 'motion-v'
  
  import { IcComputer,BsDatabaseCheck,CaIotConnect,CoBrandLinux } from '@kalimahapps/vue-icons';

  const selectedIndex = ref(0)
  
  const categories = [
  {
    title: 'Frontend Development',
    description: '...',
    icon: IcComputer,
    image: new URL('@/assets/image/front.jpeg', import.meta.url).href,
  },
  {
    title: 'Backend Development',
    description: '...',
    icon: BsDatabaseCheck,
    image: new URL('@/assets/image/back.jpeg', import.meta.url).href,
  },
  {
    title: 'IOT Development',
    description: '...',
    icon: CaIotConnect,
    image: new URL('@/assets/image/iot.jpeg', import.meta.url).href,
  },
  {
    title: 'Linux Management',
    description: '...',
    icon: CoBrandLinux,
    image: new URL('@/assets/image/linux.jpeg', import.meta.url).href,
  },
]

  </script>
  
  
  