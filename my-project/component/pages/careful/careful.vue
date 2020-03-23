<template>
	<view class="content">
		<view class="careful">
			<view class="careful-title text-center">
				<view class="careful-title">
					<view class="careful-title-text">中午休息时间注意安全</view>
					<view class="careful-time-text">
						<text class="m-r-5">课间安全</text>
						<text class="m-r-5">2019-03-04</text>
						<text class="">12：22</text>
					</view>
				</view>
			</view>
			<view class="careful-main-text">
				<text>中午休息不要随意出门</text>
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
@import url("./careful.css");
</style>
