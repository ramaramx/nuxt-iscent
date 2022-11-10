<!-- This example requires Tailwind CSS v2.0+ -->
<template>

  <nav class="flex items-center justify-between flex-wrap bg-white shadow-sm p-2 lg:p-5 py-5">
    <div class="flex items-center flex-no-shrink text-black mr-6">
      <a
      href="https://iscent.ae/"
      >
      <img
      src="../assets/image/logo.png"
      alt="logo"
      class="w-[120px] h-[25px]"
      />
    </a>
    </div>
      <div>
        <a href="mailto:info@iscent.ae" class="no-underline inline-block text-sm px-4 py-2 leading-none border rounded text-black border-black hover:bg-black hover:text-white">
          Schedule Information Session</a>
      </div>
    
  </nav>

  </template>
  
  <script>
  export default {
    name : 'TheHeader'
  }
  
  </script>