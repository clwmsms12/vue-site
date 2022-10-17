<template>
<MainHeader></MainHeader>
<MainVisual></MainVisual>
</template>

<script>
import "./assets/seting.css";
import MainHeader from './components/MainHeader.vue';
import MainVisual from './components/MainVisual.vue';

export default {
  components: {
    MainHeader,
    MainVisual,
  },
  data() {
    return {
      
    };
  },
}
</script>

<style lang="scss">
@import url(./assets/seting.css);
</style>
