<script setup lang="ts">
import { ref } from 'vue'
import Work from '@/components/Experience/Work.vue'
import Edu from '@/components/Experience/Edu.vue'

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
  <section class="flex justify-center px-3 md:px-0">
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
        <Work title="Junior Frontend Developer" link="https://www.gospace.tech/" image="gospace-labs-white.svg" durations="February 2025 - present" technologies="Web development, PHP, Laravel, Vue.js, Tailwind, Alpine.js, Inertia.js" name="Gospace labs" />
        <Work title="Junior Developer" link="https://www.shieldone.sk/" image="shieldonelogo.png" durations="June 2023 - May 2025" technologies="Web development, Wordpress, Elementor, SCCS, PHP, JS, SEO" name="Shieldone" />

      </div>
      <div id="tab2" class="tabcontent p-4 hidden space-y-4" >
        <edu title="Computer science" image="ucm.png" durations="September 2025 - Expect May 2027" name="Magister degree UCM Trnava" />
        <edu title="Computer science" image="ucm.png" durations="September 2022 - May 2025" name="Bachalor degree UCM Trnava" />
        <edu title="Mechatronics" image="spstrnava.png" durations="September 2018 - May 2022" name="SPŠ Trnava" />

      </div>
    </div>
  </section>
</template>

<style scoped>

</style>