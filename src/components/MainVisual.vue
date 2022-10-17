<template>
    <swiper
    :navigation="true"
    :modules="modules"
    :loop="true"
    :pagination="{
      clickable: true,
    }"
    class="mySwiper"
    >
        <swiper-slide
        v-for="(item) in swiperView"
        :key="item"
        >
            <div class="videoWrap">
                <div class="row">
                    <div class="col-6 text">
                        <h2 v-html="item.mainTitle"></h2>
                    </div>
                    <div class="col-6">
                        <video
                            :src="`images/01mainSlide_video/${item.src}`"
                            autoplay
                            muted
                            loop
                            class=""
                        ></video>
                    </div>
                </div>
            </div>
        </swiper-slide>
    </swiper>
</template>

<script>
import { Swiper, SwiperSlide } from "swiper/vue";

import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";

import { Pagination } from "swiper";

import sData from "@/data/01mainSlide.js";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Navigation, Pagination],
      swiperView: sData,
    };
  },
};
</script>

<style lang="scss">
.mySwiper{
    swiper-slide{
        height: 400px;
        .videoWrap {
          overflow: hidden;
          background-color: #e1eff2;
          video {
            width: 100%;
          }
        }
    }
}
</style>