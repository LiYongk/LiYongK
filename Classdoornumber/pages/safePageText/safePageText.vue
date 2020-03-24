<template>
	<view class="content">
		<view class="fireSafe">
			<!-- 标题 -->
			<view class="fireSafe-title text-center">
				<view class="fireSafe-title-up">
					<text class="">遇火自救逃生技巧</text>
				</view>
				<view class="fireSafe-title-down">
					<text class="pd-r-10">119消防主题日</text>
					<text class="pd-r-5">2019-07-04</text>
					<text class="">14：05</text>
				</view>
			</view>
			<view class="savePage-text m-t-5 text-15">
				<view class="savePage-text-box">
					校园安全与每个师生息息相关校园安全与每个师生息息相关校园安全与每个师生息息相关校园安全与每个师生息息相关校园安全与每个师生息息相关
				</view>
				<view class="savePage-text-box">
					校园安全与每个师生息息相关
					校园安全与每个师生息息相关
					校园安全与每个师生息息相关
					校园安全与每个师生息息相关
				</view>
				<view class="savePage-text-box">
					校园安全与每个师生息息相关
					校园安全与每个师生息息相关
					校园安全与每个师生息息相关
					
				</view>
				<view class="savePage-text-box">
					校园安全与每个师生息息相关校园安全与每个师生息息相关校园安全与每个师生息息相关
				</view>
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
					delta: 1
				})
			}
		}
	}
</script>

<style>
@import url("../../common/common.css");
@import url("./safePageText.css");
</style>
