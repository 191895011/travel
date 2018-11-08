<template>
    <div>
        <div class="recommend-title">
            热门推荐
        </div>
        <ul>
            <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
                <div class="item-img-wrapper">
                    <img class="item-img" :src="item.imgUrl" alt="" />
                </div>
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                    <button class="item-button">查看详情</button>
                </div>
            </li>
        </ul>
    </div>
</template>

<script type="text/javascript">
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1411/f2/17a02b681cbfb4545250a3f201cdad19.water.jpg_200x200_408ff2cb.jpg',
        title: '京东第一温泉度假村',
        desc: '京东第一温泉'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1411/f2/17a02b681cbfb4545250a3f201cdad19.water.jpg_200x200_408ff2cb.jpg',
        title: '京东第一温泉度假村',
        desc: '京东第一温泉'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1411/f2/17a02b681cbfb4545250a3f201cdad19.water.jpg_200x200_408ff2cb.jpg',
        title: '京东第一温泉度假村',
        desc: '京东第一温泉'
      }]
    }
  }
}

</script>

<style type="text/css" lang="stylus" scoped>
  @import '~styles/mixins.styl'
    .recommend-title
      margin-top:.2rem
      height:.8rem
      line-height:.8rem
      background:#eee
      text-indent:.2rem
    .item
      overflow:hidden
      display:flex
      height:1.9rem
      .item-img
        width:1.7rem
        height:1.7rem
        padding:.1rem
      .item-info
         flex:1
         padding:.1rem
         min-width:0
        .item-title
          line-height:.54rem
          font-size:.32rem
          ellipsis()
        .item-desc
          line-height:.4rem
          color:#ccc
          ellipsis()
        .item-button
          margin-top:.2rem
          background:#ff9300
          padding:0 .2rem
          border-radius:.06rem
          color:#fff
          ellipsis()
</style>
