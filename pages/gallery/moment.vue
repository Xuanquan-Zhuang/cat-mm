<template>
	<view class="container">
		
		<view class="family-box">
			<image class="family-avatar" src="../../static/logo.png"></image>
			<text class="family-name">{{name}}</text>
		</view>
		
		<image class="video-preview"></image>
		
		<view class="like-container">
			<image class="like-icon" src="../../static/tabbar/tab-cart-current.png"/>
			<text class="like-count">{{like}}</text>
		</view>
		
		<view class="tag-container">{{tags}}</view>
		
		<view class="description">{{desc}}</view>
	</view>
</template>

<script>
	export default {
		name: "GalleryMoment",
		props: {
			// 头像
			icon: {
				type: String,
				default: "--"
			},
			// 猫窝名称
			name: {
				type: String,
				default: "--"
			},
			// 上传时间
			uploadTime: {
				type: String,
				default: "未知"
			},
			// 视频预览图
			preview: {
				type: String
			},
			// 点赞数
			like: {
				type: Number,
				default: 0
			},
			// 标签
			tags: {
				type: Array
			},
			// 描述
			desc: {
				type: String
			}
		}
	}
</script>

<style>
	.container {
		display: flex;
		flex-direction: column;
		justify-content: flex-start;
		align-items: center;
		width: 100%;
		height: 600rpx;
		background-color: #007AFF;
		margin-top: 10rpx;
	}
	
	.family-box {
		display: flex;
		flex-direction: row;
		justify-content: flex-start;
		align-items: flex-end;
		width: 100%;
		height: 50rpx;
		background-color: #4CD964;
	}
	
	.family-avatar {
		width: 40rpx;
		height: 40rpx;
		margin-left: 20rpx;
	}
	
	.family-name {
		font-size: 20rpx;
		margin-left: 10rpx;
	}
	
	.video-preview {
		width: 100%;
		height: 400rpx;
		background-color: #555555;
		margin-top: 20rpx;
	}
	
	.like-container {
		width: 100%;
		height: 40rpx;
		margin-top: 20rpx;
	}
	
	.like-icon {
		width: 40rpx;
		height: 40rpx;
		margin-left: 20rpx;
	}
	
	.like-count {
		font-size: 20rpx;
		margin-left: 10rpx;
	}
	
	.tag-container {
		font-size: 20rpx;
		color: #000000;
	}
	
	.description {
		font-size: 20rpx;
		color: #8F8F94;
	}
</style>
