<template>
    <div>
        <h2 class="text-2xl font-bold text-center text-black mt-5 lg:mb-5 lg:text-6xl">Our Aroma Design Process</h2>
        <VueSlickCarousel v-bind="settings">
        <!-- <div class="flex flex-col lg:flex-row justify-center gap-5 mt-5 mb-20 px-5"> -->
          <div class="flex flex-col justify-center justify-self-center mx-auto">
            <img src="../assets/image/1.jpg"
            alt="delivery"
            class="rounded-md w-full h-full z-50 opacity-1 transition-opacity hover:opacity-90 hover:bg-black"/>
              <h2 class="text-md font-bold text-center">Brand intake & ideation</h2>
              <p class="text-sm font-regular text-center text-gray">We learn about your brand, messaging, 
clientele, and identify unique challenges that
may need to be addressed.</p>
          </div>
          <div class="flex flex-col justify-center justify-self-center mx-auto">
            <img src="../assets/image/2.jpg"
            alt="delivery"
            class="rounded-md w-full h-full z-50 opacity-1 transition-opacity hover:opacity-90 hover:bg-black"/>
              <h2 class="text-md font-bold text-center">Planning and Formulation</h2>
              <p class="text-sm font-regular text-center text-gray">Our experienced team of scent specialists and chemists create a tailored scent to drive your business outcomes. </p>
          </div>
          <div class="flex flex-col justify-center justify-self-center mx-auto">
            <img src="../assets/image/3.jpg"
            alt="delivery"
            class="rounded-md w-full h-full z-50 opacity-1 transition-opacity hover:opacity-90 hover:bg-black"/>
              <h2 class="text-md font-bold text-center">Launch and Ongoing Support</h2>
              <p class="text-sm font-regular text-gray text-center">Our team delivers quality personal service throughout onboarding, management, and optimization of your unqiue scent.</p>
          </div>
        <!-- </div> -->
      </VueSlickCarousel>
      </div>
</template>

<script>
  import ContactForm from './ContactForm.vue';
  import VueSlickCarousel from 'vue-slick-carousel';
  
  import 'vue-slick-carousel/dist/vue-slick-carousel.css'
    // optional style for arrows & dots
  import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
  
      export default {
      name: "SuccessStories",
      components: { ContactForm, VueSlickCarousel },
      data() {
          return {
             settings : {
              dots: true,
              infinite: true,
              rows: 1,
              initialSlide: 2,
              speed: 500,
              slidesToShow: 3,
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
                  "slidesToShow": 2,
                  "slidesToScroll": 2,
                  "initialSlide": 2
              }
              },
              {
              "breakpoint": 480,
              "settings": {
                  "dots" : false,
                  "slidesToShow": 1,
                  "slidesToScroll": 1
              }
              }
          ]
          },      
  }
}
      }
      </script>
  
  <style>

  </style>