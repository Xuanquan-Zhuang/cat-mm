<template>
	<view class="container">
		
		<view class="family-box">
			<image class="family-avatar" src="../../static/logo.png"></image>
			<text class="family-name">庄庄家</text>
		</view>
		
		<image class="video-preview"></image>
		
		<view class="like-container">
			<image class="like-icon" src="../../static/tabbar/tab-cart-current.png"/>
			<text class="like-count">2222</text>
		</view>
	</view>
</template>

<script>
	export default {
		name: "GalleryMoment"
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
</style>
