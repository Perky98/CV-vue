<script setup lang="ts">
const props = defineProps<{
  link: string
  image: string
  name: string
  technology: string
}>()
</script>

<template>
  <a
    :href="link"
    target="_blank"
    class="relative isolate flex flex-col justify-end overflow-hidden rounded-2xl mx-4 md:mx-0 px-8 pb-8 pt-40"
  >
    <img
      :src="`/src/assets/projects/${image}.png`"
      alt="{{ name }}"
      class="absolute inset-0 h-full w-full object-cover"
    />
    <div class="absolute inset-0 bg-gradient-to-t from-gray-900 via-gray-900/40"></div>
    <h3 class="z-10 mt-3 text-3xl font-bold text-white">{{ name }}</h3>
    <div class="z-10 gap-y-1 overflow-hidden text-sm leading-6 text-gray-300">
      {{ technology }}
    </div>
  </a>
</template>