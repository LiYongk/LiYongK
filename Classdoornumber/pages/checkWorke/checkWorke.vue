<template>
	<view class="content">
		<view class="checkWork text-center clear" :style="{backgroundImage: 'url('+imgUrl+')'}">
			<view class="check-box">
				<view class="check-left">
					<view class="check-title">
						<text class="pd-r-10">人脸考勤</text>
						<text class="check-time">12:11</text>
					</view>
					<view class="check-adress-box">
						<image class="adress-img" src="../../static/adress.png"></image>
						<view class="check-adress">一楼高一二班</view>
					</view>
					<view class="adress-img-box">
						<image src="../../static/school.png" class="scholl-img"></image>
					</view>
				</view>
				<view class="photo">
					<button type="primary" @click="startSoterAuthenticationFaceID">人脸扫码</button>
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
				imgUrl: '/static/wenh.jpg',
				src: ''
			}
		},
		methods: {
			back () {
				uni.navigateBack({
					delta: 1
				})
			},
			startSoterAuthenticationFaceID() {
				uni.startSoterAuthentication({
					requestAuthModes: ['facial'],
					challenge: '123456',
					authContent: '请用FaceID解锁',
					success(res) {
						console.log(res);
					},
					fail(err) {
						console.log(err);
					},
					complete(res) {
						console.log(res);
					}
				})
			}
		}
	}
</script>

<style>
@import url("../../common/common.css");
@import url("./checkWorke.css");
</style>
