<script setup>
</script>

<template>
  <section id="About" class="mt-16 px-6 md:px-12 lg:px-24">
    <div class="flex flex-col md:flex-row items-center justify-between gap-8">
      
      <!-- Image Container with Overlay -->
      <div class="relative w-full md:w-1/2 h-[400px] md:h-[500px] overflow-hidden rounded-lg shadow-lg">
        <img src="/About.jpg" alt="About ALCHE" class="w-full h-full object-cover">
        <div class="absolute inset-0 bg-black/50"></div>
        <h1 class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 text-white text-4xl font-extrabold text-center">
          About ALCHE
        </h1>
      </div>

      <!-- Text Content -->
      <div class="w-full md:w-1/2 space-y-6">
        <p class="text-lg text-gray-700 leading-relaxed">
          African Leadership College of Higher Education (ALCHE) prepares students for a life of purpose, leadership, and impact in the world – from day one. Through our mission-driven and experiential learning model, students at ALCHE engage in purpose-driven education, actively seeking meaning and impact in every aspect of their studies and activities.
        </p>
        
        <p class="text-lg text-gray-700 leading-relaxed">
          We believe that life is a continuous journey of discovery — both of the world and your place within it. Here, you will appreciate what you understand and identify what remains to be learned, always pushing the boundaries of your knowledge. Your destination is not just a bachelor’s degree but a new way of seeing and impacting the world.
        </p>

        <!-- Mission Statement -->
        <div class="bg-blue-900 text-white p-6 rounded-lg shadow-md">
          <h2 class="text-xl font-semibold uppercase">Our Mission</h2>
          <p class="text-lg mt-2">
            To develop millions of ethical entrepreneurial leaders for the African continent.
          </p>
        </div>
      </div>

    </div>
  </section>
</template>
