<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 3000
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'http://img.zcool.cn/community/01f7a95543380c0000019ae9819de6.jpg@2o.jpg'
      }, {
        id: '0002',
        imgUrl: 'http://img.zcool.cn/community/010d4f582ec1bca84a0d304f14e1b9.jpg'
      }, {
        id: '0003',
        imgUrl: 'http://img.zcool.cn/community/01a39258eddb07a8012049ef53b617.jpg@1280w_1l_2o_100sh.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullets
    bottom: 20px
  .wrapper >>> .swiper-pagination-bullet-active
    background-color: #fff
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 31.25%
    background-color: #eee
    .swiper-img
      width: 100%
</style>
