<template>
  <ul class="list">
      <li class="item" v-for="(item, key) of cities"
                       :key="key"
                       :ref="key"
                       @click="Aiphabetclick"
                       @touchstart="handleTouchStart"
                       @touchmove="handleTouchMove"
                       @touchend="handleTouchEnd"
      >
      {{key}}
      </li>
  </ul>
</template>

<script type="text/javascript">
export default {
  name: 'CityAlphabet',
  props: {
    cities: Object
  },
  computed: {
    letters () {
      const letters = []
      for (let i in this.cities) {
        letters.push(i)
      }
      return letters
    }
  },
  data () {
    return {
      touchStatus: false,
      startY: 0,
      timer: null
    }
  },
  updated () {
    this.startY = this.$refs['A'][0].offsetTop
  },
  methods: {
    Aiphabetclick (e) {
      const letterName = e.target.innerText
      this.$emit('change', letterName)
    },
    handleTouchStart () {
      this.touchStatus = true
    },
    handleTouchMove (e) {
      if (this.timer) {
        clearTimeout(this.timer)
      }
      this.timer = setTimeout(() => {
        if (this.touchStatus) {
          const touchY = e.touches[0].clientY - 79
          const index = Math.floor((touchY - this.startY) / 20)
          if (index >= 0 && index <= this.letters.length) {
            this.$emit('change', this.letters[index])
          }
        }
      }, 16)
    },
    handleTouchEnd () {
      this.touchStatus = false
    }
  }
}
</script>

<style type="text/css" lang="stylus" scoped>
@import '~styles/varibles.styl'
.list
  display:flex
  flex-direction:column
  justify-content:center
  position:absolute
  top:1.58rem
  right:0
  bottom:0
  width:.4rem
  .item
    line-height:.4rem
    text-align:center
    color:$bgcolor
</style>
