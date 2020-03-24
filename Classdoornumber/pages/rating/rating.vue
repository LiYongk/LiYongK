<template>
	<view>
		<view class="rating-left">
			<view class="rating-left-in rating-left-in-font">
				1
			</view>
			<view class="rating-left-bottom rating-left-bottom-font">
				总分年级排名
			</view>
		</view>
		<view class="rating-right">
			<table  border="1" class="rating-table">
				<tr class="rating-table-font-top">
					<td>评比项目</td>
					<td>08-22</td>
					<td>08-23</td>
					<td>08-24</td>
					<td>本周</td>
					<td>上月</td>
				</tr>
				<tr class="rating-table-font-tcontent">
					<td>总分</td>
					<td>0/第一名</td>
					<td>0</td>
					<td>0</td>
					<td>0</td>
					<td>0</td>
				</tr>
				<tr class="rating-table-font-tcontent">
					<td>朗诵</td>
					<td>0/第二名</td>
					<td>0</td>
					<td>0</td>
					<td>0</td>
					<td>0</td>
				</tr>
				<tr class="rating-table-font-tcontent">
					<td>唱歌</td>
					<td>0/第三名</td>
					<td>0</td>
					<td>0</td>
					<td>0</td>
					<td>0</td>
				</tr>
			</table>
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
	@import url("./ratingcss.css");
</style>
