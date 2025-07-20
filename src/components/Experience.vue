<script setup lang="ts">
import { ref } from 'vue'

  const openTab = (evt: Event, tabName: string) => {
    const tabcontent = document.getElementsByClassName("tabcontent");
    for (let i = 0; i < tabcontent.length; i++) {
      tabcontent[i].classList.add("hidden");
    }

    const tablinks = document.getElementsByTagName("button");
    for (let i = 0; i < tablinks.length; i++) {
      tablinks[i].classList.remove("active:bg-gray-200");
    }

    document.getElementById(tabName)?.classList.remove("hidden");
    (evt.currentTarget as HTMLElement).classList.add("active:bg-gray-200");
  };
</script>

<template>
  <section class="flex justify-center">
    <div class="w-full md:max-w-3xl">
      <div class="flex border-b border-gray-300">
        <button
          class="w-1/2 py-4 text-center font-medium text-gray-100 font-semibold rounded-tl-lg border-2 border-gray-100 focus:outline-none hover:bg-gray-100 hover:text-gray-700"
          @click="openTab($event, 'tab1')"
        >Work</button>
        <button
          class="w-1/2 py-4 text-center font-medium text-gray-100 font-semibold border-2 border-gray-100 rounded-tr-lg focus:outline-none hover:bg-gray-100 hover:text-gray-700"
          @click="openTab($event, 'tab2')"
        >Studies</button>
      </div>
      <div id="tab1" class="tabcontent p-4 space-y-4">
        <div class="flex gap-5">
          <img class="w-[30px] h-[30px] mt-1" src="@/assets/gospace-labs-white.svg">
          <div>
            <h2 class="text-2xl font-bold text-gray-100">Junior Frontend Developer</h2>
            <a class="font-bold text-gray-100 text-lg" target="_blank" href="https://www.gospace.tech/">Gospace labs</a>
            <h3 class="text-gray-100">February 2025 - present</h3>
            <p class="mt-2 text-gray-100">Web development, PHP, Laravel, Vue.js, Tailwind, Alpine.js, Inertia.js</p>
          </div>

        </div>
        <div class="flex gap-5">
          <img class="w-[30px] h-[30px] mt-1" src="@/assets/shieldonelogo.png">
          <div>
            <h2 class="text-2xl font-bold text-gray-100">Junior Developer</h2>
            <a class="font-bold text-gray-100 text-lg" target="_blank" href="https://www.shieldone.sk/">Shieldone</a>
            <h3 class="text-gray-100">June 2023 - May 2025</h3>
            <p class="mt-2 text-gray-100">Web development, Wordpress, Elementor, SCCS, PHP, JS, SEO</p>
          </div>

        </div>

      </div>
      <div id="tab2" class="tabcontent p-4 hidden space-y-4" >
        <div class="flex gap-5">
          <img class="w-[30px] h-[30px] mt-1" src="@/assets/ucm.png">
          <div>
            <h2 class="text-2xl font-bold text-gray-100">Computer science</h2>
            <span class="font-bold text-gray-100 text-lg">Magister degree UCM Trnava</span>
            <h3 class="text-gray-100">September 2025 - Expect May 2027</h3>
          </div>
        </div>
        <div class="flex gap-5">
          <img class="w-[30px] h-[30px] mt-1" src="@/assets/ucm.png">
          <div>
            <h2 class="text-2xl font-bold text-gray-100">Computer science</h2>
            <span class="font-bold text-gray-100 text-lg">Bachalor degree UCM Trnava</span>
            <h3 class="text-gray-100">September 2022 - May 2025</h3>
          </div>
        </div>
        <div class="flex gap-5">
          <img class="w-[30px] h-[30px] mt-1" src="@/assets/spstrnava.png">
          <div>
            <h2 class="text-2xl font-bold text-gray-100">Mechatronics</h2>
            <span class="font-bold text-gray-100 text-lg">SPŠ Trnava</span>
            <h3 class="text-gray-100">September 2018 - May 2022</h3>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>

</style>