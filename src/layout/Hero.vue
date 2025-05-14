<template>
  <section id="hero" class="w-full h-screen">
    <div class="relative w-full h-full flex flex-col  items-center">
        <div class="w-full h-2/5 flex justify-center" :style="{background:`url(${heroImage})`,backgroundSize: 'cover', backgroundPosition: 'center'}"></div>
        
        <div class="absolute bottom-0  w-[70%] h-[70%]  ">
          <div class="flex flex-col lg:flex-row">

            <div class="flex flex-col gap-5 h-full ">  
              <div class="w-48 h-48 rounded-full ring-[10px] ring-white">
                <img src="/src/assets/image/Untitled.jpeg" class="w-full h-full object-cover rounded-full" alt="" srcset="">
              </div>

              <div class="hidden mt-5 lg:flex ">
                <ul>
                  <li>asads</li>
                  <li>asdasd</li>
                  <li>eaff</li>
                  <li>aserf</li>
                </ul>
              </div>
            </div>

            <!-- right -->
            <div class=" w-full pl-6 ">

              <div class="flex flex-col lg:flex-row gap-3 text-white tracking-tight items-center top-0 mb">
                <h1 class="text-5xl font-medium">Nur Rahman RIfai </h1>
                 <div class="hidden lg:block w-[3px] h-10 bg-white"/> <!-- divider -->
                 <vue-typewriter-effect :strings="['Junior Developer', 'Tech Enthusiast']" :autostart="true" :loop="true" class="text-xl"/>
              </div>

              <div class="mt-7">
                <h2 class="text-6xl"><span class="font-bold">Hello</span> There</h2><br>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate suscipit, reprehenderit possimus commodi natus nam laboriosam, consectetur ducimus aperiam dolores vitae sequi incidunt iste similique sed. Atque dolores labore laborum!</p>
              </div>
              <div class="text-black text-2xl">
                <motion.div :initial="{scale:0}" :animate="{scale:1}" :transition="{duration:0.3,scale:3}" >cekcek</motion.div>
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
  import NavBar from './NavBar.vue'
  import { motion } from 'motion-v';
  import VueTypewriterEffect from "vue-typewriter-effect";
</script>
