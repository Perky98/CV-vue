<script setup lang="ts">

import Logo from '@/components/Stack/Logo.vue'
</script>
<template>
  <div class="w-full md:max-w-5xl mx-auto">
    <h2 class="text-center md:text-left text-3xl font-bold my-8">My stack</h2>
    <h3 class="text-center md:text-left text-2xl font-bold my-8">Frontend:</h3>

    <div class="flex  items-center justify-center gap-10 mt-2 md:justify-around">
      <logo image="vue"/>
      <logo image="qwik"/>
      <logo image="JS"/>
      <logo image="Tailwind"/>
      <logo image="Sass"/>
      <logo image="alpine"/>

    </div>
    <h3 class="text-center md:text-left text-2xl font-bold my-8">Backend:</h3>
    <div class="flex  items-center justify-center gap-10 mt-2 md:justify-around">
      <logo image="PHP"/>
      <logo image="C"/>

    </div>
    <h3 class="text-center md:text-left text-2xl font-bold my-8">Other tools:</h3>
    <div class="flex  items-center justify-center gap-10 mt-2 md:justify-around">
      <logo image="SEO"/>
      <logo image="Figma"/>
      <logo image="Git"/>


    </div>
  </div>
</template>
