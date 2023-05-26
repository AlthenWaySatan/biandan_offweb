<template>
    <swiper :effect="'cards'" :pagination="true" :initialSlide="2" :modules="modules" class="pageCardArea">
        <swiper-slide class="swiperCard">
            <img src="/pageImg/pageImg3-1.webp" alt="pageImg3-1" class="cardImg">
        </swiper-slide>
        <swiper-slide class="swiperCard">
            <img src="/pageImg/pageImg3-2.webp" alt="pageImg3-2" class="cardImg">
        </swiper-slide>
        <swiper-slide class="swiperCard">
            <img src="/pageImg/pageImg1.webp" alt="pageImg3-3" class="cardImg">
        </swiper-slide>
        <swiper-slide class="swiperCard">
            <img src="/pageImg/pageImg3-4.webp" alt="pageImg3-4" class="cardImg">
        </swiper-slide>
        <swiper-slide class="swiperCard">
            <img src="/pageImg/pageImg3-5.webp" alt="pageImg3-5" class="cardImg">
        </swiper-slide>
    </swiper>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';

import 'swiper/css/effect-cards';

// import required modules
import { EffectCards, Pagination } from 'swiper';

export default {
    components: {
        Swiper,
        SwiperSlide,
    },
    setup() {
        return {
            modules: [EffectCards, Pagination],
        };
    },
};
</script>
  