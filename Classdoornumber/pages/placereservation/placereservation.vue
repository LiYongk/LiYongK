<template>
	<view class="content">
		<!-- 无数据时显示 -->
		<view class="vuecont">
			<view class="vueimg vuesize">
				放图片处
			</view>
			<view class="vuesize">
				暂无内容
			</view>
			<view class="vuesize1">
				请联系管理员更新
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
	@import url("./placereservationcss.css");
</style>
