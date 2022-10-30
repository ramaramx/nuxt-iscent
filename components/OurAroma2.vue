<template>
    <div class="bg-black">
        <div class="flex flex-col lg:flex-row ">

            <div class="flex flex-col container p-5 py-10 gap-y-3 justify-center ">
                <h1 class="text-white text-4xl font-bold">{{title}}</h1>
                <p class="text-white text-base font-normal">Whether you want to create a haven in your home or discover the power of
                    scent marketing for your business, at iScent we use cutting-edge technology to bring the very best
                    scent-diffusion capabilities to your office, hotel, property, or business.

                    We work with brands, creating unique experiences for their customers, improving
                    consumer journeys, and building brand recognition. Our scent-marketing systems enhance environments,
                    allowing businesses to communicate their personality to customers in targeted and specific ways.

                    Whether you are looking to create a better environment for your business team,
                    impact customer experience or create a signature brand fragrance, we can help you.

                    We can target specific areas with a standalone scent diffuser machine, or create location-wide
                    experiences through ducted A/C diffusers types.

                    At iScent, we find flexible solutions for you, so you can create the best scent experience for your customers. </p>
                <a href="" class="underline text-white font-bold text-lg hover:no-underline "> Get in Touch Now!</a>
            </div>

            <VueSlickCarousel v-bind="settings" class="slick-slider">
            <img 
            src="https://images.unsplash.com/photo-1628950749921-ace26a06e307?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=580&q=80"
            alt="scent 1"
            
            class="w-[478px] h-[357px]"/>
            <img 
            src="https://images.unsplash.com/photo-1628950749921-ace26a06e307?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=580&q=80"
            alt="scent 1"
            class="w-[478px] h-[357px]" />
            <img 
            src="https://images.unsplash.com/photo-1628950749921-ace26a06e307?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=580&q=80"
            alt="scent 1"
            class="w-[478px] h-[357px]" />
            
            
            </VueSlickCarousel>
        </div>

    </div>
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel';

import 'vue-slick-carousel/dist/vue-slick-carousel.css'

export default{
    name : 'OurAroma2',
    components: {  VueSlickCarousel },
    data() {
        return {
            title : 'WE ARE EXPERTS IN CREATING SCENT EXPERIENCES',
            settings : {
                        dots: true,
                        infinite: true,
                        initialSlide: 1,
                        speed: 800,
                        slidesToShow: 1,
                        slidesToScroll: 1,
                        swipeToSlide: true,
                        draggable: true,
                        arrows: false,
                        responsive: [
                        {
                        "breakpoint": 1024,
                        "settings": {
                            "slidesToShow": 1,
                            "slidesToScroll": 1,
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
                    }
}
</script>

<style scoped>
.slick-slider{
    width: 450px;
    position: relative;
    display: block;
    box-sizing: border-box;
    -webkit-user-select: none;
    -moz-user-select: none;
    user-select: none;
    -webkit-touch-callout: none;
    -khtml-user-select: none;
    touch-action: pan-y;
    -webkit-tap-highlight-color: transparent;
}

</style>