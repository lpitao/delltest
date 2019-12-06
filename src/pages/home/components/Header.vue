<template>
  <div class="header">
    <div class="header-left">
        <span class='iconfont iconjiantouxia'></span>
    </div>
    <div class="header-input">
        <span class='iconfont icontubiao-'></span>
        输入城市/景点、游戏主题</div>
    <router-link to='/city'>
      <div class="header-right">
        {{this.$store.state.city}}
          <span class='iconfont iconfanhui'></span>
      </div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang='stylus' scoped>
@import '~styles/varibles.styl'
.header
    display : flex
    line-height: $headerHeight
    background : $bgColor
    color : #fff
    .header-left
        width : .64rem
        float: left 
        .back-icon
            text-align : center
            font-size: .4rem
    .header-input
        flex:1
        line-height :.64rem
        height: .64rem
        background :#fff
        margin-top: .12rem
        margin-left: .2rem
        border-radius : .1rem
        color: #cccccc
        padding-left : .2rem
    .header-right
        width : 1.24rem
        float : right
        text-align : center
</style>
