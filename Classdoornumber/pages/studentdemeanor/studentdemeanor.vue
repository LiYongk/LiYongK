<template>
	<view>
		<view class="bullet-left">
			<view class="b-font">学生风采</view>
		</view>
		<view class="b-content">
			<view class="b-content-h" @tap="modaltap">
				<view class="b-content-img">
					<image class="b-content-images" src="../../static/img/timg.jpg"></image>
				</view>
				<view class="b-title-font">李萌</view>
				<view class="b-content-doc1 font-style1">
					优秀奖
				</view>
				<view class="b-content-doc font-style">
					李萌同学在广州杯第一届儿歌比赛中获得优秀奖
				</view>
			</view>
		</view>
		<view class="error" @tap="error">
			<image class="error-img" src="../../static/errorimg.png"></image>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				// title: 'modal',
				// modalHidden: true,
				// modalHidden2: true
			}
		},
		methods: {
			modaltap: function (e) {
				uni.showModal({
					title: '李萌',
					content: "李萌同学在广州杯第一届儿歌比赛中获得优秀奖",
					showCancel: false,
					confirmText: "确定"
				})
			},
			error:function(){
				uni.redirectTo({
					url:'../index/index'
				})
			}
		}
	}
</script>

<style>
	@import url("./studentdemeanorcss.css");
</style>
	