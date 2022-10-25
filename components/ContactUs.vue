<template>
<section class="bg-hero-contact">
  <div class="py-8 px-5 lg:py-16 lg:pl-44 lg:px-0 mx-auto max-w-screen-md">
      <h2 class="mb-4 text-4xl tracking-tight font-extrabold lg:text-left text-center text-black">Contact Us</h2>
      <p class="mb-8 lg:mb-16 font-medium lg:text-left text-center text-gray-500 sm:text-xl">Got a technical issue? Want to send feedback about a beta feature? Need details about our Business plan? Let us know.</p>
      <form action="#" class="space-y-8">
        <div>
              <label for="name" class="block mb-2 text-sm font-medium text-gray-900 ">Name</label>
              <input type="text" id="subject" class="block p-3 w-full text-sm text-gray-900 bg-gray-50 rounded-lg border border-gray-300 shadow-sm focus:ring-primary-500 focus:border-primary-500 " placeholder="Name" required>
          </div>  
        <div>
              <label for="email" class="block mb-2 text-sm font-medium text-gray-900 ">Email</label>
              <input type="email" id="email" class="shadow-sm bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-primary-500 focus:border-primary-500 block w-full p-2.5" placeholder="example@email.com" required>
          </div>

          <div>
              <label for="telephone" class="block mb-2 text-sm font-medium text-gray-900 ">Phone Number</label>
              <input type="tel" id="telephone" class="shadow-sm bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-primary-500 focus:border-primary-500 block w-full p-2.5" placeholder="+971" required>
          </div>
          
          
          <button type="submit" class="flex justify-center py-3 px-5 text-sm font-medium lg:text-right text-center text-white rounded-lg bg-black sm:w-fit hover:bg-white hover:text-black focus:ring-4 focus:outline-none focus:ring-primary-300 ">Send message</button>
      </form>
  </div>
</section>
</template>

<style>
    .bg-hero-contact{
    background-image: url("https://images.unsplash.com/photo-1519332978332-21b7d621d05e?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=387&q=80");
    background-size: contain;
    background-repeat: no-repeat;
    margin:auto;
    }
</style>