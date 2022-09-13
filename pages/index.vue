<template>
  <div>
     <div class="px-4 py-22 h-full mx-auto lg:gap-8 xl:gap-0 lg:py-16 bg-hero" >
        <div class="mr-auto place-self-center lg:col-span-7">
            <h1 class="max-w-2xl mb-4 text-4xl font-medium tracking-tight leading-none md:text-5xl xl:text-6xl ">Bring the power of <b>aroma</b>
              to your retail experiences.</h1>
            <p class="max-w-2xl mb-6 font-light text-gray-500 text-sm lg:mb-8  lg:text-xl ">iScent helps brands design one-of-one olfactory experiences
That positively impact customer dwell time, foot traffic, return visits, and helps you craft a
memorable experience for all who interact with your brand</p>
            <a href="#" class="inline-flex items-center justify-center px-5 py-3 text-base font-medium text-center text-white border bg-black border-black rounded-lg hover:bg-white hover:text-black focus:ring-4 focus:ring-white">
              SCHEDULE CONSULTATION
            </a> 
        </div>
      </div>
        <div class="container">
          <h2 class="text-xl font-bold text-center text-black mt-5 mb-2 lg:text-4xl">The iScent Difference</h2>
          <p class="text-lg text-center lg:text-md">Custom-tailored auromas built from <b>ground-up.</b>
            <br/>No white labeling. Our <b>customer experience</b> is unparalleled. 
            <br/>Only supreme <b>quality ingredients.</b> Sourced by us. </p>
        </div>          

        <VueSlickCaraousel v-bind="settings">
          <div class="flex flex-row">
          <div class="flex flex-col justify-center items-center justify-self-center mx-auto lg:mx-10 ">
            <img src="../assets/image/delivery-w.png"
            alt="delivery"
            class="rounded-full w-20 h-20 z-50 opacity-1 transition-opacity invert hover:invert-0 hover:bg-black"/>
              <h2 class="text-md font-bold text-center">RETAIL</h2>
          </div>
         </div>

         <div class="flex flex-row">
         <div class="flex flex-col items-center justify-self-center mx-auto lg:mx-10">
            <img src="../assets/image/fragrence-w.png"
            alt="delivery"
            class="rounded-full w-20 h-20 z-50 opacity-1 transition-opacity invert hover:invert-0 hover:bg-black"/>
              <h2 class="text-md font-bold text-center">OFFICES</h2>
          </div>
        </div>
         
          <div class="flex flex-row">
          <div class="flex flex-col items-center justify-self-center mx-auto lg:mx-10">
            <img src="../assets/image/schedule-w.png"
            alt="delivery"
            class="rounded-full w-20 h-20 z-50 opacity-1 transition-opacity invert hover:invert-0 hover:bg-black"/>
              <h2 class="text-md font-bold text-center">HOTELS</h2>
          </div>
        </div>
         
          <div class="flex flex-row">
          <div class="flex flex-col items-center justify-self-center mx-auto lg:mx-10">
            <img src="../assets/image/schedule-w.png"
            alt="delivery"
            class="rounded-full w-20 h-20 z-50 opacity-1 transition-opacity invert hover:invert-0 hover:bg-black"/>
              <h2 class="text-md font-bold text-center">HEALTHCARE AND SPAS</h2>
          </div>
        </div>
         
          <div class="flex flex-row">
          <div class="flex flex-col items-center justify-self-center mx-auto lg:mx-10">
            <img src="../assets/image/schedule-w.png"
            alt="delivery"
            class="rounded-full w-20 h-20 z-50 opacity-1 transition-opacity invert hover:invert-0 hover:bg-black"/>
              <h2 class="text-md font-bold text-center">PROPERTY MANAGEMENT</h2>
          </div>
        </div>
         
          <div class="flex flex-row">
          <div class="flex flex-col items-center mx-auto lg:mx-10">
            <img src="../assets/image/schedule-w.png"
            alt="delivery"
            class="rounded-full w-20 h-20 z-50 opacity-1 transition-opacity invert hover:invert-0 hover:bg-black"/>
              <h2 class="text-md font-bold text-center">CAR SHOWROOMS</h2>
          </div>
        </div>
      </VueSlickCaraousel>

      <OurAroma/>
      <SuccesStories />
      <ContactUs />
    </div>
</template>

<script>
import OurAroma from '../components/OurAroma.vue';
import SuccesStories from '../components/SuccesStories.vue';
import ContactUs from '../components/ContactUs.vue';
import VueSlickCaraousel from 'vue-slick-carousel'

export default {
    name: "IndexPage",
    layouts: "default",
    components: { OurAroma, SuccesStories, ContactUs, VueSlickCaraousel },
    data() {
        return {
            showModal: false,
           settings : {
            dots: true,
            infinite: true,
            rows: 1,
            initialSlide: 2,
            speed: 500,
            slidesToShow: 6,
            slidesToScroll: 2,
            swipeToSlide: true,
            arrows: true,
            responsive: [
            {
            "breakpoint": 1024,
            "settings": {
                "slidesToShow": 3,
                "slidesToScroll": 3,
                "infinite": true,
                "dots": true
            }
            },
            {
            "breakpoint": 600,
            "settings": {
                "slidesToShow": 3,
                "slidesToScroll": 3,
                "initialSlide": 3
            }
            },
            {
            "breakpoint": 480,
            "settings": {
                "dots" : false,
                "slidesToShow": 2,
                "slidesToScroll": 2
            }
            }
        ]
        }
                };
            }
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
