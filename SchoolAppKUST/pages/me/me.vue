<template>
	<view class="me">
		<!-- <text>me</text> -->
		<template>
			<view class="avatar-group">
				<view class="">
					<u-row customStyle="margin:10px  10px 10px 10px "  gutter="10">
						<u-col span="4">
							<view class="demo-layout bg-purple fl">
								<u-button size="small" shape="circle" type="primary" text="加好友"></u-button>
							</view>
						</u-col>
						<u-col span="6">
							<view class="demo-layout bg-purple fr">
								<u-button type="primary" shape="circle" size="small" text="设置"></u-button>
							</view>
						</u-col>
					</u-row>
				</view>
				<view class="avatar-img">
					<u-avatar :src="src"></u-avatar>
				</view>
			</view>
		</template>
		<view>
			<u-grid :border="false" @click="click">
				<u-grid-item v-for="(baseListItem,baseListIndex) in baseList" :key="baseListIndex">
					<u-icon :customStyle="{paddingTop:20+'rpx'}" :name="baseListItem.name" :size="30"></u-icon>
					<text class="grid-text">{{baseListItem.title}}</text>
				</u-grid-item>
			</u-grid>
			<u-toast ref="uToast" />
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				baseList: [{
						name: 'photo',
						title: '关注'
					},
					{
						name: 'lock',
						title: '粉丝'
					},
					{
						name: 'star',
						title: '状态'
					},
				],
				src: '/static/weixintouxiang.png',
			}
		},
		methods: {
			click(name) {
				this.$refs.uToast.success(`点击了第${name}个`)
			}
		}
	}
</script>

<style  lang="scss" scoped>
	.avatar-group {
		display: block;
		width: auto;
		height: 250px;
		background-color: #a0cfff;
		margin: 0 auto;
		text-align: center;
	}

	.avatar-img {
		dispay: block;
		width: 50px;
		height: 50px;
		border-radius:15px;
		background: white;
		margin-top:100px; 
		margin: auto;
		/* text-align: center; */
		position: relative;
		top: 90px;
		/* left:70px; */
	}

	.avator-buton1 {
		width: 40px;
		height: 25px;
	}

	.fl {
		float: left;
	}

	.fr {
		float: right;
	}
	.bg-purple {
		width: 80px;
	}
	
</style>
