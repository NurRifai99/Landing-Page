<template>
  <section id="hero" class="w-full h-screen">
    <div class="relative w-full h-full flex flex-col  items-center">
        <div class="w-full h-2/5 flex justify-center" :style="{background:`url(${heroImage})`,backgroundSize: 'cover', backgroundPosition: 'center'}"></div>
        
        <div class="absolute bottom-0  w-[70%] h-[70%]  ">
          <div class="flex flex-col lg:flex-row">

            <div class="flex flex-col gap-5 h-full justify-center items-center ">  
              <!-- Image Profil -->
               <motion.div :initial="{scale:0.5,opacity:0}" :animate="{scale:1,opacity:1}" :transition="{duration:0.4,scale:{type:'spring',visualDuration: 0.4, bounce: 0.5}}">
                  <div class="w-48 h-48 rounded-full ring-[15px] ring-white">
                    <img src="/src/assets/image/Untitled.jpeg" class="w-full h-full object-cover rounded-full" alt="profile image" >
                  </div>
               </motion.div>

              <motion.div class="hidden mt-5 lg:flex " 
                :initial="{ opacity: 0,translateX:-10 }"
                :whileInView="{ opacity: 1 ,translateX: 1 }"
                :transition="{ duration: 0.3 }"
              >
                <VertikalNav/>
              </motion.div>
            </div>

            <!-- right -->
            <div class=" w-full pl-6 ">

              <motion.div class="flex flex-col lg:flex-row gap-3 text-white tracking-tight items-center top-0 mb"
                :initial="{ opacity: 0,translateY:10 }"  
                :whileInView="{ opacity: 1 ,translateY: 1 }"
                :transition="{ duration: 0.3 }"
              >
                <h1 class="text-5xl font-medium">Nur Rahman RIfai </h1>
                 <div class="hidden lg:block w-[3px] h-10 bg-white"/> <!-- divider -->
                 <vue-typewriter-effect 
                    :strings="['Junior Developer', 'Tech Enthusiast']" 
                    :autostart="true" 
                    :loop="true" 
                    class="text-2xl"/>
              </motion.div>

              <motion.div class="mt-7"
                :initial="{ opacity: 0,translateX:10 }"
                :whileInView="{ opacity: 1 ,translateX: 1 }"
                :transition="{ duration: 0.3 }"
              >
                <h2 class="text-6xl"><span class="font-bold">Hello</span> There</h2><br>
                <p>Saya adalah seorang siswa yang memiliki minat besar di bidang teknologi, khususnya dalam pengembangan web dan perangkat lunak. Rasa ingin tahu mendorong saya untuk terus belajar dan mengeksplorasi bagaimana teknologi dapat digunakan untuk memecahkan masalah nyata.</p>
                <br>
                <p>Saat ini, saya sedang memperdalam keterampilan di berbagai teknologi modern seperti HTML, CSS, JavaScript, dan framework seperti Vue. Tujuan saya adalah membangun fondasi yang kuat untuk berkontribusi dalam dunia digital yang terus berkembang.</p>
              </motion.div>
              <div class="text-black text-2xl">
                
              </div>
            </div>

          </div>
        </div>
        
        <div class="w-full h-3/5 bg-white"></div>
    </div>
  </section>
</template>

<script setup>
  import heroImage from '../assets/image/john-towner-3Kv48NS4WUU-unsplash.jpg'
  import { motion } from 'motion-v';
  import VertikalNav from './VertikalNav.vue'
  import VueTypewriterEffect from "vue-typewriter-effect";
</script>
