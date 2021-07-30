<!--
 * @Author: your name
 * @Date: 2021-07-29 16:11:07
 * @LastEditTime: 2021-07-30 11:55:59
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \onmyway-uniapp\pages\coupon\components\new.vue
-->
<template>
  <view class="new-content">
    <u-image
      width="100%"
      height="100%"
      src="../../../static/new.jpg"
    ></u-image>
  </view>
</template>

<script>
export default {
  data() {
    return {
      src: "",
    };
  },
  onLoad() {},
  methods: {},
};
</script>
<style lang="scss" scoped>
.new-content {
  width: 97%;
  height: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  border-radius: 20px;
  overflow: hidden;
  margin: auto auto;
}
</style>
