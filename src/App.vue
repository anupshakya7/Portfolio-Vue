<template>
  <div class="min-h-screen">
    <!-- Wrap components in Suspense to handle loading -->
     <Suspense>
      <template #default>
        <div class="bg-primary2">
          <HeroSection/>
        </div>
      </template>
      <template #fallback>
        <div class="flex justify-center items-center min-h-screen">
          <LoadingSpinner/>
        </div>
      </template>
     </Suspense>
  </div>
  
</template>
<script setup>
import {defineAsyncComponent} from 'vue';
import AOS from 'aos';
import 'aos/dist/aos.css';
AOS.init({duration:2000,delay:200});
import LoadingSpinner from './components/LoadingSpinner.vue'
const HeroSection = defineAsyncComponent(()=>import('./components/HeroSection.vue'));
</script>
<style lang="">

</style>
