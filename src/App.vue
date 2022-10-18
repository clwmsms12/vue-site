<template>
<MainHeader></MainHeader>
<MainVisual></MainVisual>
<IconBanner :data = "icon"></IconBanner>
</template>

<script>
import "./assets/seting.css";
import MainHeader from './components/MainHeader.vue';
import MainVisual from './components/MainVisual.vue';
import IconBanner from './components/IconBanner.vue';

import Banner from './data/02iconBanner.js';

export default {
  components: {
    MainHeader,
    MainVisual,
    IconBanner,
  },
  data() {
    return {
      icon : Banner,
    };
  },
}
</script>

<style lang="scss">
@import url(./assets/seting.css);
</style>
