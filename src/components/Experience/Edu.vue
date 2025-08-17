<script setup lang="ts">
const props = defineProps<{
  title: string
  image: string
  durations: string
  name: string
}>()
</script>

<template>
  <div class="flex gap-5">
    <img class="w-[30px] h-[30px] mt-1" :src="`/cv-vue/src/assets/${image}`" :alt="name" />
    <div>
      <h2 class="text-2xl font-bold text-gray-100">{{ title }}</h2>
      <span class="font-bold text-gray-100 text-lg">{{ name }}</span>
      <h3 class="text-gray-100">{{ durations }}</h3>
    </div>
  </div>
</template>
