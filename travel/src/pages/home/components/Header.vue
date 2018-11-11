<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe600;</div>
    </div>
    <div class="header-input">
        <span class="iconfont">&#xe86e;</span>
        输入城市/景点/游玩主题
    </div>
    <router-link to="/city">
        <div class="header-right">
            {{this.city}}
            <span class="iconfont arrow-icon">&#xe601;</span>
        </div>
    </router-link>
  </div>

</template>

<script>
export default {
  name: 'Header',
  props: {
    city: String
  }
}

</script >

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
    .header
        display:flex
        line-height:$headerHeight
        background:$bgcolor
        color:#fff
    .header-left
        width:.64rem
        float:left
      .back-icon
        text-align:center
        font-size:.4rem
    .header-input
        flex:1
        margin-top:.12rem
        margin-left:.2rem
        padding-left:.2rem
        height:.64rem
        line-height:.64rem
        background:#fff
        border-radius:.1rem
        color:#ccc
    .header-right
        width:1.24rem
        float:right
        text-align:center
        color:#fff
      .arrow-icon
            marign-left:-0.4rem
            font-size:.24rem
</style>
