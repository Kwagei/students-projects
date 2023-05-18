<script setup>
import { RouterLink, RouterView } from 'vue-router' 
import FooterVue from './components/FooterVue.vue'

</script>

<template>
  <div class="font-sans">
    <!-- <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" /> -->
  <RouterView />
  <FooterVue />
  </div>
</template>