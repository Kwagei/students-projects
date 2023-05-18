<template>
  <div>
    <HeaderVue />
    <main class=" bg-no-repeat bg-cover bg-fixed bg-[url(/img/vertical-page-bg.jpg)]">
      <div>
        <!-- Hero card -->
        <HeroSection/>
        <!-- Logo cloud -->
        <div>
          <div class="mx-auto max-w-7xl p-6 lg:px-8"> 
              <h2 class="text-3xl text-center font-bold tracking-tight text-white sm:text-4xl">Meet our cohorts</h2>
              <hr class="text-gray-100 mt-5 border-neutral-500">
              </div> 
        </div>
      </div> 

      <!-- More main page content here... -->
      <CohortCards />

      <!-- CTA -->
      <CTA/>
      <hr class="text-gray-100 mt-5 border-neutral-500">

    </main>
  </div>
</template>

<script setup>

import CTA from '../components/CTA.vue';
import CohortCards from '../components/CohortCards.vue'
import HeaderVue from '../components/HeaderVue.vue'
import HeroSection from '../components/HeroSection.vue';
</script>