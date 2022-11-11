<template>
<section class="bg-hero-contact">
  <div class="py-8 px-5 lg:py-16 lg:pl-44 lg:px-0 mx-auto max-w-screen-md">
      <h2 class="mb-4 text-4xl tracking-tight font-extrabold lg:text-left text-center text-black">Contact A Scent Expert </h2>
      <p class="mb-8 lg:mb-16 font-medium lg:text-left text-center text-gray-500 sm:text-xl">Interested in bringing the power of scent to your home or business? Get in touch with a scent expert to learn more about iScent’s offerings.</p>
      
      <form class="space-y-8" @submit.prevent="sendEmail">

        <v-text-field
        v-model="name"
        type="text"
        name="name"
        :error-messages="nameErrors"
        label="Name"
        outlined
        required
        @input="$v.name.$touch()"
        @blur="$v.name.$touch()"
        ></v-text-field>

        <v-text-field
        v-model="tel"
        type="tel"
        name="phone"
        :error-messages="phoneErrors"
        :counter="12"
        label="Phone Number"
        outlined
        required
        @input="$v.name.$touch()"
        @blur="$v.name.$touch()"
        ></v-text-field>
        
        <v-text-field
        v-model="email"
        type="text"
        name="email"
        :error-messages="emailErrors"
        label="E-mail"
        outlined
        required
        @input="$v.email.$touch()"
        @blur="$v.email.$touch()"
        ></v-text-field>

        <v-btn @click="clear">
        clear
      </v-btn>

        <v-btn
      type="submit"
      value="send"
      class="mr-4"
      @click="submit"
      
      >
        submit
      </v-btn>
      

      </form>
      
      <!-- <form class="space-y-8" @submit.prevent="sendEmail">
        <div>
              <label for="name" class="block mb-2 text-sm font-medium text-gray-900 ">Name</label>
              <input type="text" name="name"  class="block p-3 w-full text-sm text-gray-900 bg-gray-50 rounded-lg border border-gray-300 shadow-sm focus:ring-primary-500 focus:border-primary-500 " placeholder="Name"  required>
          </div>  
        <div>
              <label for="email" class="block mb-2 text-sm font-medium text-gray-900 ">Email</label>
              <input type="email" name="email"  class="shadow-sm bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-primary-500 focus:border-primary-500 block w-full p-2.5" placeholder="example@email.com" required>
          </div>

          <div>
              <label for="phone" class="block mb-2 text-sm font-medium text-gray-900 ">Phone Number</label>
              <input type="tel" name="phone" class="shadow-sm bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-primary-500 focus:border-primary-500 block w-full p-2.5" placeholder="+971" required>
          </div>
          
          
          <button type="submit" value="send" class="flex justify-center py-3 px-5 text-sm font-medium lg:text-right text-center text-white rounded-lg bg-black sm:w-fit hover:bg-white hover:text-black focus:ring-4 focus:outline-none focus:ring-primary-300 ">Send message</button>
      </form> -->
  </div>
</section>
</template>

<script>
import emailjs from 'emailjs-com'

import { validationMixin } from 'vuelidate'
import { required, email } from 'vuelidate/lib/validators'

export default {
  name: 'ContactUs',
  mixins: [validationMixin],

    validations: {
      name: { required},
      email: { required, email },
      tel: {required}
    },

  data() {
    return {
      name: '',
      email: '',
      tel: ''
      
    }
  },

  computed: {
    
      nameErrors () {
        const errors = []
        if (!this.$v.name.$dirty) return errors
        !this.$v.name.required && errors.push('Name is required.')
        return errors
      },
      phoneErrors () {
        const errors = []
        if (!this.$v.name.$dirty) return errors
        !this.$v.name.maxLength && errors.push('Phone Number must be at most 12 characters long')
        !this.$v.name.required && errors.push('Phone Number is required.')
        return errors
      },
      emailErrors () {
        const errors = []
        if (!this.$v.email.$dirty) return errors
        !this.$v.email.email && errors.push('Must be valid e-mail')
        !this.$v.email.required && errors.push('E-mail is required')
        return errors
      },
    },

  methods: {

    submit () {
        this.$v.$touch()
      },
      clear () {
        this.$v.$reset()
        this.name = ''
        this.email = ''
        this.tel = ''
        
      },
    sendEmail(e) {
      try {
        emailjs.sendForm('service_kfrm04n', 'template_k14kdea', e.target, 'Tplr0-2NVfteRuO70' ,
         {
          name: this.name,
          email: this.email,
          tel: this.tel
        })
        alert('thanks for submit your data')
      } catch(error) {
          console.log({error})
      }
     
    },
  }
}
</script>

<style scoped>
    .bg-hero-contact{
    background-image: url("https://images.unsplash.com/photo-1519332978332-21b7d621d05e?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=387&q=80");
    background-size: contain;
    background-repeat: no-repeat;
    margin:auto;
    }

    

    @media only screen and (max-width: 768px){
                .bg-hero-contact{
            background-image: url("https://images.unsplash.com/photo-1519332978332-21b7d621d05e?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=387&q=80");
            background-size: cover;
            background-repeat: no-repeat;
            margin:auto;
            }
    }
</style>