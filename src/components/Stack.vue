<script setup lang="ts">
const props = defineProps<{
  image: string
}>()
</script>
<template>
  <div class="w-full md:max-w-5xl mx-auto">
    <h2 class="text-center md:text-left text-3xl font-bold my-8">My stack</h2>
    <h3 class="text-center md:text-left text-2xl font-bold my-8">Fronted:</h3>

    <div class="flex flex-wrap items-center justify-center gap-10 mt-2 md:justify-around">
      <div class="text-gray-400">
        <img :src="`/src/assets/projects/${image}.png`" alt="{{image}}">
      </div>

      <div class="text-gray-400">

      </div>

      <div class="text-gray-400">

      </div>

      <div class="text-gray-400">

      </div>

      <div class="text-gray-400">

      </div>
    </div>
  </div>
</template>
