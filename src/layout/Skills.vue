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

  const selectedIndex = ref(2)
  

  import front from '../assets/image/front.jpeg'
  import back from '../assets/image/back.jpeg'
  import iot from '../assets/image/iot.jpeg'
  import linux from '../assets/image/linux.jpeg'

  const categories = [
    {
      title: 'Frontend Development',
      description:  'Frontend development focuses on building interactive and visually appealing user interfaces. Using modern frameworks and styling tools, I ensure seamless user experience.',
      icon: IcComputer,
      image:front
    },
    {
      title: 'Backend Development',
      description: 'Backend development involves handling server-side logic, databases, and APIs. I specialize in building scalable and secure backend systems.s',
      icon: BsDatabaseCheck,
      image: back
    },
    {
      title: 'IOT Development',
      description: 'IoT Development connects hardware with software to create smart systems. I work with microcontrollers and IoT platforms for automation and real-time data processing.',
      icon: CaIotConnect,
      image: iot
    },
    {
      title: 'Linux Management',
      description: 'Managing Linux System for Servers and Development Environments. I ensure system performance, security, and reliability.',
      icon: CoBrandLinux,
      image: linux
    },
  ]
  </script>
  
  
  