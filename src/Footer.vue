<script setup>

</script>


<template>
  <section id="Footer">
    <div class=" bg-[#10253E] w-full text-amber-50 flex flex-col md:flex-row justify-between items-center p-4 gap-2">
    <div class="flex  flex-col justify-between items-center p-4">
     
      <a href="#home">Return Home</a>
    </div>

    <div>
      
     
      <!-- Navigation Menu -->
      <div class=" flex flex-col md:flex-row justify-between items-center bg-[#10253E] gap-5 text-amber-50"
      >
        <a href="#About">About</a>
        <a href="#Program">Programmes</a>
        <a href="#Admission">Admission Process</a>
        <a href="#Scholarship">Scholarship</a>
      </div>
    </div>

    <slot></slot>
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
