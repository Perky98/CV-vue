<script setup lang="ts">

import Myweb from '@/components/Projects/Myweb.vue'
</script>

<template>
  <section class="mx-auto w-full max-w-3xl  ">
      <h2 class="text-center md:text-left  text-3xl font-bold my-8">Projects</h2>
    <div class="grid gap-8 grid-cols-1 md:grid-cols-2">
      <myweb link="https://www.finpomb.sk/" image="" name="FinpoMB" technology="PHP, SCSS, Wordpress, Javascript"/>
      <myweb link="https://www.parkingaround.com/" image="" name="ParkingAround" technology="PHP, Laravel, AlpineJS, Tailwind, VueJS"/>
      <myweb link="https://www.bazeny-viking.sk/" image="" name="Bazeny Viking" technology="PHP, SCSS, Wordpress, Javascript"/>
      <myweb link="https://www.tekoldany.sk/" image="" name="Tekoldany" technology="Wordpress Elementor, SCSS"/>
      <myweb link="https://www.bielakocka.sk/" image="" name="Biela kocka" technology="Wordpress Elementor"/>
      <myweb link="https://aikido-suchdol.cz/" image="" name="Aikido Dojo Suchdol nad Odrou" technology="Wordpress Elementor, CSS"/>
      <myweb link="https://www.goldeneagle.sk/" image="" name="Hotel Golden Eagle" technology="Wordpress Elementor, SCSS"/>
      <myweb link="https://www.profipotrubie.sk/" image="" name="Profipotrubie" technology="Wordpress Elementor, SCSS"/>
      <myweb link="https://www.georadar.sk/" image="" name="GeoRadar" technology="Wordpress Elementor"/>
      <myweb link="https://www.krtkofix.sk/" image="" name="Krtkofix" technology="Wordpress Elementor"/>
      <myweb link="https://www.strechybartko.sk/" image="" name="Strechy Bartko" technology="Wordpress Elementor, SCSS"/>
    </div>

  </section>
</template>