<template>
	  <view>
	        <view class="uni-padding-wrap">
	            <view class="page-section swiper">
	                <view class="page-section-spacing">
	                    <swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :style="{height:listHeight+ 'rem'}" :interval="interval" :duration="duration">
	                        <swiper-item class="swiper1">
	                            <view class="swiper-item uni-bg-red">
									<view class="doc">
										<view class="doc-top doc-top1">
											<view class="doc-lang-pair doc-lan font-week">03-16&nbsp;&nbsp;周一</view>
											<view class="doc-lang-pair font-week1">100分</view>
										</view>
										<view class="doc-top">
											<view class="doc-lang-pair doc-lan font-week">03-17&nbsp;&nbsp;周二</view>
											<view class="doc-lang-pair font-week1">99分</view>
										</view>
										<view class="doc-top">
											<view class="doc-lang-pair doc-lan font-week">03-18&nbsp;&nbsp;周三</view>
											<view class="doc-lang-pair font-week1">88分</view>
										</view>
										<view class="doc-top">
											<view class="doc-lang-pair doc-lan font-week">03-19&nbsp;&nbsp;周四</view>
											<view class="doc-lang-pair font-week1">100分</view>
										</view>
										<view class="doc-top">
											<view class="doc-lang-pair doc-lan font-week">03-20&nbsp;&nbsp;周五</view>
											<view class="doc-lang-pair font-week1">78分</view>
										</view>
									</view>
									<!-- 评分 -->
									<view>
										<view class="to-doc-bottom">
											<view class="bottom-doc bottom-doc1">
												<view class="doc-content">
													<view class="doc-b-view"></view>
													<view class="doc-hygiene">卫生</view>
													<view class="doc-hygiene1">20分</view>
												</view>
												<view class="doc-content content-font">教室卫生</view>
												<view class="doc-content content-font">公共卫生</view>
												<view class="doc-content content-font">个人卫生</view>
											</view>
											<!-- 分割线 -->
											<view class="bottom-doc-zhong"></view>
											<view class="bottom-doc bottom-doc1">
												<view class="doc-content">
													<view class="doc-b-view"></view>
													<view class="doc-hygiene">纪律</view>
													<view class="doc-hygiene1">100分</view>
												</view>
												<view class="doc-content content-font">早读</view>
												<view class="doc-content content-font">课堂纪律</view>
												<view class="doc-content content-font">体操</view>
											</view>
											<view class="doc-beiz" @tap="beiz">备注</view>
										</view>
									</view>
								</view>
	                        </swiper-item>
	                        <swiper-item class="swiper2">
	                            <view class="swiper-item uni-bg-green">
									<view class="uni-bg-fid uni-bg-fid-font uni-bg-green">
										<view>上周荣誉</view>
									</view>
									<view class="uni-bg-fid uni-bg-fid-font uni-bg-green">
										<view>本周荣誉</view>
									</view>
									<view class="uni-bg-fid uni-bg-fid-font uni-bg-green">
										<view>周一</view>
									</view>
									<view class="uni-bg-fid uni-bg-fid-font uni-bg-green">
										<view>周二</view>
									</view>
									<view class="uni-bg-fid uni-bg-fid-font uni-bg-green">
										<view>周三</view>
									</view>
									<view class="uni-bg-fid uni-bg-fid-font uni-bg-green">
										<view>周四</view>
									</view>
									<view class="uni-bg-fid uni-bg-fid-font uni-bg-green">
										<view>周五</view>
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
				listHeight:10
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
			
			beiz:function(){
				uni.showModal({
					content: "暂无备注",
					showCancel: false,
					confirmText: "确定"
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
	@import url("./monthlyassessmentcss.css");
</style>
