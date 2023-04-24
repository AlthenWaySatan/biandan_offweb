<template>
  <swiper :direction="'vertical'" :slidesPerView="'auto'" :spaceBetween="0" :mousewheel="true"
    :pagination="{ clickable: true, dynamicBullets: true }" :modules="modules" class="mySwiper"
    @transitionEnd="changeSlide">
    <swiper-slide class="page">
      <Page0></Page0>
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
import './style.css';

import Page0 from "./views/page0.vue";
import Footer from "./views/footer.vue";


// import required modules
import { Mousewheel, Pagination } from 'swiper';

export default {
  components: {
    Swiper,
    SwiperSlide,
    Page0,
    Footer,
  },
  methods: {
    changeSlide(swiper) {
      console.log('Index: ' + swiper.activeIndex);
    }
  },
  setup() {
    return {
      modules: [Mousewheel, Pagination],
    };
  },
};
</script>
