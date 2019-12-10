<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div
          class="icon"
          v-for="item of page"
          :key="item.id"
        >
          <div class="icon-img">
            <img class="icon-img-content" :src="item.imgUrl" alt="icon">
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
import bable from '@/assets/icons/bable.png'
import candy from '@/assets/icons/candy.png'
import card from '@/assets/icons/card.png'
import gift from '@/assets/icons/gift.png'
import lu from '@/assets/icons/lu.png'
import oldman from '@/assets/icons/oldman.png'
import redwine from '@/assets/icons/redwine.png'
import snowman from '@/assets/icons/snowman.png'
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconList: [{
        id: '0001',
        imgUrl: bable,
        desc: '热门书籍'
      }, {
        id: '0002',
        imgUrl: candy,
        desc: '果蔬菜糖'
      }, {
        id: '0003',
        imgUrl: card,
        desc: '圣诞贺卡'
      }, {
        id: '0004',
        imgUrl: gift,
        desc: '热门礼物'
      }, {
        id: '0005',
        imgUrl: lu,
        desc: '花样宠物'
      }, {
        id: '0006',
        imgUrl: oldman,
        desc: '戏耍老头'
      }, {
        id: '0007',
        imgUrl: redwine,
        desc: '法式红酒'
      }, {
        id: '0008',
        imgUrl: snowman,
        desc: '来打雪仗'
      }, {
        id: '0009',
        imgUrl: bable,
        desc: '热门书籍'
      }]
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

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  @import '~styles/mixins.styl'
  .icons >>> .swiper-container
    height: 0
    padding-bottom: 50%
  .icon
    position: relative
    overflow: hidden
    float: left
    width: 25%
    height: 0
    padding-bottom: 25%
    .icon-img
      position: absolute
      top: 0
      left: 0
      right: 0
      bottom: .44rem
      box-sizing: border-box
      padding: .1rem
      display: flex
      align-items: center
      justify-content: center
      .icon-img-content
        display: block
        height: 80%
        padding: .18rem
        border-radius: .4rem
        background-color: #00bcd4
    .icon-desc
      position: absolute
      left: 0
      right: 0
      bottom: 0
      height: .44rem
      line-height: .44rem
      color: $darkTextColor
      text-align: center
      ellipsis()
</style>
