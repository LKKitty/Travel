<template>
  <div>
    <div class="title">
     周末去哪儿
    </div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
           <img class="item-img" :src="item.imgUrl" alt="">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}></p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/53/02091f1ee43d0a.jpg_r_640x214_2e3256b1.jpg',
        title: '北京国际鲜花港',
        desc: '啦啦啦啦啦啦啦'
      },
      {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/aa/7baaf8a851d221.jpg_r_640x214_1431200f.jpg',
        title: '北京国际鲜花港',
        desc: '啦啦啦啦啦啦啦'
      },
      {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/9e/21df651e19af5d.jpg_r_640x214_3ea5bb38.jpg',
        title: '北京国际鲜花港',
        desc: '啦啦啦啦啦啦啦'
      },
      {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/ce/bc89bc2f0e33ea.jpg_r_640x214_3e408453.jpg',
        title: '北京国际鲜花港',
        desc: '啦啦啦啦啦啦啦'
      }
      ]
    }
  },
  components: {}
}
</script>

<style lang='stylus' scoped>
@import '~styles/mixins.styl'
.title
  margin-top: 0.2rem
  line-height: 0.8rem
  background: #eeeeee
  text-indent: 0.2rem
.item-img-wrapper
  overflow hidden
  height 0
  padding-bottom 33.9%
  .item-img
    width 100%
.item-info
  flex 1
  padding .1rem
  min-width 0
  .item-title
    line-height 0.54rem
    font-size 0.32rem
    ellisdis()
  .item-desc
    line-height .4rem
    font-size .28rem
    color #cccccc
    ellisdis()
  </style>
