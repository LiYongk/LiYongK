<template>
	<view>
		<view class="bullet-left">
			<view class="b-font">布告栏</view>
		</view>
		<view class="b-content">
			
			<view class="b-content-h" @tap="bulletin">
				<view class="b-content-img">
					<image class="b-content-images" src="../../static/img/timg.jpg"></image>
				</view>
				<view class="b-title-font">互问互答</view>
				<view class="b-content-doc font-style">
					互问互答测试
				</view>
			</view>
			
			<view class="b-content-h">
				<view class="b-content-img">
					<image class="b-content-images" src="../../static/img/timg.jpg"></image>
				</view>
				<view class="b-title-font">互问互答</view>
				<view class="b-content-doc font-style">
					先知互问互答测试232-23
				</view>
			</view>
			
			<view class="b-content-h">
				<view class="b-content-img">
					<image class="b-content-images" src="../../static/img/timg.jpg"></image>
				</view>
				<view class="b-title-font">诚意推荐</view>
				<view class="b-content-doc font-style">
					欧IT人家说带你飞看见对方会给对方过来看是否更多
				</view>
			</view>
			
			<view class="b-content-h">
				<view class="b-content-img">
					<image class="b-content-images" src="../../static/img/timg.jpg"></image>
				</view>
				<view class="b-title-font">寻物启事</view>
				<view class="b-content-doc font-style">
					本人在学校操场丢失一张学生证
				</view>
			</view>
			
		</view>
	
		<view class="error" @tap="error">
			<image class="error-img" src="../../static/errorimg.png"></image>
		</view>
	</view>
</template>

<script>
	export default{
		data:{
			return:{}
		},
		methods: {
			
			error:function(){
				uni.redirectTo({
					url:'../index/index'
				})
			},
			bulletin:function(){
				uni.redirectTo({
					url:'../bulletinboard/bulletinboardsonpage'
				})
			}
		},
	}
</script>

<style>
	@import url("./bulletinboardcss.css");
</style>
