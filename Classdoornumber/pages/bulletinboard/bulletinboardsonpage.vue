<template>
	<view class="content">
		<view class="tilte-top tilte-top-font">
			失物招领
		</view>
		<view class="finn">
			<view class="content-border">
				<view class="content-font-white">
					姚
				</view>
				<view class="name-font name-font1">
					姚老师
				</view>
				<view class="tiem-font-style time-font">
					05-04&nbsp;&nbsp;14:23
				</view>
			</view>
		</view>
		<view class="finns time-font">
			哪位同学遗失了一串钥匙，上面带着一个粉色的小布偶，请及时到教务处找姚老师认领
			2020-3-18
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
				uni.navigateTo({
					url:'../bulletinboard/bulletinboard'
				})({
					url:'../index/index'
				})
			}
		},
	}
</script>

<style>
	@import url("./bulletinboardsonpagecss.css");
</style>
