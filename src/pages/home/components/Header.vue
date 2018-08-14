<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市景点游玩主题
    </div>
    <router-link to="/City" tag="div">
       <div class="header-right">
     {{this.city}}
      <span class="iconfont arrow-icon">&#xe64a;</span>
    </div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'Header',
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
  display flex
  line-height 0.86rem
  background $bgColor
  color #ffffff
  .header-left
    width .64rem
    float left
    .back-icon
      text-align center
      font-size 0.4rem
  .header-input
    flex 1
    height 0.64rem
    line-height 0.64rem
    margin-top 0.12rem
    margin-left 0.2rem
    padding-left 0.2rem
    background #ffffff
    border-radius 0.1rem
    color #ccc
  .header-right
    width 1.24rem
    float right
    text-align center
    .arrow-icon
      margin-left -.04rem
      font-size 0.24rem
</style>
