<template>
 <div>
   <div v-if="loading" class="loading-page background-white fadeout "> </div>
    
      <Nuxt />
    <TheFooter />
 </div>

 
</template>

<script>
export default {
   data () {
        return{
        loading: true,
        }
      },
      methods: {
        start() {
          this.loading = true
        },
        finish() {
          this.loading = false
        },
      },
   mounted() {
    this.$nextTick(() => {
      this.$nuxt.$loading.start()
      setTimeout(() => this.$nuxt.$loading.finish(), 1800)
    })
  }
}
</script>



<style scoped>
    .background-white{
    background-color: white;
    width: 100vw;
    height: 100vh;
    background-image: url('~/assets/image/logo.png');
    background-position: center;
    background-repeat: no-repeat;
    transition: ease-in;
    transform: scale(1.2);
    overflow: hidden;
  }
    .loading-page {
      position: fixed;
      top: 0;
      right: 0;
      z-index: 1000;
      padding: 1rem;
      text-align: center;
      font-size: 3rem;
      font-family: sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      overflow: hidden;
    }


    .loading {
      display: inline-block;
      width: 1.5rem;
      height: 1.5rem;
      border: 4px solid rgba(255, 255, 255, 0.705);
      border-radius: 50%;
      border-top-color: #ffffff;
      animation: spin 1s ease-in-out infinite;
    }
    @keyframes spin {
      to {
        -webkit-transform: rotate(360deg);
      }
    }

    .fadeout {
  animation: fadeout 4s forwards;
  overflow: hidden;
}

@keyframes fadeout {
  to {
    opacity: 0;
    visibility: hidden;
    overflow: hidden;
  }
}

  </style>