<template>
	<view class="content">
		<view class="achievement text-center">
			<view class="achievement-center" :style="{backgroundImage: 'url('+imgUrl+')'}">
				<view class="achievement-main-box">
					<view class="achievement-title-text">
						语文
					</view>
					<view class="achievement-detail">
						暂无内容
					</view>
				</view>
			</view>
			<!-- 返回按钮 -->
			<view class="back achievement-back" @click="back">
				<image class="back-image" src="../../static/back.png"></image>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				imgUrl: '/static/cj.png'
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
@import url("../../common/common.css");
@import url("./achievement.css");
</style>
