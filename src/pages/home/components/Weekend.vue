<template>
  <div>
      <div class='title'>周末去哪er</div>
      <ul>
          <li class='item border-bottom' v-for="item of list">
               <div class='item-img-wrapper'>
                   <img class='item-img' :src='item.imgUrl'/>
               </div>
                <p class='item-title'>{{item.title}}</p>
                <p class='item-desc'>{{item.desc}}</p>
          </li>
      </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  components: {

  },
  data () {
    return {

      }
  },
  props: {
    list: Array
  }
}
</script>

<style lang='stylus' scoped>
@import '~styles/varibles.styl'
.title
    line-height : .4rem
    background : #eeeeee
    text-indent : .2rem
.item-img-wrapper
    overflow :hidden
    height: 0
    padding-bottom: 37.09%
    .item-img   
        width: 100%
.item-title
    line-height : .54rem
    font-size: .32rem
    ellipsis()
.item-desc
    line-height : .4rem
    color: #ccc
    ellipsis()
</style>
