<template>
	<view class="container">
		<h1>校园首页</h1>
		<!-- <view class="intro">本项目为：校园圈 小程序，计划寒假开发，参照需求文档。</view>
		<text class="intro">计划：1-2月 完成基本的功能 </text><br>
		<uni-link :href="href" :text="conentLink"></uni-link>
		<view class="">
		        <uni-forms :modelValue="formData">
		            <uni-forms-item label="姓名" name="name">
		                <uni-easyinput type="text" v-model="formData.name" placeholder="请输入姓名" />
		            </uni-forms-item>
		            <uni-forms-item required name="hobby" label="兴趣爱好">
		                <uni-data-checkbox multiple v-model="formData.hobby" :localdata="hobby"/>
		            </uni-forms-item>
		        </uni-forms>
		        <button @click="submitForm">Submit</button>
		    </view> -->
		<!-- 首页轮播图 -->
		<u-swiper :list="swiperList" indicator indicatorMode="line" circular keyName="image" showTitle></u-swiper>
		<u-divider text="分割线" :dot="true"></u-divider>
		<!-- 相册 -->
		<view class="u-demo-block__content">
			<view class="album">
				<view class="album__avatar">
					<image src="/static/weixintouxiang.png" mode="" style="width: 32px;height: 32px;"></image>
				</view>
				<view class="album__content">
					<u--text text="子敬" type="primary" bold size="17"></u--text>
					<u--text margin="0 0 8px 0" text="考研复习资料"></u--text>
					<u-album :urls="urls"></u-album>
				</view>
			</view>
		</view>
	</view>

</template>

<script>
	export default {
		data() {
			return {
				href: 'https://uniapp.dcloud.io/component/README?id=uniui',
				conentLink: 'uni ui的使用详情，参见文档链接',
				formData: {
					name: '',
					hobby: ''
				},
				swiperList: [{
						image: 'https://cdn.uviewui.com/uview/swiper/swiper1.png',
						title: '图一',
					},
					{
						image: 'https://cdn.uviewui.com/uview/swiper/swiper2.png',
						title: '图二',
					},
					{
						image: 'https://cdn.uviewui.com/uview/swiper/swiper3.png',
						title: '图三',
					},
				],

				// 首页相册块
				urls: [
					'https://cdn.uviewui.com/uview/album/1.jpg',
					'https://cdn.uviewui.com/uview/album/2.jpg',
					'https://cdn.uviewui.com/uview/album/3.jpg',
					'https://cdn.uviewui.com/uview/album/4.jpg',
					'https://cdn.uviewui.com/uview/album/5.jpg',
					'https://cdn.uviewui.com/uview/album/6.jpg',
					'https://cdn.uviewui.com/uview/album/7.jpg',
					'https://cdn.uviewui.com/uview/album/8.jpg',
					'https://cdn.uviewui.com/uview/album/9.jpg',
					'https://cdn.uviewui.com/uview/album/10.jpg',
				],
			}
		},
		methods: {
			submitForm() {
				console.log("信息提交成功！")
			}
		}
	}
</script>

<style>
	.container {
		padding: 20px;
		font-size: 14px;
		line-height: 24px;
	}
</style>
