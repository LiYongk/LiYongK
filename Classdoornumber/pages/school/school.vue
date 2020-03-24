<template>
	<view>
		<view class="school-outermost">
			<view class="school-img">
				<image class="images" src="../../static/img/4任课教师_照片.png"></image>
			</view>
			<view class="school-name">先知中学</view>
			<view class="tran"></view>
			<view class="tran1">学校测试数据</view>
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
	@import url("./schoolcss.css");
</style>
