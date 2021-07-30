<!--
 * @Author: your name
 * @Date: 2021-07-29 16:10:37
 * @LastEditTime: 2021-07-30 16:22:37
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \onmyway-uniapp\pages\coupon\components\city_search_box.vue
-->
<template>
  <view class="city-search">
    <view class="city">
      <view class="top">
        {{ city }}
        <u-icon name="map" size="10"></u-icon>
      </view>
      <view class="bottom">
        {{ weather }}
      </view>
    </view>
    <view class="search">
		<u-search style="color:white" placeholder="日照香炉生紫烟" v-model="keyword"></u-search>
	</view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      city: "沈阳",
      weather: "多云24℃",
	  keyword:""
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
    width: 120rpx;
    height: 100%;
    margin-top: 10px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    font-size: 10rpx;
    .bottom {
      font-size: 6px;
      transform: scale(0.7);
      color: #f2f4f3;
    }
  }
  .search {
    flex: 1;
	.u-action .u-action-active{
		color: #f2f4f3 !important
	}
  }
}
</style>