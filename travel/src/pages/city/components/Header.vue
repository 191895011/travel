<template>
  <div class="Header">
      城市选择
    <router-link to="/">
      <div class="iconfont city-back">&#xe600;</div>
    </router-link>
  </div>
</template>

<script type="text/javascript">
export default {
  name: 'CityHeader'
}
</script>

<style type="text/css" lang="stylus" scoped>
@import '~styles/varibles.styl'
 .Header
   position:relative
   height:$headerHeight
   line-height:$headerHeight
   color:#fff
   background: $bgcolor
   text-align:center
   font-size:.4rem
   .city-back
     position:absolute
     left:0
     top:0
     width:.64rem
     color:#fff
     font-size:.4rem

</style>
