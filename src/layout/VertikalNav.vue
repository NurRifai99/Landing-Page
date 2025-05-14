<template>
    <div class="flex h-40 flex-row ml-1">
        <div class="w-[2px] h-full bg-black"></div>

        <ul class="flex flex-col justify-between text-gray-600">
            <Menu url="#about" teks="About" />
            <Menu url="#skill" teks="Skill"/>
            <Menu url="#project" teks="Project"/>
            <Menu url="#contact" teks="Contact"  />
        </ul>
    </div>
</template>

<script setup>
import Menu from '../components/Menu.vue'
</script>
