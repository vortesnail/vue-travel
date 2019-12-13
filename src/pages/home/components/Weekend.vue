<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl">
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
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1609/94/945ab5b76758703a3.water.jpg_710x360_cef04618.jpg',
        title: '滕王阁',
        desc: '落霞与孤鹜齐飞，秋水共长天一色'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1501/87/9dcb13572c70d3a2aae83b44121db72b.water.jpg_710x360_2c18a835.jpg',
        title: '庐山风景名胜区',
        desc: '匡庐奇秀甲天下'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p59/201211/02/6fa821e7508df7a193835fbb.jpg_710x360_090aab20.jpg',
        title: '武功山',
        desc: '高山草甸，初见惊艳，再见依然'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .title
    margin-top: .2rem
    line-height: .8rem
    background-color: #eee
    text-indent : .2rem
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 33.9%
    .item-img
      width: 100%
  .item-info
    flex: 1
    padding: .1rem
    min-width: 0
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color: #ccc
      ellipsis()
</style>
