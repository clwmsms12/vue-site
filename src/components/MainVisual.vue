<template>
  <swiper
    :slidesPerView="1"
    :spaceBetween="30"
    :loop="true"
    :pagination="{
      clickable: true,
    }"
    :navigation="true"
    :modules="modules"
    class="mySwiper"
  >
    <swiper-slide v-for="(item, i) in swiperView" :key="i">
      <div class="container">
        <div class="row">
          <div class="col-md-6 position-relative">
            <div class="sFontWrap">
              <h2 v-html="item.mainTitle"></h2>
              <p v-html="item.subtitle"></p>
            </div>
            <div class="vBtn">
              <p>자세히 보기</p>
              <i class="fa-solid fa-arrow-right-long"></i>
            </div>
          </div>
          <div class="col-md-6 videos">
            <video
              :src="`images/01mainSlide_video/${item.mVideo}`"
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
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";
import sData from "@/data/01mainSlide.js";
// Import Swiper styles
import "swiper/css";

import "swiper/css/pagination";
import "swiper/css/navigation";

// import required modules
import { Pagination, Navigation } from "swiper";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Pagination, Navigation],
      swiperView: sData,
    };
  },
};
</script>

<style lang="scss">
.mySwiper {
  background-color: #e1eff2;
  .swiper-slide {
    height: 700px;
    .sFontWrap{
      margin-top: 32%;z-index: 1111px;margin-bottom: 30px;
      h2{font-size: 50px;color: #285E76;margin-bottom: 20px;}
      p{font-size: 18px;color: #285E76;font-weight: bold;}
    }
    .vBtn{
      display: flex;margin-bottom: 0 !important;justify-content: space-around;align-items: center;
      background: #fff;width: 200px;height: 60px;border-radius: 30px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);cursor: pointer;
      p{
        margin-right: 10px;margin-bottom: 0 !important;
        font-weight: bold;
      }
      i{
        line-height: 1.5 !important;
      }
      }
    .videos {
      height: 700px;
      display: flex;justify-content: center;align-items: center;
      background-color: #e1eff2;
      video {
        height: 700px;
      }
    }
  }
  .swiper-button-prev{
    position: absolute;left: 16%;top: 90%;transform: scale(0.4);
  }
  .swiper-button-next{
    position: absolute;left: 20%;top: 90%;transform: scale(0.4);
  }
  .swiper-pagination-horizontal{
    position: absolute;left: -31.5%;bottom: 8%;
  }
}
</style>