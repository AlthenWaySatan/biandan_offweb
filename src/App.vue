<template>
  <swiper :direction="'vertical'" :slidesPerView="1" :spaceBetween="0" :mousewheel="true"
    :pagination="{ clickable: true, }" :modules="modules" class="mySwiper">
    <swiper-slide style="background-color: #f1f2f3;">Slide 1</swiper-slide>
    <swiper-slide style="background-color: #f8b600;">Slide 2</swiper-slide>
    <swiper-slide style="background-color: #f1f2f3;">Slide 3</swiper-slide>
    <swiper-slide style="background-color: #f8b600;">Slide 4</swiper-slide>
    <swiper-slide style="background-color: #f1f2f3;">Slide 5</swiper-slide>
    <swiper-slide style="background-color: #f8b600;">Slide 6</swiper-slide>
  </swiper>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
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
