<template>
	<view class="content">
		<view class="rain">
			<!-- 头部 -->
			<view class="careful-title text-center">
				<view class="careful-title">
					<view class="careful-title-text">下雨高发季节</view>
					<view class="careful-time-text">
						<text class="m-r-5">洪水防范</text>
						<text class="m-r-5">2019-03-04</text>
						<text class="">12：22</text>
					</view>
				</view>
			</view>
			<!-- 中部 -->
			<view class="main-box" :style="{backgroundImage: 'url('+imgUrl+')'}">
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
				imgUrl: '/static/mingxing.jpg'
			}
		},
		methods: {
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
@import url("../careful/careful.css");
@import url("./rain.css");
</style>
