<script setup lang="ts">
const props = defineProps<{
  title: string
  link: string
  image: string
  durations: string
  technologies: string
  name: string
}>()
</script>

<template>
  <div class="flex gap-5">
    <img class="w-[30px] h-[30px] mt-1" :src="`/src/assets/${image}`" alt="{{name}}" />
    <div>
      <h2 class="text-2xl font-bold text-gray-100">{{ title }}</h2>
      <a class="font-bold text-gray-100 text-lg" target="_blank" :href="link">{{name}}</a>
      <h3 class="text-gray-100">{{ durations }}</h3>
      <p class="text-gray-100">{{ technologies }}</p>
    </div>
  </div>
</template>
