<template>
    <div class="bg-black">
        <div class="flex flex-col lg:flex-row ">

            <div class="flex flex-col container p-5 lg:p-20 py-10 gap-y-3 justify-center ">
                <h1 class="text-white text-4xl font-bold text-center lg:text-left">{{title}}</h1>
                <p class="text-white text-base font-normal text-center lg:text-left">{{desc}} </p>
                <a href="" class="underline text-white font-bold text-lg hover:no-underline text-center lg:text-left "> Get in Touch Now!</a>
            </div>

            <VueSlickCarousel v-bind="settings" class="slick-slider">
            <img 
            src="http://iscent.ae/landing-page/images/lp/small-sldier02.jpg"
            alt="scent 1"
            
            class="w-[478px] h-[357px]"/>
            <img 
            src="http://iscent.ae/landing-page/images/lp/small-sldier05.jpg"
            alt="scent 1"
            class="w-[478px] h-[357px]" />
            <img 
            src="http://iscent.ae/landing-page/images/lp/small-sldier07.jpg"
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
            desc :"Whether you want to create a haven in your home or discover the power of scent marketing for your business, at iScent we use cutting-edge technology to bring the very best\r\n                    scent-diffusion capabilities to your office, hotel, property, or business.\r\n\r\n                    We work with brands, creating unique experiences for their customers, improving\r\n                    consumer journeys, and building brand recognition. Our scent-marketing systems enhance environments,\r\n                    allowing businesses to communicate their personality to customers in targeted and specific ways.\r\n\r\n                    Whether you are looking to create a better environment for your business team,\r\n                    impact customer experience or create a signature brand fragrance, we can help you.\r\n\r\n                    We can target specific areas with a standalone scent diffuser machine, or create location-wide\r\n                    experiences through ducted A/C diffusers types.\r\n\r\n                    At iScent, we find flexible solutions for you, so you can create the best scent experience for your customers.",
            settings : {
                        dots: true,
                        infinite: true,
                        autoplay: true,
                        autoplaySpeed : 3000,
                        cssEase: 'ease',
                        dotsClass: 'slick-dots',
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
.slick-dots {
  background-color: transparent; /* bg color of container */
}


@media only screen and (max-width: 768px){
    .slick-slider{
    width: 100%;
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
}

</style>