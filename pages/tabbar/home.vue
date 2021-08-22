<template>
	<view class="content">
		<view class="top-box">
			
			<view class="search-box">
				<image class="search-icon" src="../../static/gallery_search_icon.jpeg"></icon>
				<input class="search-input" placeholder="搜索感兴趣的关键字" />
			</view>
			
		</view>
		
		<scroll-view>
			<view v-for="(item, index) in list">
				<GalleryMoment
					v-bind:icon="item.iconUrl"
					v-bind:name="item.familyName"
					v-bind:uploadTime="item.uploadTime"
					v-bind:like="item.like"
					v-bind:tags="item.tags"
					v-bind:desc="item.description"
				/>
			</view>
		</scroll-view>
		
	</view>
</template>

<script>
	import GalleryMoment from '../gallery/moment.vue'
	
	export default {
		components: {
			GalleryMoment
		},
		data() {
			return {
				list: [
					{
						iconUrl: "",
						familyName: "aaa",
						uploadTime: 1629643582000,
						duration: 36000,
						like: 22,
						tags: ['aa', 'bb'],
						description: "这是个描述"
					},
					{
						iconUrl: "",
						familyName: "aaa",
						uploadTime: 1629643582000,
						duration: 36000,
						like: 22,
						tags: ['aa', 'bb'],
						description: "这是个描述"
					}
				]
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
		background-color: #FFFFFF;
	}
	
	.top-box {
		width: 100%;
		height: 50rpx;
		display: flex;
		justify-content: row;
		align-items: center;
		margin-top: 10rpx;
		background-color: #F1F1F1;
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
