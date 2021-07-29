<template>
	<view class="city-search">
		<view class="city">
			沈阳
		</view>
		<view class="search">
			输入框
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	.city-search {
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content:space-around;
		width: 100%;
		height: 100%;
	}
	.city-search .city{
		width: 120rpx;
		height: 100%;
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content:center;
		background-color: #18B566;
	}
	.city-search .search{
		flex: 1;
		background: yellow;
	}

</style>