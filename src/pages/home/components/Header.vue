<template>
  <div class="header">
    <div class="header-left">
      <i class="iconfont back-icon">&#xe624;</i>
    </div>
    <div class="header-input">
      <i class="iconfont">&#xe632;</i>
      输入城市/景点/游玩
    </div>
    <div class="header-right">
      城市
      <i class="iconfont arrow-icon">&#xe6c3;</i>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header
    display: flex
    line-height: .86rem
    background-color: $bgColor
    color: #fff
    .header-left
      width: .64rem
      float: left
      .back-icon
        display: block
        text-align: center
        font-size: .4rem
    .header-input
      flex: 1
      height: .64rem
      line-height: .64rem
      margin-left: .2rem
      padding-left: .2rem
      margin-top: .12rem
      background-color: #fff
      border-radius: .1rem
      color: #ccc
    .header-right
      width: 1.24rem
      float: right
      text-align: center
      .arrow-icon
        margin-left: .04rem
        font-size: .24rem
</style>
