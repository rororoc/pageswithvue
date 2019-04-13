<template>
<div class="like-group lazy-load border-bottom">
  <div class="like-group-title">
    <img class="like-img" src="http://img1.qunarzz.com/piao/fusion/1711/89/ebc329f16c55bb02.png" alt="">
    <span class="like-title">猜你喜欢</span>
  </div>
  <ul class="like-list">
    <li class="like-item border-bottom test" v-for="item of likelist" :key="item.id">
      <a href="" class="like-fulllink">
        <div class="like-imgcon">
          <img :src="item.imgUrl" alt="" class="like-img">
        </div>
        <div class="like-info">
          <h3 class="like-info-title">{{item.liketitle}}</h3>
          <div class="like-info-comment">
            <span class="like-starlevel">
              <span class="like-starlevel-gain iconfont">&#xe61a;&#xe61a;&#xe61a;&#xe61a;&#xe61a;</span>
              <span class="like-starlevel-total"></span>
            </span>
            <span class="like-comment-num">{{item.commentnum}}条评论</span>
          </div>
          <div class="like-price">
            <span class="like-price-tag">$<em class="like-price-num">{{item.price}}</em>起</span>
            <span class="like-area">{{item.area}}</span>
          </div>
        </div>
      </a>
    </li>
  </ul>
</div>
</template>

<script>
    export default {
        name: "like",
        data(){
          return {
            likelist:[
              {
                id:'0001',
                imgUrl:'http://img1.qunarzz.com/sight/p0/1601/d4/d4f1a62140b9d93590.img.jpg_200x200_a1ff6094.jpg',
                liketitle:'牛首山文化旅游区',
                price:'87',
                area:'江北',
                commentnum:'5654',
                stars:'5'
              },
              {
                id:'0003',
                imgUrl:'http://img1.qunarzz.com/sight/201312/03/38da27f8a2ad319ec8d65eac.jpg_200x200_72a1d26d.jpg',
                liketitle:'红山森林动物园',
                price:'87',
                area:'江宁区',
                commentnum:'5654',
                stars:'5'
              },
              {
                id:'0002',
                imgUrl:'http://img1.qunarzz.com/sight/p0/1511/ea/eaf1bdc38aed9e6690.img.jpg_200x200_3032bf56.jpg',
                liketitle:'银杏湖乐园',
                price:'87',
                area:'南信大',
                commentnum:'5654',
                stars:'5'
              },
              {
                id:'0004',
                imgUrl:'http://img1.qunarzz.com/sight/p0/1411/13/0cd5a9a57ae0d1b9b935ec604ce0f9bf.water.jpg_200x200_9b808f51.jpg',
                liketitle:'南京海底世界',
                price:'87',
                area:'盘城镇',
                commentnum:'5654',
                stars:'5'
              },{
                id:'0006',
                imgUrl:'http://img1.qunarzz.com/sight/p0/1703/6a/6ae455f41a6daab2a3.water.jpg_200x200_347a48dd.jpg',
                liketitle:'老山国家森林公园',
                price:'87',
                area:'浦口区',
                commentnum:'5654',
                stars:'5'
              }
            ]
          }
        }
    }
</script>

<style lang="stylus" scoped>
@import '~styles/var.styl'
  .like-group-title
    padding: .24rem 0 .26rem
    margin-top: 0.2rem
    .like-img
      width: 0.32rem
      height: 0.32rem
      margin-left: 0.2rem
      vertical-align top
    .like-title
      display: inline-block
      margin-left:.1rem
      height: .44rem
      line-height .44rem
      color: #212121
      font-size .32rem
  .like-list
    margin-left: .24rem
    .like-item
      padding: .2rem 0
      margin-right: .2rem
      overflow: hidden
    .like-item:last-child::before
      display: none
    .like-fulllink
     display: flex
     .like-imgcon
       width: 2rem
       .like-img
         width:100%
     .like-info
      margin-left .2rem
      flex: 1 1 auto
      .like-info-title
        margin-top: 0.2rem
        color: #212121
        font-size: .32rem
        height: .44rem
        line-height:.44rem
      .like-info-comment
        margin-top: .14rem
        height: .34rem
        .like-starlevel
          display: inline-block
          width:1.5rem
          height: .28rem
          line-height:.28rem
          font-size:.28rem
          letter-spacing:.02rem
          .like-starlevel-gain
            color: #ffb436
            font-size: .28rem
        .like-comment-num
          color: $textlightcolor
          font-size:.26rem
          margin-left: .4rem
      .like-price
        display: flex
        margin-top: 0.4rem
        line-height:.4rem
        justify-content space-between
        .like-price-tag
          color: #ff8300
          font-size:.24rem
          line-height:.4rem
          .like-price-num
            font-size:.36rem
            font-weight: bold
        .like-area
          margin-right: .4rem
          color: $textlightcolor
</style>
