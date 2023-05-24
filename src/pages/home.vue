<template>
    <swiper :direction="'vertical'" :slidesPerView="'auto'" :spaceBetween="0" :mousewheel="true"
        :pagination="{ clickable: true, dynamicBullets: true }" :modules="modules" class="mySwiper"
        @transitionEnd="changeSlide">
        <swiper-slide class="page">
            <Page0 ref="page0" v-if="thisPage >= 0"></Page0>
        </swiper-slide>
        <swiper-slide class="page">
            <Page1 ref="page1" v-if="thisPage >= 1"></Page1>
        </swiper-slide>
        <swiper-slide class="footer">
            <Footer></Footer>
        </swiper-slide>
    </swiper>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
import '../style.css';

import Page0 from "../views/page0.vue";
import Page1 from "../views/page1.vue";
import Footer from "../views/footer.vue";

// import required modules
import { Mousewheel, Pagination } from 'swiper';

export default {
    data() {
        return {
            thisPage: 0
        }
    },
    components: {
        Swiper,
        SwiperSlide,
        Page0,
        Page1,
        Footer,
    },
    methods: {
        changeSlide(swiper) {
            if (this.thisPage < swiper.activeIndex)
                this.thisPage = swiper.activeIndex;
            console.log('thisPage: ' + this.thisPage);
        }
    },
    setup() {
        return {
            modules: [Mousewheel, Pagination],
        };
    },
};
</script>
  