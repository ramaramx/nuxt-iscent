<template>
    <div>
        <h2 class="text-xl font-bold text-center text-black mt-5 mb-5 lg:text-6xl">Our Aroma Design Process</h2>
        <div class="flex flex-col lg:flex-row justify-center gap-5 mt-5 mb-20 px-5">
          <div class="flex flex-col justify-center justify-self-center mx-auto">
            <img src="../assets/image/1.jpg"
            alt="delivery"
            class="rounded-md w-full h-full cursor-pointer opacity-1 transition-opacity hover:opacity-90 hover:bg-black" v-on:click="toggleModal()"/>
            <h2 class="text-md font-bold text-center" >Brand intake & ideation</h2>
            <p class="text-sm font-regular text-center text-gray">we learn about your brand, messaging, clientele, and identify unique challenges that may need to be addressed.</p>
             <div v-if="showModal" class="overflow-x-hidden overflow-y-auto fixed inset-0 z-50 outline-none focus:outline-none justify-center items-center flex">
                <div class="relative w-auto my-6 mx-auto max-w-6xl">
                    <!--content-->
                 <div class="border-0 rounded-lg shadow-lg relative flex flex-col w-full bg-white outline-none focus:outline-none">
                    <!--body-->
                    <div class="relative p-6 flex flex-row">
                    <iframe class="w-full aspect-video pr-5" src="https://www.youtube.com/watch?v=dQw4w9WgXcQ"></iframe>
                    <div class="flex flex-col">
                        <h1 class="text-4xl font-bold">METRO</h1>
                        <h2 class="text-md font-regular text-gray-500">Description : <br/>
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ullamcorper
                            ullamcorper sagittis lacinia turpis eget pretium et tellus. Pulvinar aliquam quisque vel sit egestas consequat. Nec sed nunc tristique quis urna a dui fermentum. Diam nulla at porttitor duis justo, donec.
                        </h2>
                        <h2 class="text-md font-regular text-gray-500">Talk more for business</h2>
                        <Form />
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

          <div class="flex flex-col justify-center justify-self-center mx-auto">
            <img src="../assets/image/2.jpg"
            alt="delivery"
            class="rounded-md w-full h-full cursor-pointer  opacity-1 transition-opacity hover:opacity-90 hover:bg-black" v-on:click="toggleModal()"/>
              <h2 class="text-md font-bold text-center">Planning and Formulation</h2>
              <p class="text-sm font-regular text-center text-gray">we learn about your brand, messaging, clientele, and identify unique challenges that may need to be addressed.</p>
              <div v-if="showModal" class="overflow-x-hidden overflow-y-auto fixed inset-0 z-50 outline-none focus:outline-none justify-center items-center flex">
                <div class="relative w-auto my-6 mx-auto max-w-6xl">
                    <!--content-->
                 <div class="border-0 rounded-lg shadow-lg relative flex flex-col w-full bg-white outline-none focus:outline-none">
                    <!--body-->
                    <div class="relative p-6 flex flex-row">
                    <iframe class="w-full aspect-video pr-5" src="https://www.youtube.com/watch?v=dQw4w9WgXcQ"></iframe>
                    <div class="flex flex-col">
                        <h1 class="text-4xl font-bold">METRO</h1>
                        <h2 class="text-md font-regular text-gray-500">Description : <br/>
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ullamcorper
                            ullamcorper sagittis lacinia turpis eget pretium et tellus. Pulvinar aliquam quisque vel sit egestas consequat. Nec sed nunc tristique quis urna a dui fermentum. Diam nulla at porttitor duis justo, donec.
                        </h2>
                        <h2 class="text-md font-regular text-gray-500">Talk more for business</h2>
                        <Form />
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

          <div class="flex flex-col justify-center justify-self-center mx-auto">
            <img src="../assets/image/3.jpg"
            alt="delivery"
            class="rounded-md w-full h-full opacity-1 cursor-pointer transition-opacity hover:opacity-90 hover:bg-black" v-on:click="toggleModal()"/>
              <h2 class="text-md font-bold text-center">Launch and Ongoing Support</h2>
              <p class="text-sm font-regular text-gray text-center">we learn about your brand, messaging, clientele, and identify unique challenges that may need to be addressed.</p>
              <div v-if="showModal" class="overflow-x-hidden overflow-y-auto fixed inset-0 z-50 outline-none focus:outline-none justify-center items-center flex">
                <div class="relative w-auto my-6 mx-auto max-w-6xl">
                    <!--content-->
                 <div class="border-0 rounded-lg shadow-lg relative flex flex-col w-full bg-white outline-none focus:outline-none">
                    <!--body-->
                    <div class="relative p-6 flex flex-row">
                    <iframe class="w-full aspect-video pr-5" src="https://www.youtube.com/watch?v=dQw4w9WgXcQ"></iframe>
                    <div class="flex flex-col">
                        <h1 class="text-4xl font-bold">METRO</h1>
                        <h2 class="text-md font-regular text-gray-500">Description : <br/>
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ullamcorper
                            ullamcorper sagittis lacinia turpis eget pretium et tellus. Pulvinar aliquam quisque vel sit egestas consequat. Nec sed nunc tristique quis urna a dui fermentum. Diam nulla at porttitor duis justo, donec.
                        </h2>
                        <h2 class="text-md font-regular text-gray-500">Talk more for business</h2>
                        <Form />
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
        </div>
      </div>
</template>

<script>
import Form from './form.vue';
    export default {
    name: "large-modal",
    data() {
        return {
            showModal: false
        };
    },
    methods: {
        toggleModal: function () {
            this.showModal = !this.showModal;
        }
    },
    components: { Form }
}
    </script>

<style>

</style>