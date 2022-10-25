<template>
    <div>
        <h2 class="text-2xl font-bold text-center text-black mt-5 lg:mb-5 lg:text-4xl">Success Stories</h2>
        
        <VueSlickCarousel v-bind="settings">
                        <div class="flex justify-center px-1 pb-5 py-20 max-w-sm bg-white rounded-lg border border-gray-200 shadow-md">
                            <img src="../assets/image/emirates.png"
                            alt="delivery"
                            class="flex justify-center rounded-md w-full h-50 cursor-pointer opacity-1 transition-opacity hover:opacity-90 "/>
                            <h2 class="text-2xl font-bold text-left pt-10" >EMIRATES</h2>
                            <button type="button" class="text-black  hover:text-gray-600 focus:ring-4 focus:ring-blue-300 font-medium text-lg"  v-on:click="toggleModal()">
                            Read More</button>
                            


                        </div>

                        <div class="flex justify-center px-1 py-10 pb-20 max-w-sm bg-white rounded-lg border border-gray-200 shadow-md">
                            <img src="../assets/image/museum.png"
                            alt="delivery"
                            class="flex justify-center rounded-md w-full h-50 cursor-pointer opacity-1 transition-opacity hover:opacity-90 "/>
                            <h2 class="text-2xl font-bold text-left pt-10" >MOTF</h2>
                            <button type="button" class="text-black  hover:text-gray-600 focus:ring-4 focus:ring-blue-300 font-medium text-lg"  v-on:click="toggleModal()">
                            Read More</button>
                            
                        </div>

                        <div class="flex justify-center px-1 pb-5 max-w-sm bg-white rounded-lg border border-gray-200 shadow-md">
                            <img src="../assets/image/metro-logo.jpeg"
                            alt="delivery"
                            class="flex justify-center rounded-md w-full h-50 cursor-pointer opacity-1 transition-opacity hover:opacity-90"/>
                            <h2 class="text-2xl pt-5 font-bold text-left" >Metro</h2>
                            <button type="button" class="text-black  hover:text-gray-600 focus:ring-4 focus:ring-blue-300 font-medium text-lg"  v-on:click="toggleModal()">
                            Read More</button>
                            
                        </div>                       
                </VueSlickCarousel>
                <!-- pop up 1 -->
                <div v-if="showModal" class="overflow-x-hidden overflow-y-auto fixed inset-0 z-50 outline-none focus:outline-none justify-center items-center flex">
                                <div class="relative w-auto my-6 mx-auto max-w-lg lg:max-w-6xl">
                                    <!--content-->
                                <div class="border-0 rounded-lg shadow-lg relative flex flex-col w-full bg-white outline-none focus:outline-none">
                                    <!--body-->
                                    <div class="relative lg:p-6 flex flex-col lg:flex-row">
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
                            </div>
                            <div v-if="showModal" class="opacity-25 fixed inset-0 z-40 bg-black"></div>

                            <!-- pop up 2 -->
                            <div v-if="showModal" class="overflow-x-hidden overflow-y-auto fixed inset-0 z-50 outline-none focus:outline-none justify-center items-center flex">
                                <div class="relative w-auto my-6 mx-auto max-w-lg lg:max-w-6xl">
                                    <!--content-->
                                <div class="border-0 rounded-lg shadow-lg relative flex flex-col w-full bg-white outline-none focus:outline-none">
                                    <!--body-->
                                    <div class="relative lg:p-6 flex flex-col lg:flex-row">
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
                            </div>
                            <div v-if="showModal" class="opacity-25 fixed inset-0 z-40 bg-black"></div>

                            <!-- pop up 2 -->
                            <div v-if="showModal" class="overflow-x-hidden overflow-y-auto fixed inset-0 z-50 outline-none focus:outline-none justify-center items-center flex">
                                <div class="relative w-auto my-6 mx-auto max-w-lg lg:max-w-6xl">
                                    <!--content-->
                                <div class="border-0 rounded-lg shadow-lg relative flex flex-col w-full bg-white outline-none focus:outline-none">
                                    <!--body-->
                                    <div class="relative lg:p-6 flex flex-col lg:flex-row">
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
                            </div>
                            <div v-if="showModal" class="opacity-25 fixed inset-0 z-40 bg-black"></div>

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
            showModal: false,
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
            this.showModal = !this.showModal;
        }
    },
}
    </script>

<style>
.slick-initialized .slick-slide[data-v-e4caeaf8] {
    display: block;
    padding: 50px;
}
</style>