<!--
 * @Author: zheng li
 * @Date: 2021-07-29 15:30:58
 * @LastEditTime: 2021-07-30 09:47:01
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \onmyway-uniapp\pages\shop\index.vue
-->
<template>
  <view class="shop">
    <view class="search">
      <search-box></search-box>
    </view>
    <view class="ranking">
      <ranking></ranking>
    </view>
    <view class="shop-list">
      <shop-list></shop-list>
    </view>
  </view>
</template>

<script>
export default {
  components: {
    searchBox: () => import("./components/search_box.vue"),
    ranking: () => import("./components/ranking.vue"),
    shopList: () => import("./components/shop_list.vue"),
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
.shop {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.shop .search {
  width: 100%;
  height: 80rpx;
  background: pink;
}
.shop .ranking {
  width: 100%;
  height: 200rpx;
  background: yellow;
}
.shop .shop-list {
  width: 100%;
  background: greenyellow;
}
</style>
