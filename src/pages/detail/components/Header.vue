<template>
  <div class="header">
    城市选择
    <router-link tag="div" to="/" class='header-abs'>
      <span class='iconfont iconjiantouxia header-abs-back'></span>
    </router-link>
    <div class='header-fixed'>
      景点详情
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailHeader',

}
</script>

<style lang='stylus' scoped>
.header-abs
  position : absolute
  left: .2rem
  top: .2rem
  width: .8rem
  height: .8rem
  line-height : .8rem
  text-align : center
  border-radius : .4rem
  background: rgba( 0, 0, 0, .8)
  .header-abs-back
    color: #fff
    font-size : .4rem
</style>
