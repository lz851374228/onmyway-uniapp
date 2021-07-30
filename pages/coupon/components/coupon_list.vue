<!--
 * @Author: your name
 * @Date: 2021-07-29 16:11:13
 * @LastEditTime: 2021-07-30 17:28:30
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \onmyway-uniapp\pages\coupon\components\coupon_list.vue
-->
<template>
  <view class="coupon-content">
    <view class="filter">
      <u-dropdown
        class="u-dropdown"
        ref="uDropdown"
        @open="open"
        @close="close"
      >
        <u-dropdown-item
          v-model="value1"
          title="类型"
          :options="options1"
          @change="change"
        ></u-dropdown-item>
        <u-dropdown-item
          v-model="value1"
          title="距离"
          :options="options1"
          @change="change"
        ></u-dropdown-item>
        <u-dropdown-item
          v-model="value2"
          title="数量"
          :options="options2"
        ></u-dropdown-item>
      </u-dropdown>
    </view>
    <view class="list">
      <view class="item" v-for="item in list" :key="item.id">
        <view class="left">
          <view>
            <text>￥</text>
            <text class="money">{{ item.money }}</text>
          </view>
          <view class="require">{{ item.require }}</view>
        </view>
        <view class="center">
          <view class="shop">
            <text class="name">{{ item.shopName }}</text>
            <text class="address">{{ item.shopAddress }}</text>
          </view>
          <view class="name"> {{ item.name }} </view>
          <view class="time">
            <text>有效期至：</text>
            <text>{{ item.time }}</text>
          </view>
        </view>
        <view class="right">
          <view class="number">
            <text>剩余：</text>
            <text class="num">{{ item.number }}</text>
            <text>张</text>
          </view>
          <view class="btn">
            <u-button
              type="error"
              shape="circle"
              :ripple="true"
              ripple-bg-color="#909399"
              >抢</u-button
            >
          </view>
        </view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      value1: 1,
      value2: 2,
      options1: [
        {
          label: "默认排序",
          value: 1,
        },
        {
          label: "距离优先",
          value: 2,
        },
      ],
      options2: [
        {
          label: "去冰",
          value: 1,
        },
        {
          label: "加冰",
          value: 2,
        },
      ],
      list: [
        {
          id: 111,
          money: 20.0,
          require: "满200使用",
          shopName: "川味菜馆",
          shopAddress: "据您200米",
          name: "美食优惠券",
          time: "2021.08.31",
          number: 31,
        },
        {
          id: 222,
          money: 100,
          require: "满699使用",
          shopName: "徐福记",
          shopAddress: "据您210米",
          name: "美食优惠券",
          time: "2021.08.31",
          number: 45,
        },
      ],
    };
  },
  onLoad() {},
  methods: {
    open(index) {
      // 展开某个下来菜单时，先关闭原来的其他菜单的高亮
      // 同时内部会自动给当前展开项进行高亮
      this.$refs.uDropdown.highlight();
    },
    close(index) {
      // 关闭的时候，给当前项加上高亮
      // 当然，您也可以通过监听dropdown-item的@change事件进行处理
      this.$refs.uDropdown.highlight(index);
    },
    change() {
      // 更多的细节，如有需要请自行根据业务逻辑进行处理
      // this.$refs.uDropdown.highlight(xxx);
    },
  },
  /**
   * 下拉刷新回调函数
   */
  onPullDownRefresh() {},
  /**
   * 上拉加载回调函数
   */
  onReachBottom() {},
};
</script>
<style lang="scss" scoped>
.coupon-content {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.filter {
  width: 95%;
  margin: 10rpx 20rpx 0rpx;
  background: #B8F0FF;
  border-radius: 20rpx;
}
.list {
  width: 100%;
  .item {
    $bgColor:rgb(217, 93, 121);
    height: 190rpx;
    margin: 20rpx 20rpx;
    background: rgba($color: #000000, $alpha: 0);
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    .left {
      width: 30%;
      height: 100%;
      color: white;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: space-around;
      position: relative;
      background-image: radial-gradient(
        circle at 1px 8px,
        transparent 6px,
        $bgColor 6px,
        $bgColor 0px
      );
      background-size: 500px 18px;
      background-position: 0 0, 500px 0;
      background-repeat-x: no-repeat;

      .money {
        font-size: 70rpx;
      }
      .require {
        margin-top: -50rpx;
        font-size: 16rpx;
      }
    }
    .center {
      flex: 1;
      height: 100%;
      font-size: 20rpx;
      color: white;
      background: $bgColor;
      display: flex;
      flex-direction: column;
      justify-content: space-around;
      .shop {
        .name {
          font-size: 20rpx;
          margin-right: 30rpx;
        }
        .address {
          font-size: 16rpx;
        }
      }
      .name {
        font-size: 50rpx;
        text-align: center;
      }
      .time {
        text-align: center;
      }
    }
    .right {
      width: 25%;
      height: 100%;
      border-top-right-radius: 20rpx;
      border-end-end-radius: 20rpx;
      border-left: 1px dotted #eee;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      position: relative;
      background-image: radial-gradient(
        circle at 100% 8px,
        transparent 6px,
        $bgColor 6px,
        $bgColor 0px
      );
      background-size: 200px 18px;
      background-position: 0 0, 500px 0;
      background-repeat-x: no-repeat;

      .number {
        color: white;
        font-size: 16rpx;
        .num {
          font-size: 30rpx;
        }
      }
      .btn {
        margin-top: 20rpx;
        font-size: 36rpx;
      }
    }
  }
}
</style>

