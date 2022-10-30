<template>
    <div>
      <div
        id="sky"
        class="fixed z-50 top-0 h-screen w-screen flex justify-center items-center"
      >
        <div
          class="hidden flex-col items-center justify-center bg-white w-screen h-screen md:flex"
        >          
        <nuxt-link 
          to="/">
          <!-- DON T FORGET TO CHANGE THE IMG -->
            <img src="~/assets/image/logo.png" alt="iscent-logo" />
          </nuxt-link>
          <h1 class="font-mono text-black text-6xl py-10">
            {{ error.statusCode }} - Page Not Found
          </h1>
          <nuxt-link to="/">
            <button class="px-5 py-3 bg-black text-white rounded-lg hover:text-black hover:bg-white hover:border hover:border-black transition ease-in"> 
              Back to Home</button>
          </nuxt-link>

        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: ['error'],
    layout: 'error', // you can set a custom layout for the error page
  }
  </script>
  
  <style scopped>

  
  
  </style>