<template>
    <div class="index">
        <div class="container">
            <div class="swiper-box">
                <swiper :options="swiperOption">
                    <swiper-slide v-for="item in slideList" :key="item.id">
                        <a :href="'/#/product'+item.id">
                        <img :src="item.img"></a>
                    </swiper-slide>
                    <div class="swiper-pagination" slot="pagination"></div>
                    <div class="swiper-button-prev swiper-button-white" slot="button-prev"></div>
                    <div class="swiper-button-next swiper-button-white" slot="button-next"></div>
                    <div class="swiper-scrollbar" slot="scrollbar"></div>
                </swiper>
            </div>
            <div class="caidan">

            </div>
            <div class="ads-box"></div>
            <div class="banner"></div>
            <div class="product-box"></div>
        </div>
    </div>
</template>
<script>
import { Swiper,SwiperSlide } from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'
export default {
    name:'index',
    components:{
        Swiper,
        SwiperSlide,
    },
    data(){
        return{
            swiperOption:{
                autoplay:true,
                loop:true,
                effect : 'fade',
                fadeEffect: {
                    crossFade: true,
                },
                // effect : 'cube',
                // cubeEffect: {
                //     slideShadows: true,
                //     shadow: true,
                //     shadowOffset: 100,
                //     shadowScale: 0.6
                // },
                // effect : 'coverflow',
                // slidesPerView: 3,
                // centeredSlides: true,
                // coverflowEffect: {
                //     rotate: 30,
                //     stretch: 10,
                //     depth: 60,
                //     modifier: 2,
                //     slideShadows : true
                // },
                // effect : 'flip',
                // flipEffect: {
                //     slideShadows : true,
                //     limitRotation : true,
                // },
                pagination: {
                    el: '.swiper-pagination',
                    clickable:true,
                },
                navigation: {
                    nextEl: '.swiper-button-next',
                    prevEl: '.swiper-button-prev',
                },
            },
            
            slideList:[
                {
                    id:'1',
                    img:'lunbo1.jpg',
                }, {
                    id:'2',
                    img:'lunbo2.jpg',
                }, {
                    id:'3',
                    img:'lunbo3.jpg',
                }, {
                    id:'4',
                    img:'lunbo4.jpg',
                },
            ]
        }
    },

}
</script>

<style>
    .swiper-button-prev{
        margin-left: 22%;
    }
    .swiper-button-next{
        margin-right: 15%;
    }
    .container{
        --swiper-theme-color: white;
        position: relative;
        top:58px;
    }
    img{
        width: 90%;
        border-radius: 15px;
    }
    .caidan{
        position: relative;
        margin-left: 5%;
        top:-392px;
        border-radius: 15px;
        width: 16%;
        height:385px;
        z-index: 19;
        background: rgba(0, 0, 0, 0.2);
    }

</style>