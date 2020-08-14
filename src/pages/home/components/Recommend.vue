<template>
    <div>
      <div class="title">热销推荐</div>
      <ul>
        <li class="item" v-for="item of recommendList" :key="item.id">
          <img class="item-img" :src="item.imgUrl" alt="" />
          <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
            <button class="item-btn">查看详情</button>
          </div>
        </li>
      </ul>
    </div>
</template>

<script>
export default {
  name: 'Recommend',
  data () {
    return {
      recommendList: [
        {id: '001', imgUrl: 'https://imgs.qunarzz.com/sight/p0/1707/11/117c70eca99c13e1a3.water.jpg_200x200_d6fbed20.jpg', title: '西部恐龙水乐园室内温泉馆', desc: '欢迎一起来参观'},
        {id: '002', imgUrl: 'https://imgs.qunarzz.com/sight/p0/1707/11/117c70eca99c13e1a3.water.jpg_200x200_d6fbed20.jpg', title: '西部恐龙水乐园室内温泉馆', desc: '欢迎一起来参观'},
        {id: '003', imgUrl: 'https://imgs.qunarzz.com/sight/p0/1707/11/117c70eca99c13e1a3.water.jpg_200x200_d6fbed20.jpg', title: '西部恐龙水乐园室内温泉馆', desc: '欢迎一起来参观'}
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
  .item
    overflow hidden
    display flex
    height 1.9rem
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      flex 1
      padding .1rem
      min-width 0
      .item-title
        line-height .54rem
        font-size .32rem
        ellipse()
      .item-desc
        line-height .4rem
        color #ccc
        ellipse()
      .item-btn
        line-height .44rem
        margin-top .16rem
        background #ff9300
        height .48rem
        border-radius .06rem
        color #ffffff
        width 1.5rem
</style>
