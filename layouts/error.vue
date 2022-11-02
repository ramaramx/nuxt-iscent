<template>
    <div>
      <div
        id="sky"
        class="fixed z-50 top-0 h-screen w-screen flex justify-center items-center"
      >
        <div
          class="hidden flex-col items-center justify-center bg-white w-screen h-screen md:flex"
        >  
        <img 
          src="~/assets/gif/running.gif" 
          alt="astronout"
          class="animation"
          />        
        
         
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
    layout: 'noloading', // you can set a custom layout for the error page
  }
  </script>
  
  <style scoped>

  .animation{
    height: auto;
    width: 150px;
    
    position: absolute;

    top: 150px;
    
    
  }
  
  </style>