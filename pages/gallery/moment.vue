<template>
	<view class="container">
		
		<view class="family-box">
			<image class="family-avatar" src="../../static/logo.png"></image>
			<text class="family-name">{{name}}</text>
			<text class="upload-time">{{createUploadTimeString(uploadTime)}}</text>
		</view>
		
		<video class="video-preview" show-center-play-btn="true" src="https://img.cdn.aliyun.dcloud.net.cn/guide/uniapp/%E7%AC%AC1%E8%AE%B2%EF%BC%88uni-app%E4%BA%A7%E5%93%81%E4%BB%8B%E7%BB%8D%EF%BC%89-%20DCloud%E5%AE%98%E6%96%B9%E8%A7%86%E9%A2%91%E6%95%99%E7%A8%8B@20200317.mp4"/>
		
		<view class="like-container">
			<image class="like-icon" src="../../static/tabbar/tab-cart-current.png"/>
			<text class="like-count">{{like}}</text>
		</view>
		
		<text class="tag-container">{{createTagString(tags)}}</text>
		
		<text class="description">{{desc}}</text>
		
		<view class="line"></view>
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
				type: Number,
				default: "未知"
			},
			// 视频预览图
			preview: {
				type: String
			},
			// 视频时长
			duration: {
				type: Number
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
		},
		methods: {
			createTagString: function(tags) {
				return tags.join(" ")
			},
			
			createUploadTimeString(ms) {
				let date = new Date(ms)
				return (date.getMonth() + 1) + "-" + date.getDate() + " " + date.getHours() + ":" + date.getMinutes()
			}
		}
	}
</script>

<style>
	.container {
		display: flex;
		flex-direction: column;
		justify-content: flex-start;
		align-items: flex-start;
		width: 100%;
		height: 630rpx;
		margin-top: 10rpx;
		background-color: #FFFFFF;
	}
	
	.family-box {
		display: flex;
		flex-direction: row;
		justify-content: flex-start;
		align-items: center;
		width: 100%;
		height: 60rpx;
	}
	
	.family-avatar {
		width: 40rpx;
		height: 40rpx;
		margin-left: 20rpx;
		border-radius: 20rpx;
	}
	
	.family-name {
		font-size: 20rpx;
		margin-left: 10rpx;
	}
	
	.upload-time {
		width: 98%;
		position: absolute;
		text-align: right;
		font-size: 20rpx;
		color: #808080;
	}
	
	.video-preview {
		width: 100%;
		height: 400rpx;
		background-color: #555555;
	}
	
	.like-container {
		width: 100%;
		height: 40rpx;
		margin-top: 20rpx;
		display: flex;
		flex-direction: row;
		justify-content: flex-start;
		align-items: center;
	}
	
	.like-icon {
		width: 40rpx;
		height: 40rpx;
		margin-left: 20rpx;
	}
	
	.like-count {
		font-size: 16rpx;
		margin-left: 10rpx;
	}
	
	.tag-container {
		font-size: 24rpx;
		color: #000000;
		margin-top: 10rpx;
		margin-left: 20rpx;
		font-weight: 600;
	}
	
	.description {
		font-size: 8rpx;
		color: #8F8F94;
		margin-left: 20rpx;
	}
	
	.line {
		width: 92%;
		height: 2rpx;
		background-color: #007AFF;
		margin-top: 30rpx;
		margin-left: 4%;
	}
</style>
