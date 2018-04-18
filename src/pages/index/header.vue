<template>
  <div class="header">
    <div class="iconfont">&#xe63f;</div>
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
    height: .88rem
    line-height: .88rem
    padding: .1rem .2rem
    background-image: linear-gradient(90deg,#0af,#0085ff)
    color: #fff
    .iconfont
      font-size: .4rem
      font-weight: bold
    .city
      margin: 0 .05rem
      font-size: .38rem
      font-weight: bold
      max-width: 3rem
      white-space: nowrap
      overflow: hidden
      text-overflow: ellipsis
      position relative
      &:before
        position absolute 
        top: .4rem
        right: 0
        content: ""
        border: .1rem solid #fff
        border-color: #fff transparent transparent  
</style>
