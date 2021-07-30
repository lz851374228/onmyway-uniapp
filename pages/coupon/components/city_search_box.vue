<!--
 * @Author: your name
 * @Date: 2021-07-29 16:10:37
 * @LastEditTime: 2021-07-30 17:49:43
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \onmyway-uniapp\pages\coupon\components\city_search_box.vue
-->
<template>
  <view class="city-search">
    <view class="city">
      <view>
        {{ city }}
        <u-icon name="map" size="10"></u-icon>
      </view>
      <view class="bottom">
        {{ weather }}
      </view>
    </view>
    <view class="search">
      <u-search
        style="color: white"
        placeholder="日照香炉生紫烟"
        v-model="keyword"
      ></u-search>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      city: "沈阳",
      weather: "多云24℃",
      keyword: "",
    };
  },
  onLoad() {},
  methods: {},
};
</script>

<style lang="scss" scoped>
.city-search {
  display: flex;
  flex-direction: row;
  color: white;
  align-items: center;
  justify-content: space-around;
  width: 100%;
  height: 100%;
  .city {
    width: 16%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    font-size: 20rpx;
    .bottom {
      font-size: 20rpx;
      transform: scale(0.7);
    }
  }
  .search {
    flex: 1;
  }
}
</style>