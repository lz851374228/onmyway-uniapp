<!--
 * @Author: zheng li
 * @Date: 2021-07-29 15:28:35
 * @LastEditTime: 2021-07-30 09:31:53
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \onmyway-uniapp\pages\coupon\index.vue
-->
<template>
  <view class="coupon">
    <view class="top">
      <city-search></city-search>
    </view>
    <view class="banner">
      <banner></banner>
    </view>
    <view class="new">
      <new></new>
    </view>
    <view class="coupon-list">
      <coupon-list></coupon-list>
    </view>
  </view>
</template>

<script>
export default {
  components: {
    citySearch: () => import("./components/city_search_box.vue"),
    banner: () => import("./components/banner.vue"),
    new: () => import("./components/new.vue"),
    couponList: () => import("./components/coupon_list.vue"),
  },
  data() {
    return {
      title: "Hello",
    };
  },
  onLoad() {},
  methods: {},
};
</script>

<style>
.coupon {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.coupon .top {
  width: 100%;
  height: 80rpx;
  background: pink;
}
.coupon .banner {
  width: 100%;
  background: skyblue;
}
.coupon .new {
  width: 100%;
  height: 120rpx;
  background: yellow;
}
.coupon .coupon-list {
  width: 100%;
}
</style>
