<template>
	<view class="content">
		<view class="door-jin">
			<view class="door">
				<view class="door-title text-center">
					请刷卡开门
				</view>
				<!-- 门禁图 -->
				<view class="door-image-box text-center m-t-10">
					<image class="door-image" src="../../static/door.png"></image>
				</view>
			</view>
			<!-- 返回键 -->
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
			}
		}
	}
</script>

<style>
@import url("../../common/common.css");
@import url("./door.css");
</style>
