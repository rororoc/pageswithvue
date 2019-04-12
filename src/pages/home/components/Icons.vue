<template>
  <div class="icons-wrap">
    <swiper :options="swiperOption" ref="mySwiper">
      <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img-wrap">
            <img class="icon-img" :src="item.imgUrl" alt="">
          </div>
          <div class="icon-desc">{{item.desc}}</div>
        </div>
      </swiper-slide>
      <div class="swiper-pagination icon-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
    name: "icons",
    data () {
      return {
        swiperOption:{
          pagination: '.icon-pagination'
        },
        iconlist: [
          {
            id: '0001',
            imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
            desc: '景点门票'
          },
          {
            id: '0002',
            imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
            desc: '一日游'
          },
          {
            id: '0003',
            imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
            desc: '文化古迹'
          },
          {
            id: '0004',
            imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/47/c2b659e048b11602.png',
            desc: '溜娃'
          },
          {
            id: '0005',
            imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/bd/9f7b9b2b60c1502.png',
            desc: '踏青赏花'
          },
          {
            id: '0006',
            imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/c1/6f15f887179fa002.png',
            desc: '夫子庙'
          },
          {
            id: '0007',
            imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/f6dda1876c5950d83cc159c8fd522943.png',
            desc: '总统府'
          },
          {
            id: '0008',
            imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/97/02f5043b51b2102.png',
            desc: '牛首山'
          },
          {
            id: '0009',
            imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/ac9ef584416467d8cc557aad650959fd.png',
            desc: '银杏湖'
          },
          {
            id: '00010',
            imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
            desc: '明孝陵'
          }
        ]
      }
    },
    computed: {
      pages: function () {
        const pages = []
        this.iconlist.forEach((item,index) => {
          const page = Math.floor(index/8)
          if (!pages[page]) {
            pages[page] = []
          }
          pages[page].push(item);
        })
        return pages
      }
    }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/var.styl'
  @import '~styles/minx.styl'
  .icons-wrap >>> .swiper-pagination-bullet-active
    background: $bgColor
  .icons-wrap >>> .swiper-container
    margin-top: 0.1rem
    overflow: hidden
    height: 0
    padding-bottom: 50%
    .icon
      position: relative
      overflow: hidden
      float: left
      width: 25%
      height: 0
      padding-bottom: 25%
      .icon-img-wrap
        position: absolute
        top:0
        left:0
        right:0
        bottom:.44rem
        box-sizing border-box
        padding: 0.1rem
        .icon-img
          display: block
          margin:0 auto
          height:100%
      .icon-desc
        position: absolute
        left: 0
        right: 0
        bottom:0
        height:0.44rem
        line-height:0.44rem
        text-align: center
        color: $textdarkcolor
        ellipsis()
</style>
