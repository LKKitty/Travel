<template>
  <div class="header">
   城市选择
   <router-link to='/'>
     <div class="iconfont header-back">&#xe624;</div>
   </router-link>
  </div>
</template>

<script>
export default {
  name: 'CityHeader',
  props: {
    city: String
  },
  data () {
    return {
    }
  },
  components: {}
}
</script>

<style lang='stylus' scoped>
@import '~styles/varibles'
.header
  position relative
  overflow hidden
  height $headerHeight
  line-height $headerHeight
  text-align center
  color #ffffff
  background $bgColor
  font-size 0.32rem
  .header-back
    position absolute
    top 0
    left 0
    width 0.64rem
    text-align center
    font-size .4rem
    color #ffffff
</style>
