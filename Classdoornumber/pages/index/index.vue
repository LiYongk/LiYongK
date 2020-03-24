<template>
	<view class="content" >

		<!-- 班级	时间 天气 -->
		<view class="navbar">
				<!-- 左 -->
				<view class="navbar1 cfont">
					高一(2)班
				</view>
				<view class="navbar1 cfont1" @tap="monthlyassessment()">
						月评价
						<view class="cimgs">
							<image src="../../static/img/1班级信息评价.png"  class="image"></image>
						</view>
						<view class="cimgs">
							<image src="../../static/img/1班级信息评价.png"  class="image"></image>
						</view>
						<view class="cimgs">
							<image src="../../static/img/1班级信息评价.png"  class="image"></image>
						</view>
				</view>
			
				<!-- 右 -->
				<view class="navbar2 cfont2">
					2020/3/13
				</view>
				<view class="navbar3 cfont3" @click="jumpWeather()">
					<view class="cimgs1">
						<image class="cimgs1" src="../../static/img/1班级信息_天气.png"></image>
					</view>
					多云，22℃
				</view>
		</view>
		
		<!-- 班主任介绍 -->
		<view class="middle">
			<view class="viewbar"></view>
			<view class="name cfont5">
				李萌
			</view>
			<view class="type cfont6">
				专业:&nbsp;语文<span style='margin-left: 10rpx;'>教龄:&nbsp;3年</span>
			</view>
			<view class="phone">
				<view class="phone1"></view>
				<view class="cfont7">1238794894982</view>
			</view>
			
			<!-- 图片 -->
			<view>
				<image class="viewright" src="../../static/img/2班主任介绍_照片.png"></image>
			</view>
			<!-- 查看班主任简介 -->
			<view @tap="gengduo">
				<image class="viewright1" src="../../static/img/2班主任介绍_更多.png"></image>
			</view>
		</view>
		
		<!-- 通知-->
		<view class="vright" @tap="notice">
			<view class="vtong"></view>
			<swiper class="swiper" :circular="true" :disable-touch="true" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
			    <swiper-item>
			      <view class="vtong1 cfont8">
			      	关于中秋节放假的通知
			      </view>
			      <view class="vtong2 cfont9">
			      	中秋节放假时间为9月13日-9月15日，15日下午4:30左右返校
			      </view>
			    </swiper-item>
			    <swiper-item>
			       <view class="vtong1 cfont8">
			       	关于国庆节放假的通知
			       </view>
			       <view class="vtong2 cfont9">
			       	国庆节放假时间为9月30日-10月15日，15日下午4:30左右返校
			       </view>
			    </swiper-item>
			    <swiper-item>
			       <view class="vtong1 cfont8">
			       	关于中秋节放假的通知
			       </view>
			       <view class="vtong2 cfont9">
			       	中秋节放假时间为9月13日-9月15日，15日下午4:30左右返校
			       </view>
			    </swiper-item>
			</swiper>
		</view>
		
		<!-- 班级宣传 -->
		<view class="Propaganda">
			<view class="Propaganda1">
			
			</view>
			<view class="vban bfont5">班训
				<view class="bfont">
					求实创新，自信自律
				</view>
			</view>
			<view class="vban1 bfont5">班风
				<view class="bfont">
					挥东激情，挑战自我，突破极限，超越自我
				</view>
			</view>
			<view class="vban2 bfont5">寄语
				<view class="bfont">
					做人以德，德高人敬；学习靠勤，勤能取胜
				</view>
			</view>
		</view>
		
		<!-- 任课教师 -->
		<view class="teacher" @click="jumpTheACher()">
			<view class="tviewbar"></view>
			<swiper class="demeanor4" :circular="true" :disable-touch="true" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
			    <swiper-item>
			      <view class="name cfont5">
			      	苏林
			      </view>
			      <view class="type cfont6">
			      	专业:&nbsp;语文<span style='margin-left: 10rpx;'>教龄:&nbsp;2年</span>
			      </view>
			      <view class="phone">
			      	<view class="phone1"></view>
			      	<view class="cfont7">1238794894982</view>
			      </view>
			      <!-- 图片 -->
			      <view>
			      	<image class="tviewright" src="../../static/img/4任课教师_照片.png"></image>
			      </view>
			    </swiper-item>
			    <swiper-item>
			        <view class="name cfont5">
			        	李征
			        </view>
			        <view class="type cfont6">
			        	专业:&nbsp;语文<span style='margin-left: 10rpx;'>教龄:&nbsp;2年</span>
			        </view>
			        <view class="phone">
			        	<view class="phone1"></view>
			        	<view class="cfont7">1238794894982</view>
			        </view>
			        <!-- 图片 -->
			        <view>
			        	<image class="tviewright" src="../../static/img/4任课教师_照片.png"></image>
			        </view>
			    </swiper-item>
			    <swiper-item>
			       <view class="name cfont5">
			       	李凯
			       </view>
			       <view class="type cfont6">
			       	专业:&nbsp;语文<span style='margin-left: 10rpx;'>教龄:&nbsp;2年</span>
			       </view>
			       <view class="phone">
			       	<view class="phone1"></view>
			       	<view class="cfont7">1238794894982</view>
			       </view>
			       <!-- 图片 -->
			       <view>
			       	<image class="tviewright" src="../../static/img/4任课教师_照片.png"></image>
			       </view>
			    </swiper-item>
			</swiper>
		</view>
		
		<!-- 精彩视频 -->
		<view class="Classvideo">
			<view class="video1"></view>
			<!-- <view>
				<image class="video2" src="../../static/img/5班级风采_照片.png"></image>
			</view> -->
				<video class="video2"  src="https://img.cdn.aliyun.dcloud.net.cn/guide/uniapp/%E7%AC%AC1%E8%AE%B2%EF%BC%88uni-app%E4%BA%A7%E5%93%81%E4%BB%8B%E7%BB%8D%EF%BC%89-%20DCloud%E5%AE%98%E6%96%B9%E8%A7%86%E9%A2%91%E6%95%99%E7%A8%8B@20181126.mp4"
				@error="videoErrorCallback" :danmu-list="danmuList" enable-danmu danmu-btn controls></video>
		</view>
		
		<!-- 班级风采 -->
		<view class="Classdemeanor" @tap="classdemeanor">
			<view class="demeanor1"></view>
			<view class="demeanor2">
				<swiper class="demeanor3" :circular="true" :disable-touch="true" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
				    <swiper-item>
				       <image class="demeanor3" src="../../static/img/5班级风采_照片.png"></image>
				    </swiper-item>
				    <swiper-item>
				        <image class="demeanor3" src="../../static/img/timg.jpg"></image>
				    </swiper-item>
				    <swiper-item>
				        <image class="demeanor3" src="../../static/img/timg1.jpg"></image>
				    </swiper-item>
				</swiper>
			</view>
		</view>
		
		<!-- 课程安排 -->
		<view class="curriculum" @tap="classcard">
			<view class="curr1"></view>
			<view class="currlum">
				<view class="curriculum1 colr">第一节</view>
				<view class="curriculum1 colr1">(08:00~09:00)</view>
				<view class="curriculum2 colr2">语文</view>
			</view>
			<view class="currlum1">
				<view class="curriculum1 colr">第二节</view>
				<view class="curriculum1 colr1">(08:00~09:00)</view>
				<view class="curriculum2 colr2">数学</view>
			</view>
			<view class="currlum1">
				<view class="curriculum1 colr">第三节</view>
				<view class="curriculum1 colr1">(08:00~09:00)</view>
				<view class="curriculum2 colr2">英语</view>
			</view>
			<view class="currlum1">
				<view class="curriculum1 colr">第四节</view>
				<view class="curriculum1 colr1">(08:00~09:00)</view>
				<view class="curriculum2 colr2">地理</view>
			</view>
			<view class="currlum1">
				<view class="curriculum1 colr">第五节</view>
				<view class="curriculum1 colr1">(08:00~09:00)</view>
				<view class="curriculum2 colr2">历史</view>
			</view>
			<view class="currlum1">
				<view class="curriculum1 colr">第六节</view>
				<view class="curriculum1 colr1">(08:00~09:00)</view>
				<view class="curriculum2 colr2">政治</view>
			</view>
			<view class="currlum1">
				<view class="curriculum1 colr">第七节</view>
				<view class="curriculum1 colr1">(08:00~09:00)</view>
				<view class="curriculum2 colr2">化学</view>
			</view>
		</view>
		
		<!-- 菜单 -->
		<view class="tabs-style-box">
			<!-- 滑动区域 -->
						<scroll-view class="scroll-view_H" style="width: 100%;" show-scrollbar="true"  scroll-x="true" scroll-with-animation :scroll-left="tabsScrollLeft" @scroll="scroll">
							<view class="tab" id="tab_list">
								<view class="tabs-box" @tap="school">
									<view class="tabs-img-box">
										<image class="tabs-img-style" src="../../static/546596e605166.jpg"></image>
									</view>
									<view class="tabs-font-box">
									<view class="tabs-font-style">
										学校
									</view>
									</view>
								</view>
								
								<view class="tabs-box tabs-left" @tap="bulletinboard">
									<view class="tabs-img-box">
										<image class="tabs-img-style" src="../../static/546596e605166.jpg"></image>
									</view>
									<view class="tabs-font-box">
									<view class="tabs-font-style">
										布告栏
									</view>
									</view>
								</view>
								
								<view class="tabs-box tabs-left" @tap="rating">
									<view class="tabs-img-box">
										<image class="tabs-img-style" src="../../static/546596e605166.jpg"></image>
									</view>
									<view class="tabs-font-box">
									<view class="tabs-font-style">
										七彩评比
									</view>
									</view>
								</view>
								
								<view class="tabs-box tabs-left" @tap="interclass">
									<view class="tabs-img-box">
										<image class="tabs-img-style" src="../../static/546596e605166.jpg"></image>
									</view>
									<view class="tabs-font-box">
									<view class="tabs-font-style">
										班际
									</view>
									</view>
								</view>
								
								<view class="tabs-box tabs-left" @tap="attendance">
									<view class="tabs-img-box">
										<image class="tabs-img-style" src="../../static/546596e605166.jpg"></image>
									</view>
									<view class="tabs-font-box">
									<view class="tabs-font-style">
										全校出勤汇总
									</view>
									</view>
								</view>
								
								<view class="tabs-box tabs-left" @tap="classcard">
									<view class="tabs-img-box">
										<image class="tabs-img-style" src="../../static/546596e605166.jpg"></image>
									</view>
									<view class="tabs-font-box">
									<view class="tabs-font-style">
										课程
									</view>
									</view>
								</view>
								
								<view class="tabs-box tabs-left" @tap="placereservation">
									<view class="tabs-img-box">
										<image class="tabs-img-style" src="../../static/546596e605166.jpg"></image>
									</view>
									<view class="tabs-font-box">
									<view class="tabs-font-style">
										场所预约
									</view>
									</view>
								</view>
								
								<view class="tabs-box tabs-left" @tap="commend">
									<view class="tabs-img-box">
										<image class="tabs-img-style" src="../../static/546596e605166.jpg"></image>
									</view>
									<view class="tabs-font-box">
									<view class="tabs-font-style">
										模块测试-表彰
									</view>
									</view>
								</view>
								
								<view class="tabs-box tabs-left" @tap="countdown" >
									<view class="tabs-img-box">
										<image class="tabs-img-style" src="../../static/546596e605166.jpg"></image>
									</view>
									<view class="tabs-font-box">
									<view class="tabs-font-style">
										倒计时
									</view>
									</view>
								</view>
								
								<view class="tabs-box tabs-left" @tap="studentdemeanor">
									<view class="tabs-img-box">
										<image class="tabs-img-style" src="../../static/546596e605166.jpg"></image>
									</view>
									<view class="tabs-font-box">
									<view class="tabs-font-style">
										学生风彩
									</view>
									</view>
								</view>
								<view class="tabs-box tabs-left" @click="jumpLeaving">
									<view class="tabs-img-box">
										<image class="tabs-img-style" src="../../static/546596e605166.jpg"></image>
									</view>
									<view class="tabs-font-box">
									<view class="tabs-font-style">
										留言寄语
									</view>
									</view>
								</view>
								
								<view class="tabs-box tabs-left" @click="jumpEvlate()">
									<view class="tabs-img-box">
										<image class="tabs-img-style" src="../../static/546596e605166.jpg"></image>
									</view>
									<view class="tabs-font-box">
									<view class="tabs-font-style">
										评价
									</view>
									</view>
								</view>
								
								<view class="tabs-box tabs-left" @click="jumpachievement()">
									<view class="tabs-img-box">
										<image class="tabs-img-style" src="../../static/546596e605166.jpg"></image>
									</view>
									<view class="tabs-font-box">
									<view class="tabs-font-style">
										成绩排行榜
									</view>
									</view>
								</view>
								
								<view class="tabs-box tabs-left" @click="jumpFace()">
									<view class="tabs-img-box">
										<image class="tabs-img-style" src="../../static/546596e605166.jpg"></image>
									</view>
									<view class="tabs-font-box">
									<view class="tabs-font-style">
										人脸考勤
									</view>
									</view>
								</view>
								
								<view class="tabs-box tabs-left" @click="jumpCheck()">
									<view class="tabs-img-box">
										<image class="tabs-img-style" src="../../static/546596e605166.jpg"></image>
									</view>
									<view class="tabs-font-box">
									<view class="tabs-font-style">
										安全信息
									</view>
									</view>
								</view>
								
								<view class="tabs-box tabs-left" @click="jumpMetting()">
									<view class="tabs-img-box">
										<image class="tabs-img-style" src="../../static/546596e605166.jpg"></image>
									</view>
									<view class="tabs-font-box">
									<view class="tabs-font-style">
										会议签到
									</view>
									</view>
								</view>
								
								<view class="tabs-box tabs-left" @click="jumpTest()">
									<view class="tabs-img-box">
										<image class="tabs-img-style" src="../../static/546596e605166.jpg"></image>
									</view>
									<view class="tabs-font-box">
									<view class="tabs-font-style">
										考试信息
									</view>
									</view>
								</view>
								
								<view class="tabs-box tabs-left" @click="jumpDoor()">
									<view class="tabs-img-box">
										<image class="tabs-img-style" src="../../static/546596e605166.jpg"></image>
									</view>
									<view class="tabs-font-box">
									<view class="tabs-font-style">
										门禁
									</view>
									</view>
								</view>
								
								<view class="tabs-box tabs-left" @click="jumpAbout()">
									<view class="tabs-img-box">
										<image class="tabs-img-style" src="../../static/546596e605166.jpg"></image>
									</view>
									<view class="tabs-font-box">
									<view class="tabs-font-style">
										关于
									</view>
									</view>
								</view>
								
							</view>
						</scroll-view>
		</view>
			
	</view>
</template>

<script>
	export default {
		data() {
			   return {
							imageURL: '../../static/img/0背景.png',
							background: ['color1', 'color2', 'color3'],
							indicatorDots: false,
							autoplay: true,
							interval: 6000,
							duration: 1000
					  };
		        },
				watch: {
					listActive(newVal) {     // 监听当前选中项
						this.setTabList()
					}
				},
				
				mounted () {
				    this.setTabList()
				},

		onLoad() {

		},

methods: {
		//月评价  
		monthlyassessment:function(){
			   uni.navigateTo({
				   url:'../monthlyassessment/monthlyassessment',
			   });
		   },
		 //通知
		 notice:function(){
			 uni.navigateTo({
			 		url:'../notice/notice',
			 });
		 },
		 //课表
		 classcard:function(){
			 uni.navigateTo({
			 		url:'../ClassScheduleCard/classcard',
			 });
		 },
		 //班级风采
		 classdemeanor:function(){
			 uni.navigateTo({
			 		url:'../classdemeanor/classdemeanor',
			 });
		 },
		 // 学校
		 school:function(){
			 uni.navigateTo({
			 		url:'../school/school',
			 });
		 },
		 // 布告栏
		 bulletinboard:function(){
		 			 uni.navigateTo({
		 			 		url:'../bulletinboard/bulletinboard',
		 			 });
		 },
		 // 七彩评比
		 rating:function(){
		 			 uni.navigateTo({
		 			 		url:'../rating/rating',
		 			 });
		 },
		 
		 // 班际
		 interclass:function(){
		 			 uni.navigateTo({
		 			 		url:'../interclass/interclass',
		 			 });
		 },
		 // 出勤
		 attendance:function(){
		 			 uni.navigateTo({
		 			 		url:'../attendance/attendance',
		 			 });
		 },
		 // 课程
		 // school:function(){
		 // 			 uni.navigateTo({
		 // 			 		url:'../school/school',
		 // 			 });
		 // },
		 // 预约
		 placereservation:function(){
		 			 uni.navigateTo({
		 			 		url:'../placereservation/placereservation',
		 			 });
		 },
		 // 表彰
		 commend:function(){
		 			 uni.navigateTo({
		 			 		url:'../commend/commend',
		 			 });
		 },
		 // 倒计时
		 countdown:function(){
		 			 uni.navigateTo({
		 			 		url:'../countdown/countdown',
		 			 });
		 },
		 // 学生风采
		 studentdemeanor:function(){
		 			 uni.navigateTo({
		 			 		url:'../studentdemeanor/studentdemeanor',
		 			 });
		 },
		 // 留言寄语
		 jumpLeaving () {
			 uni.navigateTo({
			 	url: '../message/message'
			 })
		 },
		 // 评价
		 jumpEvlate () {
			 uni.navigateTo({
			 	url: '../evaluate/evaluate'
			 })
		 },
		 // 跳转成绩
		 jumpachievement () {
			 uni.navigateTo({
				 url: '../achievement/achievement'
			 })
		 },
		 // 考勤
		 jumpFace () {
			uni.navigateTo({
				url: '../checkWorke/checkWorke'
			}) 
		 },
		 // 安全页
		 jumpCheck () {
			 uni.navigateTo({
				url: '../safePage/safePage'
			 })
		 },	 
		 // 会议签到
		 jumpMetting () {
			 uni.navigateTo({
			 	url: '../meeting/meeting'
			 })
		 },
		 // 门禁
		 jumpDoor () {
			 uni.navigateTo({
			 	url: '../door/door'
			 })
		 },
		 // 考试
		 jumpTest () {
			 uni.navigateTo({
			 	url: '../test/test'
			 })
		 },
		 // 关于
		 jumpAbout () {
			 console.log()
			 uni.navigateTo({
			 	url: '../about/about'
			 })
		 },
		 // 老师详情
		 jumpTheACher () {
			uni.navigateTo({
				url: '../teacher/teacher'
			}) 
		 },
		 // 天气页
		 jumpWeather () {
			 uni.navigateTo({
			 	url: '../weather/weather'
			 })
		 },
		 gengduo:function(e){
		 	uni.showModal({
		 		content:"李萌老师,中共党员中学高级化教师，现在任2020届年级副主任，班主任，年级党支部书记。工作勤勉,敬业,细致、严谨、奋进、爱校爱班级爱生，工作以来多次评为市。区。校“优秀教师”、“优秀党员”、“科学带头人”、“骨干教师”、“党员示范岗”、“、优秀班主任”",
		 		showCancel: false,
		 		confirmText: "确定"
		 	})
		 },
		 
		 
		 // 计算tabs位置
		 scrollIntoView() {  // item滚动
		 	let lineLeft = 0;
		 	this.getElementData('#tab_list', (data)=> {
		 		let list = data[0]
		 		this.getElementData(`#tab_item`, (data)=> {
		 			let el = data[this.listActive]
		 			lineLeft = el.width / 2 + (-list.left) + el.left - list.width / 2 - this.scrollLeft
		 			this.tabsScrollLeft = this.scrollLeft + lineLeft
		 		})
		 	})
		 },
		  
		 clickSort (index) {
		 	this.listActive = index
		 },
		 // scroll-view滑动事件
		 scroll(e) {
		 	this.scrollLeft = e.detail.scrollLeft;
		 },
		 setTabList() {
		 	this.$nextTick(()=>{
		 		this.setLine()
		 		this.scrollIntoView()
		 	})
		 }, 
		  
		}
	}
</script>

<!-- scoped  只应用在当前的页面 -->
<style scoped>
	@import './indexcss.css';
	
	.sticky-box {
		/* #ifndef APP-PLUS-NVUE */
		display: flex;
		position: -webkit-sticky;
		/* #endif */
		position: sticky;
		top: var(--window-top);
		z-index: 99;
		flex-direction: row;
		margin: 0px;
		border-top: 1px #f9f9f9 solid;
		border-bottom: 1px #f9f9f9 solid;
		background: #fff;
	}
		.listAll{
		width: 20%;
		text-indent: 62rpx;
		font-size: 30rpx;
		border-left: 1px #eee solid;
		margin: 1% 0 ;
		padding: 5rpx;
		position: relative;
		image{
		position: absolute;
		left: 20rpx;
		top: 8rpx;
		}
		}
		.tab {
		position: relative;
		display: flex;
		font-size: 28rpx;
		padding-bottom: 10rpx;
		white-space: nowrap;
		&__item {
		flex: 1;
		padding: 0 20rpx;
		text-align: center;
		height: 60rpx;
		line-height: 60rpx;
		color: #666;
		&.active {
			color: #09C2C9;
		}
		}
		}
		.tab__line {
		display: block;
		height:6rpx;
		position: absolute;
		bottom: 0;
		left: 0;
		z-index: 1;
		border-radius: 3rpx;
		position: relative;
		background: #2FC6CD;
		}
		.scroll-view_H {
		/* 文本不会换行，文本会在在同一行上继续，直到遇到 <br> 标签为止。 */
		white-space: nowrap;
		width: 100%;
		}
</style>
