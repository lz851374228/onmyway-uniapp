<!--
 * @Author: your name
 * @Date: 2021-07-29 15:30:50
 * @LastEditTime: 2021-07-30 09:50:04
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \onmyway-uniapp\pages\my\index.vue
-->
<template>
  <view class="my">
    <view class="base-box">
      <base-box></base-box>
    </view>
    <view class="history">
      <history></history>
    </view>
  </view>
</template>

<script>
export default {
  components: {
    baseBox: () => import("./components/base_box.vue"),
    history: () => import("./components/history.vue"),
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
.my {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.my .base-box {
  width: 100%;
  height: 300rpx;
  background: pink;
}

.my .history {
  width: 100%;
  height: 160rpx;
  background: yellow;
}
</style>
