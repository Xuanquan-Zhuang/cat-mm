<template>
	<view class="content">
		<view class="top-box">
			
			<view class="search-box">
				<image class="search-icon" src="../../static/gallery_search_icon.jpeg"></icon>
				<input class="search-input" placeholder="搜索感兴趣的关键字" />
			</view>
			
		</view>
		
		<GalleryMoment></GalleryMoment>
	</view>
</template>

<script>
	import GalleryMoment from '../gallery/moment.vue'
	
	export default {
		components: {
			GalleryMoment
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
	
	.top-box {
		width: 100%;
		height: 50rpx;
		display: flex;
		justify-content: row;
		align-items: center;
		margin-top: 10rpx;
	}
	
	.search-box {
		width: 60%;
		height: 50rpx;
		border: 2rpx solid;
		border-color: #808080;
		border-radius: 25rpx;
		margin-left: 2%;
		display: flex;
		justify-content: row;
		align-items: center;
	}
	
	.search-icon {
		margin-left: 2%;
		width: 40rpx;
		height: 40rpx;
	}
	
	.search-input {
		margin-left: 2%;
	}
</style>
