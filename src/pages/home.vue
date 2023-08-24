<template>
    <swiper :direction="'vertical'" :slidesPerView="'auto'" :spaceBetween="0" :mousewheel="true"
        :pagination="{ clickable: true, dynamicBullets: true }" :modules="modules" class="mainSwiper"
        @transitionEnd="changeSlide">
        <!-- <swiper-slide class="page">
            <Page5 v-show="thisPage >= 0"></Page5>
        </swiper-slide> -->
        <swiper-slide class="page">
            <Page0 v-show="thisPage >= 0"></Page0>
        </swiper-slide>
        <swiper-slide class="page">
            <Page1 v-show="thisPage >= 1"></Page1>
        </swiper-slide>
        <swiper-slide class="page">
            <Page2 v-show="thisPage >= 2"></Page2>
        </swiper-slide>
        <swiper-slide class="page">
            <Page5 v-show="thisPage >= 3"></Page5>
        </swiper-slide>
        <swiper-slide class="page">
            <Page3 v-if="thisPage >= 4"></Page3>
        </swiper-slide>
        <swiper-slide class="page">
            <Page4 v-show="thisPage >= 5"></Page4>
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
import Page2 from "../views/page2.vue";
import Page3 from "../views/page3.vue";
import Page4 from "../views/page4.vue";
import Page5 from "../views/page5.vue";
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
        Page2,
        Page3,
        Page4,
        Page5,
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
  