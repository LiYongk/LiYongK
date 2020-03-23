<template>
	<view class="content">
		<view class="meeting" :style="{backgroundImage: 'url('+imgUrl+')'}">
			<view class="meeting-box">
				<text class="">
					会议签到
				</text>
			</view>
			<view class="sweep-code clear" @click="active(1)">
				<view class="sweep fl">
					<view>刷脸</view>
					<view class="underline" :class="{isShow:isIndex==1}"></view>
				</view>
				<view class="code fr" @click="active(2)">
					<view>扫码</view>
					<view class="underline" :class="{isShow:isIndex==2}"></view>
				</view>
			</view>
			<!-- 暂无会议 -->
			<view class="meeting-tip-box" :class="{show:index==num}">
				<view class="meeting-tip-title">暂无会议</view>
				<view class="meeting-tip-btn" @click="closeTip(1)">确定</view>
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
				index: '1',
				num: '0',
				isIndex: '1'
			}
		},
		methods: {
			closeTip (val) {
				console.log(1)
				this.num = val
				uni.navigateBack({
					delta:1
				})
			},
			back () {
				uni.navigateBack({
					delta:1
				})
			},
			active (val) {
				console.log(val)
			}
		}
	}
</script>

<style>
@import url("../../../common/common.css");
@import url("./meeting.css");
</style>
