<script setup>
import { faMinus, faPlus } from '@fortawesome/free-solid-svg-icons'
import { ref } from 'vue'

const faqs = ref([
  {
    title: 'Eligibility Check',
    response:
      'Ensure you meet the eligibility criteria to join ALCHE before proceeding with your application.',
    status: false,
  },
  {
    title: 'Age Requirement',
    response:
      'Minimum Age: 16 years old.\nApplicants aged 16: Must undergo an interview to assess readiness.\nApplicants aged 17 turning 18 during their first year: No interview required.',
    status: false,
  },
  {
    title: 'Contextual Information',
    response:
      'Indicate any disabilities and required accommodations. Provide details about humanitarian status, if applicable.',
    status: false,
  },
  {
    title: 'Academic History',
    response:
      'Indicate your preferred degree programs and language of instruction. Include test scores if applicable.',
    status: false,
  },
  {
    title: 'Required Documents',
    response:
      'Submit transcripts, English proficiency proof, ID documents. International students need a valid passport.',
    status: false,
  },
])

const toggleFAQ = (index) => {
  faqs.value[index].status = !faqs.value[index].status
}
</script>

<template>
  <section id="Admission" class="overflow-x-hidden">
    <!-- Hero Section -->
    <div class="relative w-full h-screen">
      <img src="/studentstudying.jpg" alt="Students studying" class="w-full h-full object-cover" />
      <div class="absolute inset-0 bg-blue-900/50"></div>
      <h1 class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 text-white text-center text-3xl md:text-5xl">
        APPLICATION AND
        <span class="block text-2xl font-serif italic">ADMISSIONS</span>
      </h1>
    </div>

    <!-- Content -->
    <div class="flex flex-col lg:flex-row px-4 py-10 gap-6 max-w-screen-xl mx-auto overflow-x-hidden">
      <!-- Sidebar Navigation -->
      <div class="relative w-full lg:w-1/3">
        <img src="/admission.jpg" class="w-full h-auto rounded-md" alt="Admission" />
        <div class="absolute top-20 left-0 w-full flex justify-center px-2">
          <div class="bg-[#00A0DE] text-white p-6 rounded-lg shadow-md w-11/12 md:w-3/4 space-y-4">
            <a href="#application">Application & Admissions Process</a>
            <hr />
            <a href="#Eligibility">Eligibility Requirements</a>
            <hr />
            <a href="#InternationalRequirements">International Students Requirements</a>
          </div>
        </div>
      </div>

      <!-- Main Content -->
      <div class="w-full lg:w-2/3 space-y-10">
        <!-- Application Process -->
        <section id="application">
          <h2 class="text-[#002E6D] text-3xl md:text-4xl">Application & Admission Process</h2>
          <hr class="border-2 border-blue-600 w-full" />
          <p>The application process to ALCHE Mauritius is outlined below:</p>

          <!-- FAQ Accordion -->
          <div v-for="(faq, index) in faqs" :key="index" class="mt-4">
            <button
              @click="toggleFAQ(index)"
              class="w-full text-left bg-blue-100 text-blue-700 p-3 rounded-md flex items-center justify-between"
            >
              <span>{{ faq.title }}</span>
              <font-awesome-icon :icon="faq.status ? faMinus : faPlus" />
            </button>
            <div v-if="faq.status" class="bg-blue-600 text-white p-4 rounded-md mt-1 whitespace-pre-wrap">
              {{ faq.response }}
            </div>
          </div>
        </section>

        <!-- Eligibility Section -->
        <section id="Eligibility">
          <h2 class="text-2xl text-[#002E6D] font-bold mt-8">Eligibility Requirements</h2>
          <hr class="border-2 w-1/2 border-blue-600 my-2" />
          <p>To be eligible for admission to ALCHE, applicants must meet one of the following:</p>

          <div
            v-for="(option, i) in ['Option 1', 'Option 2', 'Option 3']"
            :key="i"
            class="bg-[#798C97] text-white p-4 rounded-lg shadow-md mt-4"
          >
            <h3 class="text-2xl font-semibold">{{ option }}</h3>
            <ul class="list-disc pl-5 mt-2">
              <li v-if="i === 0">Pass in 3 subjects at A-level</li>
              <li v-if="i === 0">+ 1 subject at Subsidiary level (HSC or equivalent)</li>

              <li v-if="i === 1">Pass in 2 subjects at A-level</li>
              <li v-if="i === 1">+ 2 subjects at Subsidiary level (HSC or equivalent)</li>

              <li v-if="i === 2">Pass in 3 A-level subjects (GCE or equivalent)</li>
            </ul>
          </div>
        </section>

        <!-- International Table -->
        <section id="InternationalRequirements" class="overflow-auto">
          <h2 class="text-2xl text-[#002E6D] font-bold mt-8">International Requirements</h2>
          <hr class="border-2 w-1/2 border-blue-600 my-2" />

          <table class="w-full text-left text-sm border border-blue-600 min-w-[600px]">
            <thead class="bg-[#10253E] text-white">
              <tr>
                <th class="border border-blue-600 p-2">Certificate</th>
                <th class="border border-blue-600 p-2">Country</th>
                <th class="border border-blue-600 p-2">Minimum Requirements</th>
                <th class="border border-blue-600 p-2">Programme Requirements (BSE & BCS)</th>
              </tr>
            </thead>
            <tbody>
              <tr class="bg-white">
                <td class="border border-[#F5A801] p-2">Cambridge Higher School Certificate</td>
                <td class="border border-[#F5A801] p-2">International</td>
                <td class="border border-[#F5A801] p-2">
                  21 points at HSC/GCE ‘A’ Level based on 3 subjects. A*=10, A=9, B=8, ..., E=5.
                </td>
                <td class="border border-[#F5A801] p-2">Math or STEM subject at Grade C or above</td>
              </tr>
              <tr class="bg-gray-50">
                <td class="border border-[#F5A801] p-2">International Baccalaureate (IB)</td>
                <td class="border border-[#F5A801] p-2">International</td>
                <td class="border border-[#F5A801] p-2">
                  Min. 28 points overall, 15 points from 3 HL subjects. No fixed SL requirement.
                </td>
                <td class="border border-[#F5A801] p-2">STEM subject at HL with 4 or higher</td>
              </tr>
              <tr class="bg-white">
                <td class="border border-[#F5A801] p-2">University Entrance Exam Certificate</td>
                <td class="border border-[#F5A801] p-2">Ethiopia</td>
                <td class="border border-[#F5A801] p-2">
                  Option 1: 7 subjects, min. 60% each, total ≥ 560.<br />
                  Option 2: 6 subjects ≥ 50%, total ≥ 335 + 1st year of uni with GPA 3.0/B.
                </td>
                <td class="border border-[#F5A801] p-2">
                  At least 80% in Math and Sciences (Chemistry, Physics)
                </td>
              </tr>
            </tbody>
          </table>
        </section>
      </div>
    </div>
  </section>
</template>
