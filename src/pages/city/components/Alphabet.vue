<template>
  <div class="list">
    <div class="item"
      v-for="item of letters"
      :key="item"
      :ref="item"
      @touchstart="handleTocuhStart"
      @touchmove="handleTocuhMove"
      @touchend="handleTocuhEnd"
      @click="handleLetterClick"
    >
      {{item}}</div>
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
      touchStatus: false,
      startY: 0,
      timer: null
    }
  },
  updated () {
    this.startY = this.$refs['A'][0].offsetTop
  },
  computed: {
    letters () {
      const letters = []
      for (let i in this.cities) {
        letters.push(i)
      }
      return letters
    }
  },
  methods: {
    handleLetterClick (e) {
      this.$emit('change', e.target.innerText)
      // for (let i = 0; i < this.$refs.item.length; i++) {
      //   this.$refs.item[i].style.color = '#00bcd4'
      // }
      // e.target.style.color = 'red'
    },
    handleTocuhStart () {
      this.touchStatus = true
    },
    handleTocuhMove (e) {
      if (this.timer) {
        clearTimeout(this.timer)
      }
      this.timer = setTimeout(() => {
        if (this.touchStatus) {
          const touchY = e.touches[0].clientY - 79
          const index = (touchY - this.startY) / 20 | 0
          if (index >= 0 && index < this.letters.length) {
            this.$emit('change', this.letters[index])
          }
        }
      }, 16)
    },
    handleTocuhEnd () {
      this.touchStatus = false
    }
  }
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
