<template>
  <view class="list">
    <uni-list>
      <uni-list-item
        :border="!waterfall"
        class="uni-list-item--waterfall"
        title="自定义商品列表"
        v-for="item in lists"
        :key="item._id"
      >
        <template v-slot:header>
          <view
            class="uni-thumb shop-picture"
            :class="{ 'shop-picture-column': waterfall }"
          >
            <image :src="item.goods_thumb" mode="aspectFill"></image>
          </view>
        </template>

        <view slot="body" class="shop">
          <view>
            <view class="uni-title">
              <text class="uni-ellipsis-2">{{ item.name }}</text>
            </view>
            <view>
              <text class="uni-tag hot-tag">{{ item.goods_tip }}</text>
              <text v-for="tag in item.tag" :key="tag" class="uni-tag">{{
                tag
              }}</text>
            </view>
          </view>
          <view>
            <view class="shop-price">
              <text>¥</text>
              <text class="shop-price-text">{{ item.goods_price }}</text>
              <text>.00</text>
            </view>
            <view class="uni-note"
              >{{ item.comment_count }}条评论 月销量
              {{ item.month_sell_count }}</view
            >
            <view class="uni-note ellipsis">
              <text class="uni-ellipsis-1">{{ item.shop_name }}</text>
              <text class="uni-link">进店 ></text>
            </view>
          </view>
        </view>
      </uni-list-item>
    </uni-list>
  </view>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      waterfall: true,
      lists: [
        {
          _id: 1,
          goods_thumb:
            "https://vkceyugu.cdn.bspapp.com/VKCEYUGU-dc-site/460d46d0-4fcc-11eb-8ff1-d5dcf8779628.png",
          name: "名称",
          goods_tip: "提示",
          tag: {
            code: 1,
          },
          goods_price: 100,
          comment_count: 10,
          month_sell_count: 20,
          shop_name: "李政",
        },
        {
          _id: 2,
          goods_thumb:
            "https://vkceyugu.cdn.bspapp.com/VKCEYUGU-dc-site/460d46d0-4fcc-11eb-8ff1-d5dcf8779628.png",
          name: "名称",
          goods_tip: "提示",
          tag: {
            code: 1,
          },
          goods_price: 100,
          comment_count: 10,
          month_sell_count: 20,
          shop_name: "李政",
        },
      ],
    };
  },
  onLoad() {},
  methods: {},
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
