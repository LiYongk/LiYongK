<template>
	<view class="content">
		<view class="weather-box" :style="{backgroundImage: 'url('+imgUrl+')'}">
			<!-- 左边的 -->
			<view class="fl weather-detail-box">
				<!-- 日期 -->
				<view class="weather-detail-top text-20">
					<view class="weather-detail-top">
						<text class="pd-r-25">周二</text>
						<text class="">2019</text>
					</view>
					<view>
						<text>八月初五</text>
					</view>
				</view>
				<!-- 天气 -->
				<view class="day-weather m-t-10">
					<text class="pd-r-5">周三</text>
					<text class="pd-r-20">中雨</text>
					<text class="">24~29°</text>
				</view>
				<view class="day-weather  two">
					<text class="pd-r-5">周四</text>
					<text class="pd-r-20">中雨</text>
					<text class="">24~29°</text>
				</view>
				<view class="day-weather ">
					<text class="pd-r-5">周五</text>
					<text class="pd-r-20">中雨</text>
					<text class="">24~29°</text>
				</view>
				<!-- 下边地点的天气 -->
				<view class="weather-bottom pd-l-5">
					<view class="guangz-weather text-20">广州</view>
					<view class="weather-temperature">
						<text class="pd-r-5">24-25°</text>
						<text>雷阵雨</text>
					</view>
					<view class="wind-direction">
						<text class="pd-r-5">东北风3-4级</text>
						<text>5.5-7.9m/s</text>
					</view>
				</view>
			</view>
			<!-- 右边的 -->
			<view class="fr weather-text">
				<text class="fl one-text">
					润物细无声
				</text>
				<text class="fl two-text">随风潜入夜</text>
			</view>
			<!-- 返回按钮 -->
			<view class="back" @click="back">
				<image class="back-image" src="../../static/back.png"></image>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				imgUrl: '/static/weather.jpg'
			}
		},
		methods: {
			back () {
				uni.navigateBack({
					delta:1
				})
			}
		}
	}
</script>

<style>
@import url("../../common/common.css");
@import url("./weather.css");
</style>
