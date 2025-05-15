<template>
    <div id="project" class="px-6 py-10 mb-10">

      <!-- Kategori -->
      <div class="flex gap-8 justify-center mb-8 text-xl font-semibold">
        <button
          :class="tab === 'My Project' ? activeClass : inactiveClass"
          ..click="tab = 'My Project'"
        >
            My Project
        </button>
        <button
          :class="tab === 'Certificate' ? activeClass : inactiveClass"
          ..click="tab = 'Certificate'"
        >
            Certificate
        </button>
      </div>
    <!-- Kategori -->
  
      <!-- Card  -->
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
        <div
          v-for="(item, index) in filteredItems"
          :key="index"
          class="bg-white rounded-xl shadow-md overflow-hidden"
        >
          <img :src="item.image" alt="" class="w-full h-48 object-cover" />
  
          <div class="p-4">
            <h3 class="text-lg font-semibold">{{ item.title }}</h3>
            <div class="flex flex-wrap items-center gap-2 mt-2 text-sm text-white">
              
              <span class="text-gray-500 ml-2">• {{ item.date }}</span>
            </div>
        
          </div>
        </div>
      </div>
      <!-- Card  -->

    </div>
  </template>
  
  <script setup>
  import { ref, computed } from 'vue'
  
  // Tab control
  const tab = ref('My Project')
  
  // Sample data
  const items = [
  {
    type: 'My Project',
    title: 'FoodTopia - Food Receipe Web',
    image: new URL('../..assets/project/foodtopiia.png', import.meta.url).href,
    date: 'Feb, 2023',
  },
  {
    type: 'My Project',
    title: 'Streamlit - Mikrotik Network Configuration',
    image: new URL('../..assets/project/streamlit.jpeg', import.meta.url).href,
    date: 'Mar, 2025',
  },
  {
    type: 'Certificate',
    title: 'MTCNA - MikroTik Certified Network Associate',
    image: new URL('../..assets/project/serti1.jpg', import.meta.url).href,
    date: 'May, 2024',
  },
  {
    type: 'Certificate',
    title: 'Belajar Dasar Manajemen Projek - Dicoding',
    image: new URL('../..assets/project/serti2.png', import.meta.url).href,
    date: 'Apr, 2024',
  },
  {
    type: 'Certificate',
    title: 'Memulai Pemograman Dengan C - Dicoding',
    image: new URL('../..assets/project/serti3.png', import.meta.url).href,
    date: 'May, 2024',
  },
]

  
  // Computed filter
  const filteredItems = computed(() =>
    items.filter((item) => item.type === tab.value)
  )
  
  const activeClass = 'border-b-2 border-black text-black'
  const inactiveClass = 'text-gray-400 hover:text-black'
  </script>
  