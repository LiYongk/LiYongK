<template>
	<view class="content">
		<view class="about" :style="{backgroundImage: 'url('+imgUrl+')'}">
			<!-- 顶部栏框 -->
			<view class="cloud-big-box">
				<!-- 左侧栏框 -->
				<view class="cloud-box transparent-bg">
					<image class="cloud-image" src="../../static/cloud.png"></image>
				</view>
				<!-- 右侧栏框 邮箱登录 -->
				<view class="transparent-bg email-box">
					<!-- 标题按钮 -->
					<view class="title-btn-box clear">
						<!-- 刷脸按钮 -->
						<view class="face-btn fl" @click="changeMethoed(1)">
							<text class="">
								刷脸
							</text>
							<view class="underline" :class="{show:num==1}"></view>
						</view>
						<!-- 账号按钮 -->
						<view class="account-btn fl" @click="changeMethoed(2)">
							<text class="">
								账号按钮
							</text>
							<view class="underline" :class="{show:num==2}"></view>
						</view>
					</view>
					<!-- 账号登录框 -->
					<view class="account-box" :class="{show:num==2}">
						<!-- 输入框 -->
						<view class="input-box-account clear">
							<!-- 账号 -->
							 <view class="account-input-box clear">
								 <image src="../../static/account.png" class="account-image fl"></image>
								 <input type="text" placeholder="账号" class="account-input fl"/>
							 </view>
							 <!-- 密码 -->
							 <view class="account-input-box  two clear">
								 <image src="../../static/password.png" class="account-image fl"></image>
								 <input type="text" placeholder="密码" class="account-input fl"/>
							 </view>
						</view>
						<!-- 按钮 -->
						<view class="sign-btn">登录</view>
						<view class="sign-tip">使用账号登录</view>
					</view>
					<!-- 刷脸框 -->
					<view class="face-swiping-box" :class="{show:num==1}">
						<camera device-position="back" flash="off" @error="error" style="width: 100%; height: 80rpx;"></camera>
						<button type="primary" @click="takePhoto">拍照</button>
						<view class="text-center">预览</view>
						<image mode="widthFix" :src="src"></image>
					</view>
				</view>
			</view>
			<!-- 底部栏 -->
			<view class="cloud-big-box m-t-10">
				<!-- 左侧栏 -->
				<view class="device-information  transparent-bg">
					<view class="device-information-box">
						<view class="information-title m-t-5">设备信息</view>
						<view class="clear m-t-10">
							<view class="fl">编号</view>
							<view class="fr">AS-GP8CFCA011F254</view>
						</view>
						<view class="clear m-t-10">
							<view class="fl information-adress">场所</view>
							<view class="fr">高一2班(一楼高一2班)</view>
						</view>
						<!-- 日期 -->
						<view class="time fr m-t-10">1.29</view>
					</view>
				</view>
				<!-- 右侧栏 -->
				<view class="system-function transparent-bg">
					<!-- wifi栏 -->
					<view class="wifi-img-box" @click="open(3); changeValue(0)">
						<image src="../../static/WIFIImg.png" class="wifi-img"></image>
						<view class="check-text">检查网络</view>
					</view>
					<view class="wifi-img-box" @click="open(3); changeValue(1)">
						<image src="../../static/upload.png" class="wifi-img"></image>
						<view class="check-text">检查更新</view>
					</view>
					<view class="wifi-img-box three" @click="open(3); changeValue(2)">
						<image src="../../static/rizhi.png" class="wifi-img"></image>
						<view class="check-text">上传日志</view>
					</view>
					<view class="wifi-img-box five" @click="open(3); changeValue(3)">
						<image src="../../static/shezhi.png" class="wifi-img"></image>
						<view class="check-text">系统设置</view>
					</view>
					<view class="wifi-img-box five" @click="open(3); changeValue(4)">
						<image src="../../static/zhiwen.png" class="wifi-img"></image>
						<view class="check-text">指纹录入</view>
					</view>
				</view>
			</view>
			<!-- 小弹框 -->
			<view class="tip-box" :class="{isShow:index==isNum}">
				<view class="tip-title">{{dataText}}</view>
				<view class="tip-btn" @click="close(1)">确定</view>
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
				imgUrl: '/static/bule.jpg',
				num: 2,
				index: 1,
				isNum: 3,
				dataText: '',
				src: ''
			}
		},
		methods: {
			takePhoto() {
				const ctx = uni.createCameraContext();
				ctx.takePhoto({
					quality: 'high',
					success: (res) => {
						this.src = res.tempImagePath
					}
				});
			},
			
			changeMethoed (val) {
				this.num = val
			},
			back () {
				uni.navigateBack({
					delta:1
				})
			},
			close (val) {
				this.index = val
			},
			open (value) {
				this.index = value
			},
			changeValue (value) {
				if (value == 0) {
					this.dataText = '网络正常'
				} else if (value == 1) {
					this.dataText = '暂无更新'
				} else if (value == 2) {
					this.dataText = '上传日志'
				} else if (value == 3) {
					this.dataText = '请登录'
				} else if (value == 4) {
					this.dataText == '请登录'
				} else {
					this.dataText = '请登录'
				}
			}
		}
	}
</script>

<style>
@import url("../../common/common.css");
@import url("./about.css");
</style>
