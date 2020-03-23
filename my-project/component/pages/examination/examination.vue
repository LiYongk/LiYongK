<template>
	<view class="content">
		<view class="examination" :style="{backgroundImage: 'url('+imgUrl+')'}">
			<view class="tip">
				<view class="test">暂无考试</view>
				<view class="close-btn" @click="closeT">确定</view>
			</view>
			 <!-- 返回按钮 -->
			 <view class="back" @click="back">
			 	<image class="back-image" src="../../../static/back.png"></image>
			 </view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				imgUrl: '/static/danyawenhua.jpg',
			}
		},
		methods: {
			closeT () {
				uni.navigateBack({
					delta:1
				})
			},
			back () {
				uni.navigateBack({
					delta:1
				})
			}
		}
	}
</script>

<style>
@import url("../../../common/common.css");
@import url("./examination.css");
</style>
