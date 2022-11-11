<template>
<form @submit.prevent="sendEmail">
    <v-text-field
      v-model="name"
      type="text"
        name="name"
      :error-messages="nameErrors"
      :counter="10"
      label="Name"
      required
      @input="$v.name.$touch()"
      @blur="$v.name.$touch()"
    ></v-text-field>
    <v-text-field
      v-model="email"
      type="tel"
        name="phone"
      :error-messages="emailErrors"
      label="E-mail"
      required
      @input="$v.email.$touch()"
      @blur="$v.email.$touch()"
    ></v-text-field>
    
    <v-btn @click="clear">
      clear
    </v-btn>
    
    <v-btn
      class="mr-4"
      :disabled="!valid"
      @click="validate"
    >
      submit
    </v-btn>
    
  </form>
</template>

<script>
  import { validationMixin } from 'vuelidate'
  import { required, email } from 'vuelidate/lib/validators'

  export default {
    mixins: [validationMixin],

    validations: {
      name: { required},
      email: { required, email },
    },

    data: () => ({
      name: '',
      email: '',
      valid: true,
      
      
    }),

    computed: {
      nameErrors () {
        const errors = []
        if (!this.$v.name.$dirty) return errors
        !this.$v.name.required && errors.push('Name is required.')
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
      validate () {
      this.valid = this.$refs.form.validate()
      if (this.valid) {
        this.snackbar = true
      }
      else 
        alert ("Thanks for Contact Us")
    },
      submit () {
        this.$v.$touch()
      },
      clear () {
        this.$v.$reset()
        this.name = ''
        this.email = ''
      },
      sendEmail(e) {
      try {
        emailjs.sendForm('service_kfrm04n', 'template_t0ll7in', e.target, 'Tplr0-2NVfteRuO70' ,
         {
          name: this.name,
          email: this.email,
          
        })
        } catch(error) {
            console.log({error})
        }
      }
  },
}
</script>