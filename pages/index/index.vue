<template>
	<view class="content">
		<u-row gutter="16" justify="space-between">
			<u-col :span="11"><u-search placeholder="搜索物品" v-model="keyword" :show-action="false"></u-search></u-col>
			<u-col :span="1"><u-icon name="scan" size="46"></u-icon></u-col>
		</u-row>
		<u-row gutter="16">
			<u-col :span="6">
				<view class="showCard">
					<u-icon name="clock" color="#2979ff" size="44"></u-icon>
					<text class="title">临期</text>
					<u-count-to :start-val="0" :end-val="l_endVal" font-size="35"></u-count-to>
				</view>
			</u-col>
			<u-col :span="6">
				<view class="showCard">
					<u-icon name="bell" color="#f29100" size="44"></u-icon>
					<text class="title">过期</text>
					<u-count-to :start-val="0" :end-val="g_endVal" font-size="35"></u-count-to>
				</view>
			</u-col>
		</u-row>
	</view>
</template>

<script>
export default {
	data() {
		return {
			keyword: '',
			l_endVal: 3,
			g_endVal: 4,
			list: [
				{
					text: '点赞',
					color: 'blue',
					fontSize: 28
				},
				{
					text: '分享'
				},
				{
					text: '评论'
				}
			],
			show: true
		};
	},
	onLoad() {},
	methods: {}
};
</script>

<style>
.content {
	display: flex;
	flex-direction: column;
	padding: 20rpx;
}
.u-row {
	margin: 30rpx 0;
}

.showCard {
	height: 120rpx;
	border-radius: 4px;
	transition: 0.5s;
	color: #fff;
	box-shadow: 0px 5px 25px rgba(65, 84, 241, 0.3);
	display: flex;
	flex-direction: row;
	align-items: center;
	padding: 20rpx;
}
.title {
	color: #303133;
	margin: 0 50rpx 0 5rpx;
	font-size: larger;
}
</style>
