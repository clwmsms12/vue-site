<template>
  <div class="jaTabVisual">
    <div class="container d-flex">
      <h2>JA 교육 프로그램</h2>
      <div class="tabWrap">
        <div class="tabList" @click="tab = 1" :class="{ active: tab == 1 }">
          진로취업
        </div>
        <div class="tabList" @click="tab = 2" :class="{ active: tab == 2 }">
          경제금융
        </div>
        <div class="tabList" @click="tab = 3" :class="{ active: tab == 3 }">
          기업가정신
        </div>
        <div class="tabList" @click="tab = 4" :class="{ active: tab == 4 }">
          디지털 리터러시
        </div>
      </div>

      <visual-tap-swiper :edu="edu"></visual-tap-swiper>
    </div>
  </div>
</template>

<script>
import JaTabSwiper from "@/components/JaTabSwiper.vue";
export default {
  JaTabSwiper,
  props: ["edu"],
  data() {
    return {
      tab: 1,
    };
  },
};
</script>

<style lang="scss">
.jaTabVisual {
    padding: 100px 0;
    h2{font-weight: bold;}
  .tabWrap {
    display: flex;justify-content: space-around;
    text-align: center;
    width: 700px;
    height: 40px;
    position: relative;
    cursor: pointer;
    &.active:after {
      content: "";
      position: absolute;
      width: 100%;
      height: 3px;
      background: rgb(34, 111, 141);
      left: 0;
      bottom: 0;
    }
    .tabList{
        align-self: center;
    }
  }
}
</style>