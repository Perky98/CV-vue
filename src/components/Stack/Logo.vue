<script setup lang="ts">
const props = defineProps<{
  image: string
}>()
</script>

<template>
  <div class="relative text-gray-400">
    <img class=" h-[3rem]" :src="`/CV-vue/assets/stack/${image}.png`" alt="image">
  </div>
</template>

