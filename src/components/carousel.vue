<template>
  <div class='carousel'>
     <swiper :options="swiperOption" ref="mySwiper" class="swiper_container">

    <swiper-slide class="swiper_item"><img src="../../static/carousel3.png" /></swiper-slide>
    <swiper-slide  class="swiper_item"><img src="../../static/carousel1.png" /></swiper-slide>
    <swiper-slide  class="swiper_item"><img src="../../static/carousel2.png" /></swiper-slide>
    
    <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
  import "swiper/dist/css/swiper.css";
  import {swiper,swiperSlide} from "vue-awesome-swiper";
  export default {
    name: 'carousel',
    components: {
      swiper,
      swiperSlide
    },
    data() {
      return {
        swiperOption: {
          pagination: {
            el: '.swiper-pagination',
            dynamicBullets: true
          },
          autoplay: {
            delay: 2500,
            disableOnInteraction: false
          }
        }
      };
    },
    computed: {
      swiper() {
      return this.$refs.mySwiper.swiper;
      }
    },
    mounted() {
      console.log('this is current swiper instance object', this.swiper);
      this.swiper.slideTo(3,1000,false);
    }
  };
</script>

<style lang='less' scoped>
  .caousel {
    .swiper_container {
      width: 100%;
      height: 180px;
    }
  }
  img {
    width: 100%;
    height: 180px;
  }
</style>