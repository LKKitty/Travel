<template>
  <div>
    <div class="title">
      热销推荐
    </div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
          <img class="item-img" :src="item.imgUrl" alt="">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecomment',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1803/12/126471e0966aca5ba3.img.jpg_200x200_f1286016.jpg',
        title: '北京国际鲜花港',
        desc: '啦啦啦啦啦啦啦'
      },
      {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1803/12/126471e0966aca5ba3.img.jpg_200x200_f1286016.jpg',
        title: '北京国际鲜花港',
        desc: '啦啦啦啦啦啦啦'
      },
      {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1803/12/126471e0966aca5ba3.img.jpg_200x200_f1286016.jpg',
        title: '北京国际鲜花港',
        desc: '啦啦啦啦啦啦啦'
      },
      {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1803/12/126471e0966aca5ba3.img.jpg_200x200_f1286016.jpg',
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
.item
  overflow hidden
  display flex
  height 1.9rem
  .item-img
    width 1.7rem
    height 1.7rem
    padding 0.1rem
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
    .item-button
      line-height 0.44rem
      margin-top 0.16rem
      background #ff9300
      padding 0.02rem
      border-radius 0.06rem
      font-size 0.20rem
      color #ffffff
</style>
