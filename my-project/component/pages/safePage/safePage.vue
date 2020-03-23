<template>
	<view class="content">
		<view class="safePage"  :style="{backgroundImage: 'url('+imgUrl+')'}">
			<view class="safePage-menu">
				<view class="safePage-menu-box one" >
					<image src="../../../static/protectT.png"></image>
					<view class="">动态</view>
				</view>
				<view class="safePage-menu-box two" @click="jumpFireSafe">
					<image src="../../../static/protect.png"></image>
					<view>遭遇火灾自救逃生</view>
				</view>
				<view class="safePage-menu-box three" @click="jumpSafeCampus">
					<image src="../../../static/protect.png"></image>
					<view>校园安全</view>
				</view>
				<view class="safePage-menu-box fore" @click="jumpCareful">
					<image src="../../../static/child.jpg"></image>
					<view>中午休息时间注意安全</view>
				</view>
				<view class="safePage-menu-box five" @click="jumpRain">
					<image src="../../../static/protect.png"></image>
					<view>下雨高发季节</view>
				</view>
			</view>
			<!-- 返回按钮 -->
			<view class="back safePage-back" @click="back">
				<image class="back-image" src="../../../static/back.png"></image>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				imgUrl: '/static/wenh.jpg',
			}
		},
		methods: {
			// 跳转防火安全
			jumpFireSafe () {
				uni.navigateTo({
					url: '../fireSafe/fireSafe'
				})
			},
			// 跳转校园安全
			jumpSafeCampus () {
				uni.navigateTo({
					url: '../safePageText/safePageText'
				})
			},
			back () {
				uni.navigateBack({
					delta:1
				})
			},
			jumpCareful () {
				uni.navigateTo({
					url: '../careful/careful'
				})
			},
			jumpRain () {
				uni.navigateTo({
					url: '../rain/rain'
				})
			}
		}
	}
</script>

<style>
@import url("../../../common/common.css");
@import url("./safePage.css");
</style>
