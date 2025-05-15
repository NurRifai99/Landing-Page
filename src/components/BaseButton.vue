<!-- Base Button for hero section -->
<template>
    <a
      :href="url"
      class="w-full sm:w-auto rounded-full bg-gray-400 px-5 sm:px-6 py-2 sm:py-3 font-semibold shadow-lg transition-all hover:bg-gray-500 hover:scale-[1.1] text-sm sm:text-base text-center"
    >
      <slot/>
    </a>
  </template>
  
  <script setup>
  defineProps({
    url: String
  });

  </script>
  