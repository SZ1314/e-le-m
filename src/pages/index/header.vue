<template>
  <div class="header">
    <div class="iconfont">&#xe675;</div>
    <div class="city">北京科技职业学院</div>
  </div>
</template>
<script>
export default {
  name: 'index-header'
}
</script>

<style lang="stylus" scoped>
  @import "../../assets/stylus/varibles.styl";
  .header
    display: flex
    box-sizing: border-box
    align-items: center
    height: .9rem
    padding: .1rem .2rem
    background-image: linear-gradient(90deg,#0af,#0085ff)
    color: #fff
    .iconfont
      font-size: .3rem
      font-weight: bold
    .city
      margin: 0 .05rem
      font-size: .3rem
      font-weight: bold
      max-width: 2rem
      white-space: nowrap
      overflow: hidden
      text-overflow: ellipsis
      position relative
      &:before
        position absolute
        top: .1rem
        right: 0
        content: ""
        border: .06rem solid #fff
        border-color: #fff transparent transparent
</style>
