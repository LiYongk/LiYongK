<template>
	<view class="content teacher">
		<!-- 教师风尚 -->
		<view class="fashion-image-box fl">
			<image src="../../static/4任课教师_照片.png" mode="scaleToFill" class="fashion"></image>
		</view>
		<swiper class="swiper" indicator-dots="true">
			<swiper-item>
				<view class="person-introduce-box fl" >
					<view class="person-introduce" @click="showTeacher(2); changeName(0)">
						<view class="">
							<image class="person-image" src="../../static/4任课教师_照片.png"></image>
						</view>
						<view class="introduce-text">
							<view class="name">李铮</view>
							<view class="teacher-introduce">老师 田齐深，大学本科，2018级教师 </view>
							<view class="moto">走进音乐殿堂，享受音乐符力量</view>
						</view>
					</view>
					<!-- 第二个人物 -->
					<view class="person-introduce two" @click="showTeacher(2); changeName(1)">
						<view class="">
							<image src="../../static/4任课教师_照片.png" class="person-image"></image>
						</view>
						<view class="introduce-text">
							<view class="name">海城电子</view>
							<view class="teacher-introduce">老师，曾获得优秀教师将</view>
							<view class="moto">大学本科</view>
						</view>
					</view>
					<!-- 人物介绍下面的盒子 -->
					<!-- 第一个人物 -->
					<view class="person-introduce" @click="showTeacher(2); changeName(2)">
						<view class="">
							<image class="person-image" src="../../static/4任课教师_照片.png"></image>
						</view>
						<view class="introduce-text">
							<view class="name">李凯</view>
							<view class="teacher-introduce">班主任 优秀教师</view>
							<view class="moto">李凯毕业于东本师范</view>
						</view>
					</view>
					<!-- 第二个人物 -->
					<view class="person-introduce" @click="showTeacher(2);changeName(3)">
						<view class="">
							<image class="person-image" src="../../static/4任课教师_照片.png"></image>
						</view>
						<view class="introduce-text">
							<view class="name">肖宝平</view>
							<view class="teacher-introduce">老师 优秀教师</view>
							<view class="moto">走进音乐殿堂</view>
						</view>
					</view>			
				</view>
			</swiper-item>
			<swiper-item>
				<view class="person-introduce-box fl" >
					<view class="person-introduce" @click="showTeacher(2);changeName(3)">
						<view class="">
							<image class="person-image" src="../../static/4任课教师_照片.png"></image>
						</view>
						<view class="introduce-text">
							<view class="name">李铮</view>
							<view class="teacher-introduce">老师</view>
							<view class="moto">走进音乐殿堂</view>
						</view>
					</view>
					<!-- 第二个人物 -->
					<view class="person-introduce two" @click="showTeacher(2);changeName(3)">
						<view class="">
							<image src="../../static/4任课教师_照片.png" class="person-image"></image>
						</view>
						<view class="introduce-text">
							<view class="name">李铮</view>
							<view class="teacher-introduce">老师</view>
							<view class="moto">走进音乐殿堂</view>
						</view>
					</view>
					<!-- 人物介绍下面的盒子 -->
					<!-- 第一个人物 -->
					<view class="person-introduce" @click="showTeacher(2);changeName(3)">
						<view class="">
							<image class="person-image" src="../../static/4任课教师_照片.png"></image>
						</view>
						<view class="introduce-text">
							<view class="name">李铮</view>
							<view class="teacher-introduce">老师</view>
							<view class="moto">走进音乐殿堂</view>
						</view>
					</view>
					<!-- 第二个人物 -->
					<view class="person-introduce" @click="showTeacher(2);changeName(3)">
						<view class="">
							<image class="person-image" src="../../static/4任课教师_照片.png"></image>
						</view>
						<view class="introduce-text">
							<view class="name">李铮</view>
							<view class="teacher-introduce">老师</view>
							<view class="moto">走进音乐殿堂</view>
						</view>
					</view>
				</view>
			</swiper-item>
		</swiper>
		<!-- 返回按钮 -->
		<view class="back" @click="backPage">x</view>
		<view class="person-introduce techerDetail" :class="{show:index==2}">
			<view class="techer-pictrue fl">
				<image src="../../static/4任课教师_照片.png" class="person-image"></image>
			</view>
			<view class="techerIntroduce fl m-l-5">
				<view class="introduce-text">
					<view class="name">{{techerName}}</view>
					<view class="teacher-introduce">老师</view>
					<view class="moto">走进音乐殿堂</view>
				</view>
			</view>
			<!-- 关闭弹框按钮 -->
			<view class="close-btn" @click="close(1)">x</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				show:false,
				techerName: '',
				index: 1
			}
		},
		methods: {
			backPage () {
				uni.navigateBack({
					delta: 1
				})
			},
			showTeacher (val) {
				this.$data.index = 2
			},
			close () {
				this.$data.index = 1
			},
			changeName (val) {
				if (val == 0) {
					this.techerName = '李铮'
				} else if (val == 1) {
					this.techerName = '海城电子'
				} else if (val == 2) {
					this.techerName = '李凯'
				} else if (val == 3) {
					this.techerName = '肖宝平'
				}
			}
		}
	}
</script>

<style>
@import url("../../common/common.css");
@import url("./techer.css");
.teacher-page {
	display: flex;
	direction: row;
}
.fashion-image-box {
	width: 150rpx;
	height: 50%;
}
.fashion {
	width: 150rpx;
	height: 180rpx;
}
.lizheng-image {
	width: 130rpx;
	height: 180rpx;
}

	
</style>
