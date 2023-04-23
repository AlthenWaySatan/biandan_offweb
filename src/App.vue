<template>
  <swiper :direction="'vertical'" :slidesPerView="1" :spaceBetween="0" :mousewheel="true"
    :pagination="{ clickable: true, }" :modules="modules" class="mySwiper">
    <swiper-slide class="page">
    </swiper-slide>
    <swiper-slide class="footer">
    </swiper-slide>
  </swiper>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';

import './style.css';

// import required modules
import { Mousewheel, Pagination } from 'swiper';

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Mousewheel, Pagination],
    };
  },
};
</script>
