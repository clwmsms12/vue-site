<template>
  <swiper :navigation="true" :modules="modules" class="mySwiper1">
    <swiper-slide v-for="item in edu" :key="item" class="container">
        <div class="row">
          <div class="col-md-6">
            <h2 v-html="item.title"></h2>
            <p v-html="item.subtitle"></p>
            <div class="btn2">
              <p>자세히 보기</p>
              <i class="fa-solid fa-arrow-right-long"></i>
            </div>
          </div>
          <div class="col-md-6">
            <img :src="`images/03eduProgram/${item.src}`" alt="">
          </div>
        </div>
    </swiper-slide>
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
    .mySwiper1{
      background: skyblue;padding: 50px 0;
      .swiper-wrapper{}
        .container{
            left: 50%;transform: translateX(-50%);
            h2{font-weight: bold;margin-bottom: 20px;}
            img{height: 362px;}
            p{margin-bottom: 80px;font-size: 18px;}
            .btn2{
              display: flex;margin-bottom: 0 !important;justify-content: space-around;align-items: center;
              background: #fff;width: 200px;height: 60px;border-radius: 30px;
              box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);cursor: pointer;
              p{
                margin-right: 10px;margin-bottom: 0 !important;
                font-weight: bold;
              }
            }
        }
    }
</style>