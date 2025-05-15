<template>
    <div class="flex h-40 flex-row ml-1 ">
      <div class="w-[2px] h-full bg-black"></div>
  
      <div class="px-3 ">
        <ul class="h-full flex flex-col justify-between text-gray-600 ml-2">
            <Menu
              v-for="item in menuItems"
              :key="item.teks"
              :url="item.url"
              :teks="item.teks"
              :is-active="activeLink === item.url"
              @click="() => setActive(item.url)"
            />
      </ul>
      </div>
      
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  import Menu from '../components/Menu.vue'
  
  const activeLink = ref('#about')
  
  const menuItems = [
    { url: '#about', teks: 'About' },
    { url: '#skill', teks: 'Skill' },
    { url: '#project', teks: 'Project' },
    { url: '#contact', teks: 'Contact' },
  ]
  
  function setActive(link) {
    activeLink.value = link

    const target = document.querySelector(link)

    if (target) {
      target.scrollIntoView({ behavior: 'smooth' })
    }
  }
  </script>
  