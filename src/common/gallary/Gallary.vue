<template>
    <div class="container" @click="handleGallaryClick">
        <div class="wrapper">
            <swiper :options="swiperOptions">
                <!-- slides -->
                <swiper-slide 
                    v-for="(item, index) in imgs"
                    :key="index"
                >
                    <img  class='gallary-img' :src="item"/>
                </swiper-slide>
                <!-- Optional controls -->
                <div class="swiper-pagination"  slot="pagination"></div>
            </swiper>
        </div>
    </div>
</template>
<script>
import DetailBanner from './components/Banner'
export default {
    name: 'CommonGallary',
    props: {
        type: Array,
        default () {
            return [
                https://img1.qunarzz.com/p/tts7/1705/51/f52208d80997f702.jpg_r_640x420x90_fbecec04.jpg,
                https://img1.qunarzz.com/p/tts7/1705/51/f52208d80997f702.jpg_r_640x420x90_fbecec04.jpg
            ]
        }
    },
    data () {
        return {
            swiperOptions: {
                pagination: '.swiper-pagination',
                paginationType: 'fraction',
                observeParents: true,
                observer: true
            }
        }
    },
    methods: {
        handleGallaryClick () {
            this.$emit('close')
        }
    }
}
</script>

<style lang="stylus" scoped>
.container >>> .swiper-container
.container
    display : flex
    flex-direction : column
    justify-content : center
    z-index: 99
    position: fixed
    left: 0
    right: 0
    top: 0
    bottom: 0
    background: #000
    .wrapper
        overflow : hidden
        height: 0
        width: 100%
        padding-bottom: 100%
        .gallary-img
            width: 100%
        .swiper-pagination
            color: #fff
            bottom: -1rem
</style>