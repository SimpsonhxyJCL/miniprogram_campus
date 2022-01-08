<template>
	<view class="container">
		
		<view class="intro">本项目为：校园圈 小程序，计划寒假开发，参照需求文档。</view>
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
		    </view>
	</view>
	
</template>

<script>
	export default {
		data() {
			return {
				href: 'https://uniapp.dcloud.io/component/README?id=uniui',
				conentLink:'uni ui的使用详情，参见文档链接',
				formData:{
					name:'',
					hobby:''
				},
				// hobby:['学习','听歌']
			}
		},
		methods: {
			submitForm(){
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
