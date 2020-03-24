<template>
	<view class="content">
		<view class="messge-box" :style="{backgroundImage: 'url('+imgUrl+')'}">
			<image src="../../static/4任课教师_照片.png" class="fl fashion-image"></image>
			<view class="fl slogan" @click="showEla(1)">
				<view class="surname text-15">姜</view>
				<view class="surname-text-box">
					<text class="techer-name">姜笑老师</text>
					<text class="teacher-class">你好高一二班</text>
				</view>
			</view>
			<!-- 隐藏框 -->
			<view class="elastic" :class="{isActive:index==num}" >
				<view class="close-btn" @click="removeActive(2)">
					x
				</view>
				<view class="surname text-15 show fl">姜</view>
				<view class="surname-text-box one pd-l-15">
					<view class="">
						姜笑老师
					</view>
					<view class="v-time">
						<text class="pd-r-10">04-24</text>
						<text class="">15:35</text>
					</view>
				</view>
				<view class="hello-teacher">
					你好高一二班
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
				imgUrl: '/static/cu.jpg',
				num: '0',
				index: '1'
			}
		},
		methods: {
			back () {
				uni.navigateBack({
					delta:1
				})
			},
			showEla (val) {
				console.log(val)
				this.num = val
			},
			removeActive (number) {
				this.num = number
			}
		}
	}
</script>

<style>
@import url("../../common/common.css");
@import url("./message.css");
</style>
