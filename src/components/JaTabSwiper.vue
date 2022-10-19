<template>
  <swiper :navigation="true" :modules="modules" class="mySwiper">
    <swiper-slide v-for="item in edu" :key="item" class="container">
        <h2 v-html="item.title"></h2>
        <p v-html="item.subtitle"></p>
        <img :src="`images/03eduProgram/${item.src}`" alt="">
    </swiper-slide>
    <swiper-slide>Slide 2</swiper-slide>
    <swiper-slide>Slide 3</swiper-slide>
    <swiper-slide>Slide 4</swiper-slide>
  </swiper>
</template>

<script>
import { Swiper, SwiperSlide } from "swiper/vue";

import "swiper/css";

import "swiper/css/navigation";

import { Navigation } from "swiper";

import edu from "@/data/03eduProgram.js"

export default {
    components: {
    Swiper,
    SwiperSlide,
    },
    props:[
        "edu",
    ],
    setup() {
      return {
        modules: [Navigation],
        edu:edu,
      };
    },
}
</script>

<style lang="scss">
    .mySwiper{
        .container{
            left: 50%;transform: translateX(-50%);
            h2{font-weight: bold;}
        }
    }
</style>