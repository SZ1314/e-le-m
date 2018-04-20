<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <swiper-slide v-for = "(page, index) of pageList" :key = "index">
        <div class="area-con">
          <div class="area-item" v-for = "item of page" :key = "item.id">
            <img class="area-img" :src = "item.imgUrl" :title = "item.title"/>
            <P class="area-desc">{{item.title}}</P>
          </div>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>
<script>
export default {
  name: 'index-icons',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination'
      }
    }
  },
  computed: {
    pageList () {
      const pages = []
      this.list.forEach((value, index) => {
        const page = Math.floor(index / 10)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(value)
      })
      return pages
    }
  }
}
</script>
<style lang="stylus" scoped>
  .icons
    height: 3.6rem
    overflow hidden
    .area-con
      display: flex
      flex-wrap: wrap
      .area-item
        display: flex
        flex-direction: column
        justify-content: space-between
        align-items: center
        margin-top .22rem
        width: 20%
        height: 1.3rem
        .area-img
          width .9rem
          height .9rem
        .area-desc
          text-align center
          overflow hidden
          white-space nowrap
          text-ovrflow ellipsis
          width 100%
          font-size .1rem
</style>
