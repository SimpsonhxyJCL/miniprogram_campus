<template>
	<view class="loginContainer">
		<h1>登录页面</h1>
		<view class="helloMsg">{{msg}}</view>
		<!--微信登录 -->
		<u-button type="primary" size="normal"  text="微信登录" @click="logIn()" style=" margin-top: 200px;"></u-button>
		<!-- 手机验证码登录 -->
		
	</view>
</template>

<script>
	export default {
		data(){
			return {
				msg:'Hello KUSTER',
			}
		},
		methods:{
			logIn(){
				// 参考之前写的拉取微信用户信息并授权登录
				uni.navigateTo({
					url:'../index/index'
				})
			}
		},
	}
</script>

<style lang=scss>
	.loginContainer{
		background-color: "#7dabff";
		width: auto;
		height: 100%;
		padding: 20px;
		font-size: 14px;
		line-height: 24px;
		.helloMsg{
			margin-top: 200rpx;
			margin-bottom: 200rpx;
			font-size: 24px;
			text-align: center;
			color:"#303133" ;
		}
	}
</style>
