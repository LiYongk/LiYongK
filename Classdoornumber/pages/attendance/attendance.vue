<template>
	<view>
		<view class="rating-left">
			<view class="rating-left-in rating-left-in-font">
				1
			</view>
			<view class="rating-left-bottom rating-left-bottom-font">
				考勤
			</view>
		</view>
		<view class="rating-right">
			<table  border="1" class="rating-table">
				<tr class="rating-table-font-top">
					<td>名称</td>
					<td>总出勤</td>
					<td>异常</td>
					<td>迟到</td>
					<td>未打卡</td>
					<td>缺勤</td>
					<td>无故缺勤</td>
					<td>请假</td>
				</tr>
				<tr class="rating-table-font-tcontent">
					<td>高一1班</td>
					<td>9</td>
					<td>0</td>
					<td>0</td>
					<td>0</td>
					<td>0</td>
					<td>0</td>
					<td>0</td>
				</tr>
				<tr class="rating-table-font-tcontent">
					<td>高一2班</td>
					<td>7</td>
					<td>0</td>
					<td>0</td>
					<td>0</td>
					<td>0</td>
					<td>0</td>
					<td>0</td>
				</tr>
				<tr class="rating-table-font-tcontent">
					<td>高二1班</td>
					<td>8</td>
					<td>0</td>
					<td>0</td>
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
	@import url("./attendancecss.css");
</style>
