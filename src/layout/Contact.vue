<template>
    <div class=" w-full flex flex-col gap-4 justify-center md:justify-start text-xl sm:text-2xl md:text-3xl">

        <div className="container mx-auto grid grid-cols-1 md:grid-cols-2 gap-6 px-4 sm:px-8 md:px-12">
          <motion.a
          v-for="(social, index) in socials"
          :key="index"
          :href="social.link"
          target="_blank"
          rel="noopener noreferrer"
          class="flex items-center gap-3 py-2 bg-black rounded-lg transition transform hover:scale-105 hover:shadow-lg"
          :while-hover="{ scale: 1.1 }"
          :transition="{ stiffness: 300 }"
        >
          <component :is="social.icon" class="text-white w-6 h-6" />
          <span class="text-white text-sm md:text-2xl">{{ social.label }}</span>
          <p class="text-gray-300 text-sm">{{ social.account }}</p>
          </motion.a>
        </div>
    </div>
  </template>
  
  <script setup>
  import { motion } from 'motion-v'
  
  import { AkInstagramFill, AkLinkedinBoxFill, AkGithubFill,MdSharpEmail } from '@kalimahapps/vue-icons'
  const socials = [
    {
      icon: AkLinkedinBoxFill,
      link: 'https://www.linkedin.com/in/your-linkedin-username',
      label: 'LinkedIn',
      account: 'your-linkedin-account',
    },
    {
      icon: AkInstagramFill,
      link: 'https://instagram.com/your-instagram-username',
      label: 'Instagram',
      account: 'your-instagram-account',
    },
    {
      icon: AkGithubFill,
      link: 'https://github.com/your-github-username',
      label: 'GitHub',
      account: 'your-github-account',
    },
    {
      icon: MdSharpEmail,
      link: 'mailto:your-email@gmail.com',
      label: 'Email',
      account: 'your-email@gmail.com',
    },
  ]
  </script>
  