<template>
	<view>
		
		<view class="uni-padding-wrap">
		    <view class="page-section swiper">
		        <view class="page-section-spacing">
		            <swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :style="{height:listHeight+ 'rem'}" :interval="interval" :duration="duration">
		                <swiper-item class="swiper1">
		                   		<view class="commend-title">
		                   			<view class="commend-font">
		                   				表彰
		                   			</view>
		                   		</view>
		                   		<view class="comend-content comend-font">
		                   			姗姗同学第一名
		                   		</view>
		                   		<view class="bottom-content comend-font">
		                   			<view class="inner-frame">
		                   				先知中学
		                   			</view>
		                   			<view class="inner-frame">
		                   				2020-3-19
		                   			</view>
		                   		</view>
		                </swiper-item>
						
		                <swiper-item class="swiper2">
							<view class="commend-title">
								<view class="commend-font colo-style2">
									表彰
								</view>
							</view>
							<view class="comend-content comend-font">
								姗姗 祝姗姗同学总成绩荣获全校第一名
							</view>
							<view class="bottom-content comend-font">
								<view class="inner-frame">
									先知中学
								</view>
								<view class="inner-frame">
									2020-3-19
								</view>
							</view>
		                </swiper-item>
						
		                <swiper-item class="swiper3">
		                    <view class="swiper-item uni-bg-blue">
								<view class="commend-title">
									<view class="commend-font colo-style3">
										表彰
									</view>
								</view>
								<view class="comend-content comend-font">
									林品如老师积极活泼
								</view>
								<view class="bottom-content comend-font">
									<view class="inner-frame">
										高一2班
									</view>
									<view class="inner-frame">
										2020-3-19
									</view>
								</view>
							</view>
		                </swiper-item>
						
						<swiper-item class="swiper4">
						    <view class="swiper-item uni-bg-blue">
								<view class="commend-title">
									<view class="commend-font colo-style4">
										表彰
									</view>
								</view>
								<view class="comend-content comend-font">
									李明明 恭贺新婚
								</view>
								<view class="bottom-content comend-font">
									<view class="inner-frame">
										高一2班
									</view>
									<view class="inner-frame">
										2020-3-19
									</view>
								</view>
							</view>
						</swiper-item>
						
						<swiper-item class="swiper5">
						    <view class="swiper-item uni-bg-blue">
								<view class="commend-title">
									<view class="commend-font colo-style5">
										表彰
									</view>
								</view>
								<view class="comend-content comend-font">
									李飞三好学生
								</view>
								<view class="bottom-content comend-font">
									<view class="inner-frame">
										育才中学
									</view>
									<view class="inner-frame">
										2020-3-19
									</view>
								</view>
							</view>
						</swiper-item>
						
						<swiper-item class="swiper6">
						    <view class="swiper-item uni-bg-blue">
								<view class="commend-title">
									<view class="commend-font colo-style6">
										表彰
									</view>
								</view>
								<view class="comend-content comend-font">
									林帆 荣获三号学生称号
								</view>
								<view class="bottom-content comend-font">
									<view class="inner-frame">
										先知中学
									</view>
									<view class="inner-frame">
										2020-3-19
									</view>
								</view>
							</view>
						</swiper-item>
						
						<swiper-item class="swiper7">
						    <view class="swiper-item uni-bg-blue">
								<view class="commend-title">
									<view class="commend-font colo-style7">
										表彰
									</view>
								</view>
								<view class="comend-content comend-font">
									李可可 荣获三号学生称号
								</view>
								<view class="bottom-content comend-font">
									<view class="inner-frame">
										先知中学
									</view>
									<view class="inner-frame">
										2020-3-19
									</view>
								</view>
							</view>
						</swiper-item>
						
						
		            </swiper>
		        </view>
		    </view>
		</view>
		
		
		
		<view class="error" @tap="error">
			<image class="error-img" src="../../static/errorimg.png"></image>
		</view>
	</view>
</template>

<script>
	export default {
	    data() {
	        return {
	            background: ['color1', 'color2', 'color3'],
	            indicatorDots: true,
	            autoplay: stop(),
	            interval: 2000,
	            duration: 500,
				listHeight:11
	        }
	    },
	    methods: {
				getEleHeight(list){
                let info = uni.createSelectorQuery().in(_self).select(list);
        　　　  　info.boundingClientRect(function(data) { //data - 各种参数
        　　　  　    if(data != null){
                        _self.listHeight = data.height;
                    }else{
                        setTimeout(function(){
                            _self.getEleHeight('.swiper-item');
                        },3)
                    }
        　　    }).exec()
            },
			learnmore:function(){
				uni.navigateTo({
					url:'../learnmore/learnmore',
				})
			},
			error:function(){
				uni.redirectTo({
					url:'../index/index'
				})
			}
			
	    }
	}
</script>

<style>
	@import url("./commendcss.css");
</style>
