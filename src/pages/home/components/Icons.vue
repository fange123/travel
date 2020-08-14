<template>
    <div class="icons">
      <swiper>
        <swiper-slide v-for="(page,index) of pages" :key="index">
          <div class="icon" v-for="item of page" :key="item.id">
            <div class="icon-image" >
              <img class="icon-image-content" :src="item.imgUrl" alt="" />
            </div>
            <p class="icon-content">{{item.desc}}</p>
          </div>
        </swiper-slide>
      </swiper>
    </div>
</template>

<script>
export default {
  name: 'homeIcons',
  data () {
    return {
      iconList: [
        {id: '001', imgUrl: 'https://s.qunarzz.com/homenode/images/touchheader/hotel.png', desc: '酒店'},
        {id: '002', imgUrl: 'https://s.qunarzz.com/homenode/images/touchheader/flight.png', desc: '机票'},
        {id: '003', imgUrl: 'https://s.qunarzz.com/homenode/images/touchheader/train.png', desc: '火车票'},
        {id: '004', imgUrl: 'https://s.qunarzz.com/homenode/images/touchheader/package.png', desc: '七彩丹霞'},
        {id: '005', imgUrl: 'https://s.qunarzz.com/homenode/images/touchheader/piao.png', desc: '海洋馆'},
        {id: '006', imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png', desc: '月牙泉'},
        {id: '007', imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20198/0d9d40366944421b906683a906c4f22f.png', desc: '莫高窟'},
        {id: '008', imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20197/011dbbb4b74df765dadf13a50af027e8.png', desc: '周边游'},
        {id: '009', imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1803/dd/cce1231836f10a02.png', desc: '一日游'}
      ]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style scoped lang="stylus">
  @import "~style/varibles.styl"
  @import "~style/mixins.styl"
  .icons >>> .swiper-container
    width 100%
    height 0
    padding-bottom 50%
    touch-action: none;
  .icon
    float left
    width 25%
    padding-bottom 25%
    overflow hidden
    position relative
    .icon-image
      position absolute
      top 0
      left 0
      right 0
      bottom .44rem
      box-sizing border-box
      padding .1rem
      .icon-image-content
        display block
        margin 0 auto
        height 100%
    .icon-content
      position absolute
      height .44rem
      left 0
      right 0
      bottom 0
      line-height .44rem
      text-align center
      color $darkTextColor
      ellipsis()

</style>
