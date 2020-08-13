<template>
    <div class="header">
      <div class="header-left">
        <div class="iconfont back-icon">&#xe602;</div>
      </div>
      <div class="header-input">
        <span class="iconfont">&#xe600;</span>
        请输入城市名/景点/游玩主题</div>
      <div class="header-right">
        城市
        <span class="iconfont city-icon">&#xe665;</span>
      </div>
    </div>
</template>

<script>
export default {
  name: 'homeHeader'
}
</script>

<style scoped lang="stylus">
  @import "~style/varibles.styl"
  .header
    display flex
    line-height .86rem
    background $bgColor
    color #fff
    .back-icon
      text-align center;
      font-size .35rem
    .header-left
      text-align center
      float left
      width .64rem
    .header-input
      padding-left .2rem
      flex 1
      height .64rem
      line-height .64rem
      margin-top .12rem
      margin-left .2rem;
      background #fff
      color #ccc
      border-radius .1rem
    .header-right
      width 1.24rem
      float right
      text-align center
      .city-icon
        font-size .2rem
</style>
