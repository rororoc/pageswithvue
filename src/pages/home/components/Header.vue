<template>
<div class="header">
  <div class="header-left">
    <span class="iconfont">&#xe624;</span>
  </div>
  <div class="header-input"><span class="iconfont">&#xe632;</span>输入城市/景点/游玩主题</div>
  <div class="header-right">城市<span class="iconfont">&#xe64a;</span></div>
</div>
</template>

<script>
    export default {
        name: "homeheader",

    }
</script>

<style lang="stylus" scoped>
@import '~styles/var.styl'
  .header
    display: flex
    height:0.88rem
    line-height: 0.88rem
    background-color: $bgColor
    .header-left
      float: left
      width:0.4rem
      line-height: .88rem
      padding: 0 .2rem
      color: #ffffff
      font-size: .36rem
    .header-input
      flex:1
      padding-left 0.2rem
      background #ffffff
      height: .6rem
      margin: .14rem 0
      line-height: .6rem
      border-radius 0.06rem
      color: #e4e7ea
      ellipsis()
      .iconfont
        font-size 0.34rem
    .header-right
      float: right
      width: 1.3rem
      text-align center
      color: #ffffff
      .iconfont
        font-size 0.24rem
        padding-left: 0.1rem
</style>
