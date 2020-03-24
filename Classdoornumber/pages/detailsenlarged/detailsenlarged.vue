<template>
	<view>
		<view class="body">
			<view class="img-box">
				<image class="img-style" src="../../static/546596e605166.jpg" mode="widthFix"></image>
			</view>
			<view class="inter-head div-filter">
				<view class="item-classname font-color-size">
					高二2班
				</view>
				<view class="class-information font-color-size1">
					这是一个五星的班级
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
					url:'../learnmore/learnmore'
				})
			}
		},
	}
</script>

<style>
	@import url("./detailsenlargedcss.css");
</style>
