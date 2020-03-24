<template>
	<view class="content">
		<!-- 无数据时显示 -->
		<!--<view class="vuecont">
			<view class="vueimg vuesize">
				放图片处
			</view>
			<view class="vuesize">
				暂无内容
			</view>
			<view class="vuesize1">
				请联系管理员更新
			</view>
		</view> -->
		<!-- 有数据时显示 -->
		<view class="kecheng">课程表</view>
		<view class="tables">
			<table border="1"  style="border-collapse:collapse;width: 400rpx;height: 100rpx;">
				<tr>
					<td>时间</td>
					<td>星期一</td>
					<td>星期二</td>
					<td>星期三</td>
					<td>星期四</td>
					<td>星期五</td>
					<td>星期六</td>
					<td>星期日</td>
				</tr>
				<tr>
					<td>8:00~9:00</td>
					<td>语文</td>
					<td>数学</td>
					<td>英语</td>
					<td>地理</td>
					<td>生物</td>
					<td>化学</td>
					<td>物理</td>
				</tr>
				<tr>
					<td>9:00~10:00</td>
					<td></td>
					<td></td>
					<td></td>
					<td></td>
					<td></td>
					<td></td>
					<td></td>
				</tr>
				<tr>
					<td>10:00~11:00</td>
					<td></td>
					<td></td>
					<td></td>
					<td></td>
					<td></td>
					<td></td>
					<td></td>
				</tr>
				<tr>
					<td>12:00~13:00</td>
					<td></td>
					<td></td>
					<td></td>
					<td></td>
					<td></td>
					<td></td>
					<td></td>
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
	
	@import './classcss.css';
	
	
	
</style>
