<template>
    <div>
        <div class="weekend-title">
            周末去哪
        </div>
        <ul>
            <li class="item" v-for="item of WeekList" :key="item.id">
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
  data () {
    return {
      WeekList: [{
        id: '001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1507/82/06e79c5f8d6e7.jpg_r_640x214_5e63707e.jpg',
        title: '当地人玩什么',
        desc: '石家庄人民周末好玩法'
      }, {
        id: '002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1509/79/e3036d299610f8.jpg_r_640x214_ac8d495d.jpg',
        title: '石家庄的秋天',
        desc: '金秋时节无限美，层林尽染好风光'
      }, {
        id: '003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/d1/3070ad726f861b.jpg_r_640x214_39709b85.jpg',
        title: '石家庄必游TOP5',
        desc: '旅游资源丰富，名胜古迹众多'
      }]
    }
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
       padding-bottom:33.9%
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
