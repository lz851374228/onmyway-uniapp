<!--
 * @Author: zheng li
 * @Date: 2021-07-29 15:28:35
 * @LastEditTime: 2021-07-30 16:56:12
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
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background: #75C4CE
}
.coupon .top {
  width: 100%;
  height: 80rpx;
}
.coupon .banner {
  width: 100%;
}
.coupon .new {
  width: 100%;
  height: 120rpx;
}
.coupon .coupon-list {
  width: 100%;
  flex: 1;
}
</style>
