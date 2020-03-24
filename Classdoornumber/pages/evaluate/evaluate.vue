<template>
	<view class="content">
		<view class="evaluate text-center">
			<image src="../../static/email.png" class="evaluate-image"></image>
			<view class="emial-text-box">
				<text class="underline"></text>
				<text class="text-25">暂无内容</text>
				<text class="m-t-5 text-25">请联系管理员新</text>
			</view>
			<!-- 返回按钮 -->
			<view class="back" @click="back">
				<image class="back-image" src="../../static/back.png"></image>
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
			},
		}
	}
</script>

<style>
@import url("../../common/common.css");
@import url("./evaluate.css");
</style>
