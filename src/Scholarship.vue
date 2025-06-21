<script setup>
import { faMinus, faPlus } from '@fortawesome/free-solid-svg-icons'
import {ref} from 'vue'
const faqs = ref([
    {
        title: "Requirement 1", 
        response: "Applicants must be otherwise unable to afford ALCHE tuition with any other form of aid. Individuals must demonstrate financial need and substantial socio-economic disadvantage, which acceptable official supporting documents can clearly verify.",
        status: false
    }, {
        title: "Requirement 2",
        response: "Individuals meeting the following descriptions are especially encouraged to apply;a. Female applicants. b. Individuals with physical or learning disabilities (see the various definitions of disabilities here and here).c. Aged 26 and below",
        status: false

    },{
        title: "Requirement 3",
        response: "Be academically strong with clear potential to thrive at ALCHE Meet ALCHE admission criteria Strong National Exam Scores of at least a B average",
        status: false

    }
]) 

const showfaq = (index) => {
    faqs.value[index].status = !faqs.value[index].status

}
</script>

<template>
<section id="Scholarship">
    <div class="mainContainer">
    <div class="firstLine">
        <div class="relative w-full h-screen object-cover">
                <img src="/studentstudying.jpg" alt="students studying" class="w-full h-screen object-cover" />
                <div class="absolute inset-0 bg-blue-900/50"></div>
                <h1 class="text-3xl absolute top-1/5 text-white text-center">Mastercard Foundation Scholars Program
                </h1 >
    <div class="absolute top-50 w-full flex flex-row justify-around items-center gap-4">
        <div>
            <img src="/masterCard.png" alt="students studying" class=" w-80 hidden md:block" />
        </div>
              <div>
                <p class=" text-white md:text-2xl">One of our objectives at ALCHE is to make education accessible to potential future leaders across the continent from disadvantaged backgrounds by reducing the barriers between prospective students and their post-secondary education.</p>
              </div>      
                   
                </div>
                
            </div>

    </div>
    <div class="imageBearer w-full grid grid-cols-1 md:grid-cols-4 relative">
        <div class=" col-span-3">
            <img src="/SCHOLARSHIP-2.jpg" alt="students studying" class="w-full h-auto object-cover rounded-3xl mt-4"  />
        </div>
<div class=" bg-[#B62227] rounded-3xl p-6 h-fit md:mt-40 md:absolute md:left-90">
<p class=" text-white font-mono">ALCHE, in partnership with the Mastercard Foundation, is proud to offer the Mastercard Foundation Scholars Program, which provides fully-funded scholarships to exceptionally deserving and talented students across the continent. These full-ride scholarships are awarded to students who demonstrate financial need, academic excellence, and great leadership potential in using the scholarship opportunity as a valuable tool in making a meaningful impact in their community.</p>
      

</div>

    </div>
<div class="secondToLastCarrier bg-gradient-to-r from-[#EF481C] via-[#F4971C] to-[#F2801C] w-full rounded-2xl flex flex-col md:p-6 md:flex-row lg:pr-20">
    <div class="image object-cover md:flex-[2] ">
<img src="/SCHOLARSHIP-2.jpg"/>
    </div>

    <div class="centerText bg-[#01A0AE] text-white rounded-2xl p-4 w-full md:flex-[1] lg:flex-[1]">
        <h1 class="text-white font-mono text-2xl">Our program follows this major principle:</h1>
    <p>The Scholars’ Program at ALCHE is based primarily on demonstrated financial need and high academic achievement but is also subject to meeting all other eligibility requirements and availability.</p>

    </div >
    
    <div class="secondText rounded-2xl bg-white w-full p-2 md:flex-[3] lg:flex-[1.5]">
<p>To be eligible to apply for a scholarship, one must first meet the ALCHE Admissions requirements. If eligible for admission to ALCHE, an applicant will be required to provide additional information during their application which will be used to determine their eligibility for the Mastercard Foundation Scholars program.  <span class="block m-2">The Mastercard Foundation Scholarships offered at ALCHE are full-ride scholarships covering full tuition and additional financial support throughout the scholars’ journey at ALCHE. </span ></p>
<p class="w-full bg-[#F5A801] p-2 text-white text-2xl font-sans rounded-2xl"> <font-awesome-icon :icon="['fas', 'circle-info']" class="mr-2 text-white text-3xl "/>Please note that very limited scholarships are available per intake.</p>
    </div>
</div>
<div class="eligibility bg-[#B62227] ">
<h1 class="text-3xl text-white font-extrabold text-center p-2">Eligibility Requirements for the
    Mastercard Foundation Scholarships</h1>
<h1 class="  text-white text-center font-semibold text-2xl">Mastercard Foundation Scholarships</h1>
<div v-for="(faq, index) in faqs" :key="index" class="pr-4 pl-4 ">
<h1 @click="showfaq(index)" class=" cursor-pointer text-blue-600  border-0 bg-blue-100 w-full m-0 p-4"><span >
    <font-awesome-icon :icon=" faq.status === true ? faMinus  : faPlus"  class=" text-blue-600 "/>

</span>{{ faq.title }}</h1>
<p v-if="faq.status === true" class=" border-0  font-extralight bg-transparent text-white rounded-2xl p-2">{{ faq.response }}</p>
                </div>
</div> 
<div class="bg-[#01A0AE] w-fit justify-center flex flex-col md:flex-row mt-4"> 
    <p class=" font-bold uppercase text-white text-2xl text-center lg:text-2xl p-2 justify-center">Scholarship <span class="font-extrabold text-3xl text-white md:text-4xl lg:text-6xl text-center">Application Journey</span></p>
    <h4 class="text-white font-bold text-2xl text-center">Here’s a quick glance at our Scholarship Application Journey</h4>
</div>
<div class="flex flex-col md:flex-row gap-2  ">
    <div class="shadow-2xl shadow-blue-300 rounded-3xl p-6 bg-white">
        <h1 class="text-gray-400 text-2xl p-2">Step 1: Apply for Admission to ALCHE</h1>
        <p class="relative pb-2 after:content-[''] after:absolute after:left-0 after:bottom-0 after:w-full after:h-0.5 after:bg-blue-600 after:scale-x-50 after:transition-transform after:duration-300 hover:after:scale-x-100 m-1.5">Applicants must first begin an admissions application to ALCHE. Only applicants eligible for admission to ALCHE will be allowed to apply for the Scholarship. 

You may start your Admissions application here.</p>
    </div>
    <div class="shadow-2xl shadow-blue-300 rounded-3xl p-6 bg-white">
        <h1 class="text-gray-400 text-2xl p-2">Step 2: Eligibility Check</h1>
        <p class="relative pb-2 after:content-[''] after:absolute after:left-0 after:bottom-0 after:w-full after:h-0.5 after:bg-blue-600 after:scale-x-50 after:transition-transform after:duration-300 hover:after:scale-x-100">
  The first part of the scholarship application process would be to submit some information that would be used to determine a candidate’s eligibility for the scholarship. Only candidates who are eligible will proceed to the next step of the application process.
</p>

    </div>
</div>
    </div>
</section>
    
</template>