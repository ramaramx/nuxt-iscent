<template>
    <div>
        <h2 class="text-2xl font-bold text-center text-black mt-5 lg:mb-5 lg:text-6xl">Our Client</h2>
        
        <VueSlickCarousel v-bind="settings">
                        <div class="flex items-center justify-center px-4">
                            <div class="max-w-sm overflow-hidden rounded-xl bg-white shadow-md duration-200 hover:scale-105 hover:shadow-xl">
                                <img src="https://upload.wikimedia.org/wikipedia/commons/d/d0/Emirates_logo.svg" alt="plant" class="h-[250px] w-full" />
                                <div class="p-5">
                                    <h1 class="text-2xl mb-5 text-black font-bold">Emirates</h1>
                                <button v-on:click="toggleModal()" 
                                class="w-full rounded-md bg-black  py-2 text-white hover:bg-white hover:text-black hover:border-black hover:shadow-md duration-75">See More</button>
                                </div>
                            </div>
                        </div>

                        <div class="flex items-center justify-center px-4">
                            <div class="max-w-sm overflow-hidden rounded-xl bg-white shadow-md duration-200 hover:scale-105 hover:shadow-xl">
                                <img src="../assets/image/museum.png" alt="plant" class="h-[250px] w-full" />
                                <div class="p-5">
                                    <h1 class="text-2xl mb-5 text-black font-bold">Museum Of The Future</h1>
                                <button v-on:click="toggleModal()" 
                                class="w-full rounded-md bg-black  py-2 text-white hover:bg-white hover:text-black hover:border-black hover:shadow-md duration-75">See More</button>
                                </div>
                            </div>
                        </div>

                        <div class="flex items-center justify-center px-4">
                            <div class="max-w-sm overflow-hidden rounded-xl bg-white shadow-md duration-200 hover:scale-105 hover:shadow-xl">
                                <img src="https://upload.wikimedia.org/wikipedia/en/9/97/Dubai_Metro_Logo.png" alt="plant" class="h-[250px] w-full" />
                                <div class="p-5">
                                <h1 class="text-2xl mb-5 text-black font-bold">Metro</h1>
                                <button v-on:click="toggleModal()" 
                                class="w-full rounded-md bg-black  py-2 text-white hover:bg-white hover:text-black hover:border-black hover:shadow-md duration-75">See More</button>
                                </div>
                            </div>
                        </div>



                    
                </VueSlickCarousel>
                                
                                <!-- pop up 1 -->
                                <div v-if="showModal1" class="px-20 overflow-x-hidden overflow-y-auto fixed inset-0 z-50 outline-none focus:outline-none justify-center items-center flex">
                          
                                    <!--content-->
                                <div class="border-0 rounded-lg shadow-lg relative flex flex-col w-full bg-white outline-none focus:outline-none">
                                    <!--body-->
                                    <div class="gap-x-5 relative lg:p-6 flex flex-col lg:flex-row">
                                    <iframe class="w-full aspect-video " src="https://www.youtube.com/embed/TWACe_5KEBo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>></iframe>
                                    <div class="flex flex-col">
                                        <h1 class="text-4xl font-bold">METRO</h1>
                                        <h2 class="text-md font-regular text-gray-500">Description : <br/>
                                            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ullamcorper
                                            ullamcorper sagittis lacinia turpis eget pretium et tellus. Pulvinar aliquam quisque vel sit egestas consequat. Nec sed nunc tristique quis urna a dui fermentum. Diam nulla at porttitor duis justo, donec.
                                        </h2>
                                        <h2 class="text-md font-regular text-gray-500">Talk more for business</h2>
                                        <ContactForm />
                                    </div>
                                    </div>
                                    <!--footer-->
                                    <div class="flex items-center justify-end p-6 border-t border-solid border-slate-200 rounded-b">
                                        <button class="text-red-500 bg-transparent border border-solid border-red-500 hover:bg-red-500 hover:text-white active:bg-red-600 font-bold uppercase text-sm px-6 py-3 rounded outline-none focus:outline-none mr-1 mb-1 ease-linear transition-all duration-150" type="button" v-on:click="toggleModal()">
                                        Close
                                        </button>
                                    </div>
                                </div>
                            
                            </div>
                            <div v-if="showModal1" class="opacity-25 fixed inset-0 z-40 bg-black"></div>

                            <!-- pop up 2 -->
                            <div v-if="showModal2" class="px-20 overflow-x-hidden overflow-y-auto fixed inset-0 z-50 outline-none focus:outline-none justify-center items-center flex gap-x-5">
                                
                                    <!--content-->
                                <div class="border-0 rounded-lg shadow-lg relative flex flex-col w-full bg-white outline-none focus:outline-none">
                                    <!--body-->
                                    <div class="gap-x-5 relative lg:p-6 flex flex-col lg:flex-row">
                                        <iframe class="w-full aspect-video " src="https://www.youtube.com/embed/TWACe_5KEBo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                                    <div class="flex flex-col">
                                        <h1 class="text-4xl font-bold">METRO</h1>
                                        <h2 class="text-md font-regular text-gray-500">Description : <br/>
                                            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ullamcorper
                                            ullamcorper sagittis lacinia turpis eget pretium et tellus. Pulvinar aliquam quisque vel sit egestas consequat. Nec sed nunc tristique quis urna a dui fermentum. Diam nulla at porttitor duis justo, donec.
                                        </h2>
                                        <h2 class="text-md font-regular text-gray-500">Talk more for business</h2>
                                        <ContactForm/>
                                    </div>
                                    </div>
                                    <!--footer-->
                                    <div class="flex items-center justify-end p-6 border-t border-solid border-slate-200 rounded-b">
                                        <button class="text-red-500 bg-transparent border border-solid border-red-500 hover:bg-red-500 hover:text-white active:bg-red-600 font-bold uppercase text-sm px-6 py-3 rounded outline-none focus:outline-none mr-1 mb-1 ease-linear transition-all duration-150" type="button" v-on:click="toggleModal()">
                                        Close
                                        </button>
                                    </div>
                                </div>
                             
                            </div>
                            <div v-if="showModal2" class="opacity-25 fixed inset-0 z-40 bg-black"></div>

                            <!-- pop up 3 -->
                            <div v-if="showModal3" class="px-20 overflow-x-hidden overflow-y-auto fixed inset-0 z-50 outline-none focus:outline-none justify-center items-center flex">
                             
                                    <!--content-->
                                <div class="border-0 rounded-lg shadow-lg relative flex flex-col w-full bg-white outline-none focus:outline-none">
                                    <!--body-->
                                    <div class="gap-x-5 relative lg:p-6 flex flex-col lg:flex-row">
                                        <iframe class="w-full aspect-video" src="https://www.youtube.com/embed/TWACe_5KEBo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                                    <div class="flex flex-col">
                                        <h1 class="text-4xl font-bold">METRO</h1>
                                        <h2 class="text-sm lg:text-md font-regular text-gray-500">Description : <br/>
                                            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ullamcorper
                                            ullamcorper sagittis lacinia turpis eget pretium et tellus. Pulvinar aliquam quisque vel sit egestas consequat. Nec sed nunc tristique quis urna a dui fermentum. Diam nulla at porttitor duis justo, donec.
                                        </h2>
                                        <h2 class="text-md font-regular text-gray-500">Talk more for business</h2>
                                        <ContactForm />
                                    </div>
                                    </div>
                                    <!--footer-->
                                    <div class="flex items-center justify-end p-6 border-t border-solid border-slate-200 rounded-b">
                                        <button class="text-red-500 bg-transparent border border-solid border-red-500 hover:bg-red-500 hover:text-white active:bg-red-600 font-bold uppercase text-sm px-6 py-3 rounded outline-none focus:outline-none mr-1 mb-1 ease-linear transition-all duration-150" type="button" v-on:click="toggleModal()">
                                        Close
                                        </button>
                                    </div>
                                </div>
                            
                            </div>
                            <div v-if="showModal3" class="opacity-25 fixed inset-0 z-40 bg-black"></div>

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
            showModal3: false,
            settings : {
            dots: true,
            infinite: true,
            rows: 1,
            initialSlide: 2,
            speed: 500,
            slidesToShow: 3,
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
        toggleModal: function () {
            this.showModal1 = !this.showModal1;
        },
        toggleModal: function () {
            this.showModal2 = !this.showModal2;
        },
        toggleModal: function () {
            this.showModal3 = !this.showModal3;
        }
    },
}
    </script>

<style >
.slick-initialized .slick-slide[data-v-e4caeaf8] {
    display: block;
    padding: 50px;
}
</style>