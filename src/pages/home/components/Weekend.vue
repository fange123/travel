<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item" v-for="item of weekendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" alt="" />
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'Weekend',
  data () {
    return {
      weekendList: [
        {id: '001', imgUrl: 'https://imgs.qunarzz.com/sight/source/1606/9c/d601bd634c8d50.jpg_r_640x214_909d1d4a.jpg', title: '西部恐龙水乐园室内温泉馆', desc: '欢迎一起来参观'},
        {id: '002', imgUrl: 'https://imgs.qunarzz.com/sight/source/1606/9c/d601bd634c8d50.jpg_r_640x214_909d1d4a.jpg', title: '西部恐龙水乐园室内温泉馆', desc: '欢迎一起来参观'},
        {id: '003', imgUrl: 'https://imgs.qunarzz.com/sight/source/1606/9c/d601bd634c8d50.jpg_r_640x214_909d1d4a.jpg', title: '西部恐龙水乐园室内温泉馆', desc: '欢迎一起来参观'}
      ]
    }
  }
}
</script>
<style scoped lang="stylus">
  @import "~style/mixins.styl"
  .title
    margin-top .2rem
    line-height .8rem
    background #eee
    text-indent .2rem
  .item-img-wrapper
    height 0;
    padding-bottom 33.9%
    overflow hidden
    .item-img
      width 100%
  .item-info
    padding .1rem
    .item-title
      line-height .54rem
      font-size .32rem
      ellipse()
    .item-desc
      line-height .4rem
      color #ccc
      ellipse()
</style>
