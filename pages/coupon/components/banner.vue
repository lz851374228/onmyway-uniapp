<!--
 * @Author: your name
 * @Date: 2021-07-29 16:11:00
 * @LastEditTime: 2021-07-30 11:35:45
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \onmyway-uniapp\pages\coupon\components\banner.vue
-->
<template>
  <view class="banner-content">
    <view class="wrap">
      <u-swiper :list="list"></u-swiper>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      list: [
        {
          image: "https://cdn.uviewui.com/uview/swiper/1.jpg",
          title: "昨夜星辰昨夜风，画楼西畔桂堂东",
        },
        {
          image: "https://cdn.uviewui.com/uview/swiper/2.jpg",
          title: "身无彩凤双飞翼，心有灵犀一点通",
        },
        {
          image: "https://cdn.uviewui.com/uview/swiper/3.jpg",
          title: "谁念西风独自凉，萧萧黄叶闭疏窗，沉思往事立残阳",
        },
      ],
    };
  },
  onLoad() {},
  methods: {},
};
</script>
<style lang="scss" scoped>
.wrap {
  padding: 10rpx 15rpx;
  
}
</style>