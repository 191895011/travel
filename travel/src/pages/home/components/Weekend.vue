<template>
    <div>
        <div class="weekend-title">
            周末去哪
        </div>
        <ul>
            <li class="item" v-for="item of weekendList" :key="item.id">
                <div class="item-img-warpper">
                    <img  class="item-img" :src="item.imgUrl " alt="" />
                </div>
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                </div>
            </li>
        </ul>
    </div>
</template>

<script type="text/javascript">
export default {
  name: 'Weekend',
  props: {
    weekendList: Array
  }
}
</script>

<style type="text/css" lang="stylus" scpoed>
@import '~styles/mixins.styl'
  .weekend-title
    margin-top:.2rem
    line-height:.8rem
    background:#eee
    text-indent:.2rem
  .item
    .item-img-warpper
       overflow:hidden
       width:100%
       height:0
       padding-bottom:37.9%
      .item-img
         display:block
         width:100%
    .item-info
      padding:.1rem
      .item-title
         height:.54rem
         line-height:.54rem
         font-size:.32rem
         ellipsis()
      .item-desc
        line-height:.4rem
        color:#ccc
        ellipsis()
</style>
