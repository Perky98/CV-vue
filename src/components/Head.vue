<script setup>
import { computed } from 'vue'

// zadaj svoj dátum narodenia
const birthDate = new Date('2003-08-09')

const age = computed(() => {
  const today = new Date()
  let years = today.getFullYear() - birthDate.getFullYear()
  const monthDiff = today.getMonth() - birthDate.getMonth()
  const dayDiff = today.getDate() - birthDate.getDate()

  if (monthDiff < 0 || (monthDiff === 0 && dayDiff < 0)) {
    years--
  }

  return years
})
</script>

<template>
  <section class="flex flex-col flex-wrap p-10 px-8 sm:py-20 md:py-20 lg:py-40 lg:pt-20 mx-auto h-full  justify-between  ">
    <h1 class="text-3xl font-bold md:text-7xl">Juraj Hertel</h1>
    <h3 class="text-3xl py-3">Frontend Developer | Maybe one day Fullstack</h3>
    <div class="flex flex-col md:flex-row gap-1 md:gap-4">
      <div class="flex gap-4 py-3 items-center">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" width="30" height="30">
          <path d="M50 15 C35 15, 25 25, 25 40 C25 55, 50 75, 50 75 C50 75, 75 55, 75 40 C75 25, 65 15, 50 15 Z"
                fill="#4aa962"/>

          <!-- Vnitřní kruh -->
          <circle cx="50" cy="40" r="8" fill="#fff"/>
        </svg>
        <p >Horné Otrokovce | Slovakia </p>
      </div>
      <div class="flex gap-4 py-3 items-center">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" width="30" height="30">
          <!-- Torta podstavec -->
          <ellipse cx="50" cy="80" rx="35" ry="8" fill="#4aa962"/>

          <!-- Torta spodok -->
          <rect x="15" y="65" width="70" height="15" fill="#4aa962"/>

          <!-- Torta vrch -->
          <ellipse cx="50" cy="65" rx="35" ry="8" fill="#4aa962"/>

          <!-- Sviečka -->
          <rect x="47" y="35" width="6" height="30" fill="#4aa962"/>

          <!-- Plameň -->
          <ellipse cx="50" cy="30" rx="4" ry="8" fill="#4aa962"/>

          <!-- Biele detaily -->
          <!-- Dekorácia na torte -->
          <circle cx="35" cy="70" r="3" fill="#FFFFFF"/>
          <circle cx="50" cy="68" r="3" fill="#FFFFFF"/>
          <circle cx="65" cy="70" r="3" fill="#FFFFFF"/>

          <!-- Odlesk na plameň -->
          <ellipse cx="48" cy="28" rx="1.5" ry="3" fill="#FFFFFF"/>
        </svg>
        <p >{{ age }} years</p>
      </div>
    </div>

    <div class="flex gap-5">
      <a >CV</a>
      <a href="">
        <svg width="30" height="30" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
          <path d="M50 10C27.909 10 10 27.909 10 50c0 17.696 11.472 32.704 27.396 38.021 2.004.367 2.738-.871 2.738-1.934 0-.954-.035-4.116-.054-7.466-11.129 2.42-13.479-4.717-13.479-4.717-1.821-4.625-4.446-5.858-4.446-5.858-3.634-2.483.275-2.433.275-2.433 4.017.283 6.133 4.125 6.133 4.125 3.571 6.117 9.367 4.35 11.646 3.325.363-2.583 1.396-4.35 2.542-5.35-8.892-1.013-18.238-4.446-18.238-19.788 0-4.371 1.563-7.946 4.125-10.746-.413-1.013-1.788-5.088.392-10.604 0 0 3.363-1.075 11.017 4.104 3.196-.888 6.625-1.333 10.033-1.35 3.404.017 6.838.462 10.042 1.35 7.646-5.179 11.004-4.104 11.004-4.104 2.188 5.516.813 9.591.4 10.604 2.571 2.8 4.121 6.375 4.121 10.746 0 15.392-9.371 18.763-18.296 19.754 1.438 1.238 2.717 3.683 2.717 7.421 0 5.35-.046 9.663-.046 10.975 0 1.071.725 2.321 2.754 1.929C78.546 82.683 90 67.683 90 50 90 27.909 72.091 10 50 10z" fill="white"/>
        </svg>
      </a>
      <a>
        <svg width="30" height="30" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
          <path d="M87.877 87.548H72.897V63.953c0-5.604-.113-12.808-7.799-12.808-7.8 0-8.994 6.091-8.994 12.4V87.55H41.123V38.542h14.365v6.538h.209c1.996-3.781 6.874-7.799 14.148-7.799 15.119 0 17.909 9.952 17.909 22.884V87.548zM22.347 32.003c-4.79 0-8.678-3.916-8.678-8.706S17.557 14.591 22.347 14.591c4.791 0 8.678 3.916 8.678 8.706s-3.887 8.706-8.678 8.706zM29.835 87.548H14.851V38.542h14.984V87.548zM95.359 0H4.634C2.072 0 0 2.071 0 4.634v90.732C0 97.929 2.072 100 4.634 100h90.725c2.562 0 4.641-2.071 4.641-4.634V4.634C100 2.071 97.921 0 95.359 0z" fill="white"/>
        </svg>
      </a>
    </div>
  </section>
</template>
