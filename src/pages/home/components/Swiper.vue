<template>
  <div class="wrapper">
    <swiper :options="swiperOption" v-if="showSwiper">
    <!-- slides -->
    <swiper-slide v-for="item in swiperList" :key="item.id">
      <img :src="item.imgUrl" class="swiper-img">
    </swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    swiperList: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      }
    }
  },
  computed: {
    showSwiper () {
      return this.swiperList.length
    }
  }
}
</script>

<style lang='stylus' scoped>
.wrapper >>> .swiper-pagination-bullet-active
  background #ffffff
.wrapper
  overflow hidden
  width 100%
  height 0
  padding-bottom 31.3%
  background #eeeeee
  .swiper-img
    width 100%
</style>
