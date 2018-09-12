<template>
  <div class="list">
    <div class="item" v-for="(item,key) of cities" :key="key">{{key}}</div>
  </div>
</template>

<script>
export default {
  name: 'CityAlphabet',
  props: {
    cities: Object
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
.list
  display flex
  flex-direction column
  justify-content center
  position absolute
  top 1.64rem
  right 0
  bottom 0
  width 0.4rem
  .item
    line-height 0.4rem
    text-align center
    color $bgColor
</style>
