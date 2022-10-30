<template>
  <div>
     <div class="px-4  py-20 h-full mx-auto lg:gap-8 xl:gap-0 lg:py-20 bg-hero" >
        <div class="mx-auto container gap-x-10">
            <h1 class="max-w-2xl mb-4 text-2xl font-medium tracking-tight leading-none md:text-5xl xl:text-6xl ">Bring the power of <b>aroma</b>
              to your retail experiences.</h1>
            <p class="max-w-2xl mb-6 font-light text-gray-500 text-sm lg:mb-8  lg:text-xl ">iScent helps brands design one-of-one olfactory experiences
That positively impact customer dwell time, foot traffic, return visits, and helps you craft a
memorable experience for all who interact with your brand</p>
            
          <button @click="scrollToAnchorPoint('contact')" class="inline-flex items-center justify-center px-5 py-3 text-base font-medium text-center text-white border bg-black border-black rounded-lg hover:bg-white hover:text-black focus:ring-4 focus:ring-white">
              SCHEDULE CONSULTATION
          </button> 
        </div>
      </div>
        <div class="container mx-auto py-20" >
          <h2 class="text-xl font-bold text-center text-black mt-5 mb-2 lg:text-6xl">The iScent Difference</h2>
          <p class="text-lg text-center lg:text-md">1. Custom-tailored auromas built from <b>ground-up.</b>
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
                <h2 class="text-md font-bold text-center">RETAIL</h2>
            </div>
         </div>

         <div class="flex flex-row">
          <div class="flex flex-col justify-center items-center  mx-auto lg:mx-10 transform transition duration-500 hover:scale-110">
            <img src="../assets/image/building.png"
            alt="delivery"
            class=" w-20 h-20 z-50  "/>
              <h2 class="text-md font-bold text-center">OFFICES</h2>
          </div>
        </div>
         
          <div class="flex flex-row">
            <div class="flex flex-col justify-center items-center  mx-auto lg:mx-10 transform transition duration-500 hover:scale-110">
            <img src="../assets/image/resort.png"
            alt="delivery"
            class=" w-20 h-20 z-50  "/>
              <h2 class="text-md font-bold text-center">HOTELS</h2>
          </div>
        </div>
         
          <div class="flex flex-row">
            <div class="flex flex-col justify-center items-center  mx-auto lg:mx-10 transform transition duration-500 hover:scale-110">
            <img src="../assets/image/healthcare.png"
            alt="delivery"
            class=" w-20 h-20 z-50  "/>
              <h2 class="text-md font-bold text-center">HEALTHCARE AND SPAS</h2>
          </div>
        </div>
         
          <div class="flex flex-row">
            <div class="flex flex-col justify-center items-center  mx-auto lg:mx-10 transform transition duration-500 hover:scale-110">
            <img src="../assets/image/property.png"
            alt="delivery"
            class=" w-20 h-20 z-50  "/>
              <h2 class="text-md font-bold text-center">PROPERTY MANAGEMENT</h2>
          </div>
        </div>
         
          <div class="flex flex-row">
            <div class="flex flex-col justify-center items-center  mx-auto lg:mx-10 transform transition duration-500 hover:scale-110">
            <img src="../assets/image/showroom.png"
            alt="delivery"
            class=" w-20 h-20 z-50  "/>
              <h2 class="text-md font-bold text-center">CAR SHOWROOMS</h2>
          </div>
        </div>
      </VueSlickCaraousel>

      <OurAroma/>
      
      <SuccesStories />
      <div ref="contact">
      <ContactUs />
    </div>
    </div>
</template>

<script>
import OurAroma from '../components/OurAroma.vue';
import SuccesStories from '../components/SuccesStories.vue';
import ContactUs from '../components/ContactUs.vue';
import VueSlickCaraousel from 'vue-slick-carousel'

export default {
    name: "index",
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
            speed: 800,
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
    background-image: url("~/assets/image/hero.png");
    background-size: cover;
    background-repeat: round;
    margin:auto;
  }

  @media only screen and (max-width: 768px){
      .bg-hero {
    background-image: url("~/assets/image/hero.png");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
  }
  }
  </style>


