<template>
  <div class="wrap">
    <swiper :options="swiperOption" ref="mySwiper">
      <!-- slides -->
      <swiper-slide v-for="item of list" :key="item.id"><img class="slide-img" :src="item.imgUrl" alt=""></swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
    export default {
        name: "slider",
        data () {
          return {
            swiperOption: {
              pagination: '.swiper-pagination',
              loop:true,
              autoplay: 3000
            },
            list: [
              {
                id: '001',
                imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/0cec5adeeac137e202e2ebf3f44e2045.jpg_750x200_d62d9c73.jpg'
              },
              {
                id: '002',
                imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/3f47010a2312c32fff92fec3bcc99563.jpg_750x200_7ae774e5.jpg'
              },
              {
                id: '003',
                imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/ed5f4115226306e48e6fad106a038afe.jpg_750x200_64df48d6.jpg'
              },
              {
                id: '004',
                imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/87a224d0349d94a11e97f31aa1aba4f5.jpg_750x200_1f78af87.jpg'
              },
              {
                id: '005',
                imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/389d0194766566f8f1185aa19b759c25.jpg_750x200_22620261.jpg'
              }
            ]
          }
        }
    }
</script>

<style lang="stylus" scoped>
  .wrap >>> .swiper-pagination-bullet
    background: rgba(255,255,255, .5)
  .wrap >>> .swiper-pagination-bullet-active
    background: rgba(255,255,255,1)
  .wrap
    overflow: hidden
    height: 0
    padding-bottom: 26.66666667%
    .slide-img
      width: 100%
</style>
