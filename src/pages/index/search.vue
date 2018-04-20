<template>
  <div class="search">
    <div class="content">
      <span class="iconfont">&#xe673;</span>
      搜索饿了么商家、商品名称
    </div>
  </div>
</template>
<script>
export default {
  name: 'index-search'
}
</script>
<style lang="stylus" scoped>
  .search
    display: flex
    box-sizing: border-box
    item-align: center
    height: 1rem
    padding: .18rem .2rem
    background-image: linear-gradient(90deg,#0af,#0085ff)
    color: #fff
    .iconfont
      font-size: .3rem
    .content
      display: flex
      justify-content: center
      align-items: center
      width: 100%
      height: 100%
      background: #fff
      color: #999
</style>
