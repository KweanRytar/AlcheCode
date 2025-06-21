<script setup>
import { ref, onMounted, onUnmounted } from 'vue';
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
import { faBars, faXmark } from '@fortawesome/free-solid-svg-icons';

const isMenuOpen = ref(false);
const isScrolled = ref(false);

const toggle = () => {
  isMenuOpen.value = !isMenuOpen.value;
};

// Function to handle scroll event
const handleScroll = () => {
  isScrolled.value = window.scrollY > 50; // If scrolled more than 50px
};

// Attach scroll event when component mounts
onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

// Remove event listener when component unmounts
onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});
</script>


<template>
  <section id="home" class="mb-20" >
    <div class=" bg-[#10253E] w-full text-amber-50 flex flex-col md:flex-row justify-between items-center p-4 gap-2 fixed top-0 left-0 z-50 ">
    <div class="flex  flex-col justify-between items-center p-4">
      <h1>Alche</h1>
      <a href="#home">LEADERSHIP COLLEGE OF HIGHER EDUCATION</a>
    </div>

    <div>
      <!-- Toggle Button -->
      <button 
        class="text-2xl p-2 rounded-md md:hidden cursor-pointer bg-transparent" 
        @click="toggle"
      >
        <font-awesome-icon :icon="isMenuOpen ? faXmark : faBars" />
      </button>

      <!-- Navigation Menu -->
      <div 
        :class="{
          'flex flex-col md:flex-row justify-between items-center bg-[#10253E] gap-5 text-amber-50 ' : true,
          'hidden': !isMenuOpen,
          'md:flex': true
        }"
      >
        <a href="#About">About</a>
        <a href="#Program">Programmes</a>
        <a href="#Admission">Admission Process</a>
        <a href="#Scholarship">Scholarship</a>
      </div>
    </div>

    <a href="https://alcheducation.com/apply-now/" class=" mt-4 w-24 p-2 text-[#10253E] border-l-4 border-r-0 border-t-0 border-b-0 border-[#F5A801] bg-amber-50 hover:text-[#F5A801] ">Apply now</a>
  </div>
  </section>
  
</template> 

<style scoped>
@media (max-width: 768px) {
  .hidden {
    display: none;
  }
}
</style>
