<script setup>
import { ref } from 'vue';
const videoLink = ref('/Homevideo.mp4');


</script>
<template>
<section>
    <div class="relative w-full h-screen overflow-hidden">
      <!-- Background Video -->
      <video autoplay loop muted playsinline class="absolute top-0 left-0 w-full h-full object-cover">
        <source src="/Homevideo.mp4" type="video/mp4" />
        Your browser does not support the video tag.
      </video>

      <!-- Blue Overlay -->
      <div class="absolute inset-0 bg-blue-900/50"></div>

      <!-- Overlay Content -->
      <div class="absolute inset-0 flex flex-col items-center justify-center text-white">
        <h1 class="text-4xl font-bold">An education that gives Limitless Opportunities</h1>
        <p class="text-lg mt-2">Discover opportunities you never imagined; from exchange programs, visiting faculty, diverse network to an innovative learning model, a LIMITLESS education awaits you at ALCHE.</p>
        <a href="#/Program" class=" mt-0 w-38 p-2 text-[#10253E] border-l-4 border-r-0 border-t-0 border-b-0 border-[#F5A801] bg-amber-50 hover:text-[#F5A801]" >EXPLORE PROGRAMS</a>
      </div>
    </div>
  </section>
</template>