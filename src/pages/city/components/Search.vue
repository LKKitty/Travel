<template>
  <div class="search">
   <input type="text" class="search-input" placeholder="输入城市名或拼音">
  </div>
</template>

<script>
export default {
  name: 'CitySearch',
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
.search
  height .62rem
  padding 0.1rem
  background $bgColor
  .search-input
    box-sizing border-box
    height 0.62rem
    width 100%
    padding 0 0.1rem
    line-height 0.62rem
    text-align center
    border-radius 0.06rem
    color #666
</style>
