<template>
<MainHeader></MainHeader>
<MainVisual></MainVisual>
<IconBanner :data = "icon"></IconBanner>
<ja-tab></ja-tab>
<ja-tab-swiper></ja-tab-swiper>
</template>

<script>
import "./assets/seting.css";
import MainHeader from './components/MainHeader.vue';
import MainVisual from './components/MainVisual.vue';
import IconBanner from './components/IconBanner.vue';
import JaTab from './components/JaTab.vue';
import JaTabSwiper from './components/JaTabSwiper.vue';

import Banner from './data/02iconBanner.js';
import edu from './data/03eduProgram';

export default {
  components: {
    MainHeader,
    MainVisual,
    IconBanner,
    JaTab,
    JaTabSwiper,
  },
  data() {
    return {
      icon : Banner,
      edu : edu,
    };
  },
}
</script>

<style lang="scss">
@import url(./assets/seting.css);
</style>
