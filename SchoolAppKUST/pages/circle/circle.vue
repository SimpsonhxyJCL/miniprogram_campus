<template>
	<view class="circle">
		<text>圈子</text>
		<u-row customStyle="margin:10px  10px 10px 10px "  gutter="10">
			<u-col span="4">
				<view class="demo-layout bg-purple fl">
					<u-button size="small" shape="circle" type="primary" text="纸条"></u-button>
				</view>
			</u-col>
			<u-col span="5">
				<view class="demo-layout bg-purple fr">
					<u-button type="primary" shape="circle" size="small" text="关注"></u-button>
				</view>
			</u-col>
		</u-row>
	</view>
</template>

<script>
</script>

<style>
	.bg-purple {
		width: 80px;
	}
	.fr{
		float:right;
	}
	.fl{
		float:left;
	}
</style>
