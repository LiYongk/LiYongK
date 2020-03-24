<template>
	<view>
	<view class="content">
		<view class="tilte">
			关于国庆节放假的通知
		</view>
		<view class="content1">
				国庆节放假时间为9月30日-10月15日，15日下午4:30左右返校
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
			}
		},
	}
</script>

<style>
	@import './noticecss.css';
</style>
