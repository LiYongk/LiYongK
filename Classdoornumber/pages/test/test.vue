<template>
	<view class="content">
		<view class="cultural-bg" :style="{backgroundImage: 'url('+imgUrl+')'}">
			<!-- 标题 -->
			<view class="test-title">
				<text class="">测试通知</text>
			</view>
			<view class="main-person">
				<text class="person-name">
					发法撒旦
				</text>
			</view>
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
				imgUrl: '/static/background.jpg'
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
@import url("./test.css");
</style>
