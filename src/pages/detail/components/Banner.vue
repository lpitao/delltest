<template>
    <div>
        <div  class="banner" @click="handleBannerClick">
            <img class="banner-img" src="https://img1.qunarzz.com/vs_ceph_vs_tts/99e43fe9-5680-4702-81d1-fd4f20f5fdd6.jpg_r_640x420x90_6834ad54.jpg"/>
            <div class="banner-info">
                <div class="banner-title">
                    dsfsfsdfd
                </div>
                <div class="banner-number">39</div>
            </div>
        </div>
        <!-- <common-gallary 
            :imgs="imgs" 
            v-show="showGallary"
            @close="handleGallaryClose"
        ></common-gallary> -->
    </div>
</template>
<script>
//import CommonGallary from '@/common/gallary/Gallary'
export default {
    name: 'DetailBanner',
    data (){
        return {
             imgs: ['https://img1.qunarzz.com/p/tts7/1705/51/f52208d80997f702.jpg_r_640x420x90_fbecec04.jpg']
        }
    },
    methods: {
        handleBannerClick () {
            this.showGallary = true
        },
        handleGallaryClose(){
            this.showGallary = false
        }
    },
    components: {
        //CommonGallary
    }
}
</script>

<style lang="stylus" scoped>
.banner
    position : relative
    overflow :hidden
    height: 0
    padding-bottom: 55%
    .banner-img
        width : 100%
    .banner-info
        display : flex
        position :absolute
        left: 0
        right : 0
        bottom: 0
        line-height : .6rem
        color: #fff
        background-image : linear-gradient(top, rgba(0,0,0,0),rgba(0,0,0,0.8))
        .banner-title
            flex: 1
            font-size: .32rem
            padding: 0 .2rem
        .banner-number
            margin-top: .14rem
            padding: 0 .4rem
            height: .32rem
            line-height : .32rem
            border-radius : .2rem
            background : rgba(0,0,0,.8)
            font-size: .24rem
</style>