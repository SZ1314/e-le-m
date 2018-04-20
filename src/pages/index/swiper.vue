<template>
  <div class="slide-content">
    <swiper :options="swiperOption">
      <swiper-slide v-for = "item of list" :key = "item.id">
        <img class="slide-img" :src = "item.imgUrl" />
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'index-swiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        loop: true,
        autoplay: 3000,
        pagination: '.swiper-pagination'
      }
    }
  }
}
</script>
<style lang="stylus" scoped>
  .slide-content
    overflow: hidden
    height: 0
    padding-bottom: 28.1%
    .slide-img
        width:100%
</style>
