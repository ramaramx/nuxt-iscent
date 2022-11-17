<template>
    <div>
        <h2 class="text-2xl font-bold text-center text-black mt-5 lg:mb-5 lg:text-4xl">Success Stories</h2>
        
        <VueSlickCarousel v-bind="settings">
                        <div class="flex items-center justify-center px-4">
                                    <div class="w-full max-w-sm overflow-hidden rounded-xl bg-white shadow-md duration-200 hover:scale-105 hover:shadow-xl py-10">
                                        
                                        <div class="flex justify-center">
                                            <img src="~/assets/image/paramount-logo.jpeg" alt="plant" class="h-[150px] w-[150px]" />
                                        </div>
        
                                        <div class="p-5">
                                        <h1 class="text-2xl mb-5 text-black font-bold">Paramount</h1>
                                        <button @click="toggleModal1()" 
                                        class="w-full rounded-md bg-black  py-2 text-white hover:bg-white hover:text-black hover:border-black hover:shadow-md duration-75">See More</button>
                                        </div>
                                    </div>
                                </div>

                                
                                
                                <div class="flex items-center justify-center px-4">
                                            <div class="w-full max-w-sm overflow-hidden rounded-xl bg-white shadow-md duration-200 hover:scale-105 hover:shadow-xl py-10">
                                                
                                                <div class="flex justify-center">
                                                    <img src="~/assets/image/rixos.png" alt="plant" class="h-[150px] w-[250px]" />
                                                </div>
                
                                                <div class="p-5">
                                                <h1 class="text-2xl mb-5 text-black font-bold">Rixos</h1>
                                                <button @click="toggleModal2()" 
                                                class="w-full rounded-md bg-black  py-2 text-white hover:bg-white hover:text-black hover:border-black hover:shadow-md duration-75">See More</button>
                                                </div>
                                            </div>
                                        </div>
                                    

                                <div class="flex items-center justify-center px-4 container">
                                    <div class="w-full max-w-sm overflow-hidden rounded-xl bg-white shadow-md duration-200 hover:scale-105 hover:shadow-xl py-10">
                                        <div class="flex justify-center">
                                        <img src="https://upload.wikimedia.org/wikipedia/commons/d/d0/Emirates_logo.svg" alt="plant" class="h-[150px] w-[200px]" />
                                        </div>
                                        <div class="p-5">
                                            <h1 class="text-2xl mb-5 text-black font-bold">Emirates</h1>
                                        <!-- <button v-on:click="toggleModal()" 
                                        class="w-full rounded-md bg-black  py-2 text-white hover:bg-white hover:text-black hover:border-black hover:shadow-md duration-75">See More</button> -->
                                        </div>
                                    </div>
                                </div>
        
                                <div class="flex items-center justify-center px-4">
                                    <div class="w-full max-w-sm overflow-hidden rounded-xl bg-white shadow-md duration-200 hover:scale-105 hover:shadow-xl py-10">
        
                                        <div class="flex justify-center">
                                            <img src="../assets/image/museum.png" alt="plant" class="h-[150px] w-[200px]" />
                                        </div>
        
                                        <div class="p-5">
                                            <h1 class="text-2xl mb-5 text-black font-bold">Museum Of The Future</h1>
                                        <!-- <button v-on:click="toggleModal()" 
                                        class="w-full rounded-md bg-black  py-2 text-white hover:bg-white hover:text-black hover:border-black hover:shadow-md duration-75">See More</button> -->
                                        </div>
                                    </div>
                                </div>
        
                                <div class="flex items-center justify-center px-4">
                                    <div class="w-full max-w-sm overflow-hidden rounded-xl bg-white shadow-md duration-200 hover:scale-105 hover:shadow-xl py-10">
                                        
                                        <div class="flex justify-center">
                                            <img src="https://upload.wikimedia.org/wikipedia/en/9/97/Dubai_Metro_Logo.png" alt="plant" class="h-[150px] w-[150px]" />
                                        </div>
        
                                        <div class="p-5">
                                        <h1 class="text-2xl mb-5 text-black font-bold">Metro</h1>
                                        <!-- <button v-on:click="toggleModal()" 
                                        class="w-full rounded-md bg-black  py-2 text-white hover:bg-white hover:text-black hover:border-black hover:shadow-md duration-75">See More</button> -->
                                        </div>
                                    </div>
                                </div>
                                
                                
                        </VueSlickCarousel>
                
<!-- pop up 1 -->
<div v-if="showModal1" class="px-1 lg:px-20 overflow-x-hidden overflow-y-auto fixed inset-0 z-50 outline-none focus:outline-none justify-center items-center flex">
                          
                          <!--content-->
                      <div class="border-0 rounded-lg shadow-lg relative flex flex-col w-full bg-white outline-none focus:outline-none">
                          <!--body-->
                          <div class="gap-x-5 relative lg:p-6 flex flex-col lg:flex-row">
                          <iframe class="w-full aspect-video " src="https://www.youtube.com/embed/XPyP49A6TBk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>></iframe>
                          <div class="flex flex-col">
                              <h1 class="text-4xl font-bold">PARAMOUNT</h1>
                              <p class="text-md font-regular text-gray-500">Description : <br/>
Paramount Hotel Dubai had a vision to create three distinct atmospheres within their landmark hotel, each meant to illicit a different feeling. All three scents were designed as signature scents both individually, and also synergistically, flowing from one room to another organically. 
“What’s wonderful about iScent is that its not a perfume. You don’t walk into the hotel and get showered with perfume when you walk through the room. Rather, you walk into a feeling. You walk into a scene. Onto a stage. You are enveloped by this paramount feel and character”
                              </p>
                              
                              <ContactForm />
                          </div>
                          </div>
                          <!--footer-->
                          <div class="flex items-center justify-end p-6 border-t border-solid border-slate-200 rounded-b">
                              <button class="text-red-500 bg-transparent border border-solid border-red-500 hover:bg-red-500 hover:text-white active:bg-red-600 font-bold uppercase text-sm px-6 py-3 rounded outline-none focus:outline-none mr-1 mb-1 ease-linear transition-all duration-150" type="button" 
                              v-on:click="toggleModal1()">
                              Close
                              </button>
                          </div>
                      </div>
                  
                  </div>
                  
                  
                  <!-- pop up 2 -->
                  <div v-if="showModal2" class="px-0 lg:px-20 overflow-x-hidden overflow-y-auto fixed inset-0 z-50 outline-none focus:outline-none justify-center items-center flex gap-x-5">
                      
                      <!--content-->
                  <div class="border-0 rounded-lg shadow-lg relative flex flex-col w-full bg-white outline-none focus:outline-none">
                      <!--body-->
                      <div class="gap-x-5 relative lg:p-6 flex flex-col lg:flex-row">
                          <iframe class="w-full aspect-video " src="https://www.youtube.com/embed/BTi41C-hrXM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                      <div class="flex flex-col">
                          <h1 class="text-4xl font-bold">RIXOS</h1>
                          <p class="text-md font-regular text-gray-500">Description : <br/>
                            The mission of Rixios Premium Hotel Dubai was simple: to provide an immediate sense of freshness as soon as a new patron walks through the front doors. Working with iScent, Rixios deployed their signature scent through HVAC diffusers throughout the hotel lobby. Both guests and hotel staff immediately noticed a more fresh, open, and breathable environment in the hotel.
                            “The first impression is key and with iScent it allowed us to put the freshest and cleanest foot forward”
                          </p>
                          
                          <ContactForm/>
                      </div>
                      </div>
                      <!--footer-->
                      <div class="flex items-center justify-end p-6 border-t border-solid border-slate-200 rounded-b">
                          <button  class="text-red-500 bg-transparent border border-solid border-red-500 hover:bg-red-500 hover:text-white active:bg-red-600 font-bold uppercase text-sm px-6 py-3 rounded outline-none focus:outline-none mr-1 mb-1 ease-linear transition-all duration-150" 
                          type="button" v-on:click="toggleModal2()">
                          Close
                          </button>
                      </div>
                  </div>
               
              </div>
              

                  

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
            
            showModal1: false,
            showModal2: false,
            
           settings : {
            dots: true,
            infinite: true,
            rows: 1,
            initialSlide: 0,
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
        }
                };
            },
    methods: {
        toggleModal1: function () {
            this.showModal1 = !this.showModal1;
        },
        
        toggleModal2: function () {
            this.showModal2 = !this.showModal2;
        }
    //   toggleModal1() {
    //     this.showModal1 = true;
    //   },
    //   toggleModal2(){
    //     this.showModal2 = true;
    //   },
    //   closeModal1() {
    //     this.showmodal1 = false;
    //   },
    //   closeModal2() {
    //     this.showmodal2 = false;
    //   }
    
    },
}
    </script>

<style>
.slick-initialized .slick-slide[data-v-e4caeaf8] {
    display: block;
    padding: 50px;
}
</style>