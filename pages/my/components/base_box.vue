<!--
 * @Author: your name
 * @Date: 2021-07-30 09:45:30
 * @LastEditTime: 2021-07-30 09:47:54
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \onmyway-uniapp\pages\my\components\base.vue
-->
<template>
  <view class="base-content"> 基本信息 </view>
</template>

<script>
export default {
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
.base-content {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-around;
  width: 100%;
  height: 100%;
}
</style>