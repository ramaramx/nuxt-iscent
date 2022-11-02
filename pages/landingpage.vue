<template>
    <div>
       <div class="h-screen py-10  mx-auto  lg:py-20 bg-hero" >
          <div class=" flex flex-col justify-center items-center  px-10 mt-52">
              <h1 class="max-w-2xl mb-4 text-2xl text-center text-white font-semibold md:text-5xl xl:text-6xl uppercase">Bring the power of aroma
                to your retail experiences.</h1>
              <p class="max-w-2xl mb-6 font-normal text-white text-center text-sm lg:mb-8  lg:text-xl ">iScent helps brands design one-of-one olfactory experiences
              That positively impact customer dwell time, foot traffic, return visits, and helps you craft a memorable experience for all who interact with your brand
              </p>
            
            <div class="flex flex-row gap-x-5">
            <button @click="scrollToAnchorPoint('started')" class="inline-flex items-center justify-center px-5 py-3 text-base font-medium text-center text-white border bg-black border-black rounded-lg hover:bg-white hover:text-black transition ease">
                Get Started
            </button>
            
            <button @click="scrollToAnchorPoint('contact')" class="inline-flex items-center justify-center px-5 py-3 text-base font-medium text-center text-white border bg-black border-black rounded-lg hover:bg-white hover:text-black transition ease">
                Schedule Now
            </button>

          </div>
          
          </div>
        </div>


          <div class="container mx-auto py-14" >
            <h2 class="text-2xl font-bold text-center text-black mb-2 lg:text-6xl">The iScent Difference</h2>
            <p class="text-base text-center lg:text-lg pt-5">1. Custom-tailored auromas built from <b>ground-up.</b>
              <br/>2. No white labeling. Our <b>customer experience</b> is unparalleled. 
              <br/>3. Only supreme <b>quality ingredients.</b> Sourced by us. </p>

        </div>          
          
          <!-- <div>
            <h1 class="text-xl font-bold text-center text-black mt-5 mb-2 lg:text-4xl lg:mx-[500px]">Creating Signature Scents For Business</h1>
            <p class="text-base text-center lg:text-lg">Give your business its own scent identity with captivating and unique fragrance compositions. With a wide range of customizable fragrances, we develop industry-centric scent marketing solutions for businesses of all types.</p>
          </div> -->
  
          <VueSlickCaraousel v-bind="settings">
            <div class="flex flex-row">
              <div class="flex flex-col justify-center items-center  mx-auto lg:mx-10 transform transition duration-500 hover:scale-110">
                <img src="../assets/image/supermarket.png"
                alt="delivery"
                class=" w-20 h-20 z-50  "/>
                  <h2 class="text-lg font-semibold text-center">RETAIL</h2>
              </div>
           </div>
  
           <div class="flex flex-row">
            <div class="flex flex-col justify-center items-center  mx-auto lg:mx-10 transform transition duration-500 hover:scale-110">
              <img src="../assets/image/building.png"
              alt="delivery"
              class=" w-20 h-20 z-50  "/>
                <h2 class="text-lg font-semibold text-center">OFFICES</h2>
            </div>
          </div>
           
            <div class="flex flex-row">
              <div class="flex flex-col justify-center items-center  mx-auto lg:mx-10 transform transition duration-500 hover:scale-110">
              <img src="../assets/image/resort.png"
              alt="delivery"
              class=" w-20 h-20 z-50  "/>
                <h2 class="text-lg font-semibold text-center">HOTELS</h2>
            </div>
          </div>
           
            <div class="flex flex-row">
              <div class="flex flex-col justify-center items-center  mx-auto lg:mx-10 transform transition duration-500 hover:scale-110">
              <img src="../assets/image/healthcare.png"
              alt="delivery"
              class=" w-20 h-20 z-50  "/>
                <h2 class="text-lg font-semibold text-center">HEALTHCARE AND SPAS</h2>
            </div>
          </div>
           
            <div class="flex flex-row">
              <div class="flex flex-col justify-center items-center  mx-auto lg:mx-10 transform transition duration-500 hover:scale-110">
              <img src="../assets/image/property.png"
              alt="delivery"
              class=" w-20 h-20 z-50  "/>
                <h2 class="text-lg font-semibold text-center">PROPERTY MANAGEMENT</h2>
            </div>
          </div>
           
            <div class="flex flex-row">
              <div class="flex flex-col justify-center items-center  mx-auto lg:mx-10 transform transition duration-500 hover:scale-110">
              <img src="../assets/image/showroom.png"
              alt="delivery"
              class=" w-20 h-20 z-50  "/>
                <h2 class="text-lg font-semibold text-center">CAR SHOWROOMS</h2>
            </div>
          </div>
        </VueSlickCaraousel>
        
        <div ref="started">
        <OurAroma2 />
      </div>
        
        <SuccessStories2 />
        <div ref="contact">
        <ContactUs />
        
        <!-- <section class="bg-white dark:bg-gray-900">
          <div class="gap-8 items-center py-8 px-4 mx-auto max-w-screen-xl xl:gap-16 md:grid md:grid-cols-2 sm:py-16 lg:px-6">
              <img class="w-full dark:hidden" src="https://flowbite.s3.amazonaws.com/blocks/marketing-ui/cta/cta-dashboard-mockup.svg" alt="dashboard image">
              <img class="w-full hidden dark:block" src="https://flowbite.s3.amazonaws.com/blocks/marketing-ui/cta/cta-dashboard-mockup-dark.svg" alt="dashboard image">
              <div class="mt-4 md:mt-0">
                  <h2 class="mb-4 text-4xl tracking-tight font-extrabold text-gray-900 dark:text-white">Choose From Our Vast Collection of Fragrances or Create Your Own Signature Scent</h2>
                  <p class="mb-6 font-light text-gray-500 md:text-lg dark:text-gray-400">Schedule Free Consultation Now</p>
                  <a href="#" class="inline-flex items-center font-medium rounded-lg border text-sm px-5 py-2.5 text-center text-white bg-black hover:bg-white hover:text-black hover:border-black focus:ring-4 focus:ring-primary-300  transition ease-in">
                      Get started
                      <svg class="ml-2 -mr-1 w-5 h-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
                  </a>
              </div>
          </div>
      </section> -->

      </div>
    </div>
  </template>
  
  <script>
import ContactUs from '../components/ContactUs.vue';
import VueSlickCaraousel from 'vue-slick-carousel'
import OurAroma2 from '../components/OurAroma2.vue';
import SuccessStories2 from '../components/SuccessStories2.vue';
  
  export default {
      name: 'landingpage',
      layout: 'noloading',
      components: {  ContactUs, VueSlickCaraousel, OurAroma2, SuccessStories2 },
  
      data() {
          return {
            
              showModal: false,
             settings : {
              dots: true,
              infinite: true,
              rows: 1,
              initialSlide: 2,
              speed: 800,
              slidesToShow: 6,
              slidesToScroll: 2,
              swipeToSlide: true,
              arrows: false,
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
              },
        methods: {
              scrollToAnchorPoint(refName) {
              const el = this.$refs[refName]
              el.scrollIntoView({ behavior: 'smooth'})
          }
      }
    
  }
  </script>
  
  <style scoped>
    .bg-hero {
      background-image: url("~/assets/image/hero-bg.png");
      background-size: cover;
      background-repeat: no-repeat;
      background-position: center;
      margin:auto;   
    }


    @media only screen and (max-width: 768px){
      
    }
    </style>
  
  
  