<template>
  <div>
     <div class="px-4 py-8 mx-auto lg:gap-8 xl:gap-0 lg:py-16 bg-hero" >
        <div class="mr-auto place-self-center lg:col-span-7">
            <h1 class="max-w-2xl mb-4 text-4xl font-medium tracking-tight leading-none md:text-5xl xl:text-6xl dark:text-white">Bring the power of <strong>aroma</strong>
              to your retail experiences.</h1>
            <p class="max-w-2xl mb-6 font-light text-gray-500 text-sm lg:mb-8  lg:text-xl dark:text-gray-400">iScent helps brands design one-of-one olfactory experiences
That positively impact customer dwell time, foot traffic, return visits, and helps you craft a
memorable experience for all who interact with your brand</p>
            <a href="#" class="inline-flex items-center justify-center px-5 py-3 text-base font-medium text-center text-white border bg-black border-black rounded-lg hover:bg-white hover:text-black focus:ring-4 focus:ring-white">
              SCHEDULE CONSULTATION
            </a> 
        </div>
      </div>
        <div class="container">
          <h2 class="text-xl font-bold text-center text-black mt-5 mb-2 lg:text-6xl">The iScent Difference</h2>
          <p class="text-sm text-center lg:text-md">Custom-tailored auromas built from <strong>ground-up.</strong>
            <br/>No white labeling. Our <strong>customer experience</strong> is unparalleled. 
            <br/>Only supreme <strrong>quality ingredients.</strrong> Sourced by us. </p>
        </div>                
        <div class="flex flex-row justify-center gap-2 mt-5 mb-10  snap-x">
          <div class="flex flex-col justify-center justify-self-center mx-auto lg:mx-10 ">
            <img src="../assets/image/delivery-w.png"
            alt="delivery"
            class="rounded-full w-20 h-20 z-50 opacity-1 transition-opacity invert hover:invert-0 hover:bg-black"/>
              <h2 class="text-md font-bold text-center">RETAIL</h2>
          </div>
          <div class="flex flex-col justify-center justify-self-center mx-auto lg:mx-10">
            <img src="../assets/image/fragrence-w.png"
            alt="delivery"
            class="rounded-full w-20 h-20 z-50 opacity-1 transition-opacity invert hover:invert-0 hover:bg-black"/>
              <h2 class="text-md font-bold text-center">RETAIL</h2>
          </div>
          <div class="flex flex-col justify-center justify-self-center mx-auto lg:mx-10">
            <img src="../assets/image/schedule-w.png"
            alt="delivery"
            class="rounded-full w-20 h-20 z-50 opacity-1 transition-opacity invert hover:invert-0 hover:bg-black"/>
              <h2 class="text-md font-bold text-center">RETAIL</h2>
          </div>
        </div>
      <OurAroma/>
      <SuccesStories />
      <ContactUs />
    </div>
</template>

<script>
import OurAroma from '../components/OurAroma.vue';
import SuccesStories from '../components/SuccesStories.vue';
import ContactUs from '../components/ContactUs.vue';
export default {
    name: "IndexPage",
    layouts: "default",
    components: { OurAroma, SuccesStories, ContactUs }
}
</script>

<style scoped>
  .bg-hero {
    background-image: url("~/assets/image/hero.png");
    background-size: cover;
    background-repeat: round;
    margin:auto;
  }
  </style>
