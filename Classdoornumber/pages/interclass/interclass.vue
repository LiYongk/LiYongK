<template>
	  <view>
	        <view class="uni-padding-wrap">
	            <view class="page-section swiper">
	                <view class="page-section-spacing">
	                    <swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :style="{height:listHeight+ 'rem'}" :interval="interval" :duration="duration">
	                        <swiper-item class="swiper1">
	                            <view class="inter-head div-filter">
	                            	<view class="item-classname font-color-size">
	                            		高二2班
	                            	</view>
	                            	<view class="class-information font-color-size1">
	                            		这是一个五星的班级
	                            	</view>
	                            	<view class="learn-more font-color-size1" @tap="learnmore">
	                            		了解更多>>
	                            	</view>
	                            </view>
	                        </swiper-item>
	                        <swiper-item class="swiper2">
								<view class="education education-font">
									<view class="education-tilte">安全教育重要通知</view>
									<view class="education-content">
										世间没有最悠扬的曲子，却有安全这一曲绕梁余音，跌宕起伏地浅唱着生命的旋律；凡尘没有最优美的诗词，却有安全这一阕千古绝唱，平仄起伏地叹咏着生命的韵味；人生没有最神韵的色彩，却有安全这一簇浓墨重彩，惟妙惟肖地勾勒着生命的蓝图。
										是否有一叶无帆扁舟，顺利地驶进一个个有生命的港湾，最后抵达成功的彼岸？是否有一支丹青妙笔，神奇地画出一双双不流泪的眼睛，永久墨染幸福的忧伤？是否有一种断弦琴瑟，流畅地弹奏出一簌簌无哀伤的音符，永世绽放生命的浪花？
										世间没有最悠扬的曲子，却有安全这一曲绕梁余音，跌宕起伏地浅唱着生命的旋律；凡尘没有最优美的诗词，却有安全这一阕千古绝唱，平仄起伏地叹咏着生命的韵味；人生没有最神韵的色彩，却有安全这一簇浓墨重彩，惟妙惟肖地勾勒着生命的蓝图。
										是否有一叶无帆扁舟，顺利地驶进一个个有生命的港湾，最后抵达成功的彼岸？是否有一支丹青妙笔，神奇地画出一双双不流泪的眼睛，永久墨染幸福的忧伤？是否有一种断弦琴瑟，流畅地弹奏出一簌簌无哀伤的音符，永世绽放生命的浪花？
									</view>
									<view class="inter-head1 div-filter1">
										<view class="item-classname font-color-size">
											露露家园驿站
										</view>
										<view class="class-information font-color-size1">
											
										</view>
										<view class="learn-more font-color-size1">
											了解更多>>
										</view>
								</view>
								</view>
	                        </swiper-item>
	                        <swiper-item class="swiper3">
	                            <view class="swiper-item uni-bg-blue">暂无内容</view>
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

<style scoped>
	
	@import url("./interclasscss.css");
	
</style>
