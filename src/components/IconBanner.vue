<template>
  <div class="container">
    <ul class="BanWrap">
        <li v-for="(item,i) in data" :key="i">
            <img :src="`./images/02iconBanner/${item.src}`" alt="">
            <h4 v-html="item.title"></h4>
            <p v-html="item.subtitle"></p>
        </li>
    </ul>
  </div>
</template>

<script>
export default {
    props: ["data"],
}
</script>

<style lang="scss">
    .container{
        .BanWrap{
            display: flex;background: pink;justify-content:space-around;
            padding: 90px 0;
            li{
                display: flex;justify-content: center;align-items: center;
                flex-direction: column;
                cursor: pointer;
                &:hover img{transform: translateY(-30px);}
                img{
                    height: 140px;margin-bottom: 25px;
                    transition: 0.3s;
                    }
                h4{text-align: center;font-size: 18px;font-weight: bold;margin-bottom: 10px;}
                p{font-size: 15px;text-align: center;}
            }
        }
    }
</style>