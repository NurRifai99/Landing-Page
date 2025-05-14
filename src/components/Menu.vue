<template>
    <li class="my-2">
        <a class="px-3 py-2 text-black" :href="url" >{{ teks }}</a>
    </li>
</template>

<script setup>

const props = defineProps({
  teks: String,
  url: String,
})

</script>
