<!--
 * @Author: zheng li
 * @Date: 2021-07-29 15:28:35
 * @LastEditTime: 2021-07-30 17:49:12
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
      <new-box></new-box>
    </view>
    <view class="coupon-list">
      <coupon-list></coupon-list>
    </view>
  </view>
</template>

<script>
import citySearch from "./components/city_search_box.vue";
import banner from "./components/banner.vue";
import newBox from "./components/new_box.vue";
import couponList from "./components/coupon_list.vue";
export default {
  components: {
    citySearch,
    banner,
    newBox,
    couponList,
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

<style lang="scss" scoped>
.coupon {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background: #75c4ce;
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
