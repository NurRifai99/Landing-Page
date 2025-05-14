<script setup>
// import { defineProps } from 'vue'

const {props} = defineProps({
  menu: String,
  url: String,
})

</script>

<template>
    <li class="px-3 py-2 bg-red-700">
        <a class="text-white" :href="url" >{{ menu }}</a>
    </li>
</template>
