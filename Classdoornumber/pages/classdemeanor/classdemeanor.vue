<template>
	<view>
	      <view class="classdemeanor-border">
	      	<view class="classdemeanor-font">祝大家国庆节快乐！</view>
	      </view>
		  <view class="error" @tap="error">
		  	<image class="error-img" src="../../static/errorimg.png"></image>
		  </view>
	</view>
</template>

<script>
	 export default {
	     data() {
	         return {}
	     },
	     methods: {
	        error:function(){
	        	uni.redirectTo({
	        		url:'../index/index'
	        	})
	        }
	     }
	 }
</script>

<style>
	@import url("./classdemeanorcss.css");
</style>
