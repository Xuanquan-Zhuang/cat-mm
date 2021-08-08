<template>
	<view class="content">
		<view class="topBar">
			<view class="searchBox">
				<image class="searchIcon" src="/static/gallery_search_icon.jpeg"/>
				<input class="searchInput"/>
			</view>
			<text class="sort">排序</text>
		</view>
		
		<scroll-view class="itemList">
			<view class="itemRow">
				<view class="item"></view>
				<view class="item"></view>
			</view>
			
			<view class="itemRow">
				<view class="item"></view>
				<view class="item"></view>
			</view>
			
			<view class="itemRow">
				<view class="item"></view>
				<view class="item"></view>
			</view>
			
			<view class="itemRow">
				<view class="item"></view>
				<view class="item"></view>
			</view>
			
			<view class="itemRow">
				<view class="item"></view>
				<view class="item"></view>
			</view>
			
			<view class="itemRow">
				<view class="item"></view>
				<view class="item"></view>
			</view>
		</scroll-view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			renderGallery: function() {
				
			}
		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}
	
	.topBar {
		height: 50rpx;
		width: 100%;
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: flex-start;
		margin-top: 20rpx;
	}
	
	.sort {
		widith: 40%;
		height: 50rpx;
		font-size: 36rpx;
		color: #8f8f94;
		margin-left: 3%;
		background: #007AFF;
	}
	
	.searchBox {
		width: 60%;
		height: 50rpx;
		border-radius: 25rpx;
		border: 5rpx solid;
		border-color: #000000;
		margin-left: 2%;
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: flex-start;
	}
	
	.searchIcon {
		width: 50rpx;
		height: 50rpx;
	}
	
	.searchInput {
		font-size: 30rpx;
	}
	
	.itemList {
		margin-top: 20rpx;
	}
	
	.itemRow {
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
		margin-top: 10rpx;
		height: 100rpx;
	}
	
	.item {
		width: 40%;
		height: 100rpx;
		background: #007AFF;
		margin-right: 10rpx;
		margin-left: 10rpx;
	}
</style>
