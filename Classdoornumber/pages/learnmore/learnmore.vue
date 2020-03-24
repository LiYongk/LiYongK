<template>
	<view>
		<view class="outer-frame" @tap="xiangqin">
			<view class="picture-box">
				<image class="image" src="../../static/546596e605166.jpg"></image>
			</view>
			<view class="font-box">
				<view class="font-style">
					高三2班
				</view>
			</view>
		</view>
		
		<view class="outer-frame">
			<view class="picture-box">
				<image class="image" src="../../static/img/timg1.jpg"></image>
			</view>
			<view class="font-box">
				<view class="font-style">
					高二2班
				</view>
			</view>
		</view>
		
		<view class="outer-frame">
			<view class="picture-box">
				<image class="image" src="../../static/img/5班级风采_照片.png"></image>
			</view>
			<view class="font-box">
				<view class="font-style">
					高三一2班
				</view>
			</view>
		</view>
		
		<view class="outer-frame">
			<view class="picture-box">
				<image class="image" src="../../static/img/timg.jpg"></image>
			</view>
			<view class="font-box">
				<view class="font-style">
					高三5班
				</view>
			</view>
		</view>
		
		<view class="outer-frame">
			<view class="picture-box">
				<image class="image" src="../../static/img/timg.jpg"></image>
			</view>
			<view class="font-box">
				<view class="font-style">
					高三5班
				</view>
			</view>
		</view>
		
		<view class="outer-frame">
			<view class="picture-box">
				<image class="image" src="../../static/img/timg.jpg"></image>
			</view>
			<view class="font-box">
				<view class="font-style">
					高三5班
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
		data(){
			return{
				
				}
			},
			methods:{
				error:function(){
					uni.redirectTo({
						url:'../interclass/interclass'
					})
				},
				xiangqin:function(){
					uni.navigateTo({
						url:'../detailsenlarged/detailsenlarged'
					})
				}
			}
	}
</script>

<style>
	@import url("./learnmorecss.css");
</style>
