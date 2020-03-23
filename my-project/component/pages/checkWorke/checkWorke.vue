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
						<image class="adress-img" src="../../../static/adress.png"></image>
						<view class="check-adress">一楼高一二班</view>
					</view>
					<view class="adress-img-box">
						<image src="../../../static/school.png" class="scholl-img"></image>
					</view>
				</view>
				<view class="photo">
					<camera device-position="font"  class="camera">
						<view class="primary-button">
							<button type="primary" @click="takePhto">拍照</button>
							<view class="">预览</view>
						</view>
						<image mode="widthFix" :src="src"></image>
					</camera>
				</view>
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
				imgUrl: '/static/wenh.jpg'
			}
		},
		methods: {
			back () {
				uni.navigateBack({
					delta: 1
				})
			},
			takePhto () {
				 const ctx = uni.createCameraContext();
				            ctx.takePhoto({
				                quality: 'high',
				                success: (res) => {
									console.log(res)
				                    this.src = res.tempImagePath
				                }
				            });
				        },
				        error(e) {
				            console.log(e.detail);
				        }
		}
	}
</script>

<style>
@import url("../../../common/common.css");
@import url("./checkWorke.css");
</style>
