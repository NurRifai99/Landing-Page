<template>
  <li>
    <a
      :href="url"
      @click.prevent="$emit('click')"
      :class="[
        'transition-all duration-300',
        isActive ? 'font-bold text-black' : 'text-gray-500'
      ]"
    >
      {{ teks }}
    </a>
  </li>
</template>

<script setup>
defineProps({
  url: String,
  teks: String,
  isActive: Boolean
})

defineEmits(['click'])
</script>
