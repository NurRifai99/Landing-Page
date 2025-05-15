<template>
    <div id="contact" class="w-full min-h-[70vh] flex justify-center items-center bg-gray-100  px-4">
      <div class="w-full max-w-6xl bg-white  shadow-lg rounded-xl p-8 flex flex-col items-center gap-8 text-center">
        <motion.div
          class="text-4xl md:text-5xl font-extrabold text-gray-800 text-black"
          :initial="{ opacity: 0, translateY: 50 }"
          :whileInView="{ opacity: 1, translateY: 0 }"
          :transition="{ duration: 0.8, ease: 'easeInOut' }"
        >
          Contact Me
        </motion.div>
  
        <div class="grid grid-cols-2 sm:grid-cols-2 md:grid-cols-4 gap-6 w-full">
          <motion.a
            v-for="(item, index) in socials"
            :key="index"
            :href="item.link"
            target="_blank"
            rel="noopener noreferrer"
            class="flex flex-col items-center gap-2 p-4 rounded-lg bg-gray-400 hover:bg-gray-100 dark:hover:bg-gray-700 transition duration-300 shadow-md"
            :initial="{ opacity: 0, scale: 0.9 }"
            :whileInView="{ opacity: 1, scale: 1 }"
            :transition="{ duration: 0.5, delay: index * 0.1 }"
          >
            <component :is="item.icon" class="text-4xl text-black " />
            <span class="font-medium text-lg text-black ">{{ item.label }}</span>
            <span class="text-sm text-black ">{{ item.account }}</span>
          </motion.a>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { motion } from 'motion-v'
  import { AkInstagramFill, AkLinkedinBoxFill, AkGithubFill, MdSharpEmail } from '@kalimahapps/vue-icons'
  
  const socials = [
    {
      icon: AkLinkedinBoxFill,
      link: 'https://www.linkedin.com/in/ynur-rahman-rifai',
      label: 'LinkedIn',
      account: 'nur-rahman-rifai',
    },
    {
      icon: AkInstagramFill,
      link: 'https://instagram.com/nur_rifaiii',
      label: 'Instagram',
      account: 'nur_rifaiii',
    },
    {
      icon: AkGithubFill,
      link: 'https://github.com/NurRifai99',
      label: 'GitHub',
      account: 'NurRifai99',
    },
    {
      icon: MdSharpEmail,
      link: 'mailto:nurrahmanrifai3@gmail.com',
      label: 'Email',
      account: 'nurrahmanrifai3@gmail.com',
    },
  ]
  </script>
  
  <style scoped>
  /* Optional scoped styles */
  </style>
  