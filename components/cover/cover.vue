<template>
	<view>
		<view  class="view-body">
			<!-- 每一个视频 -->
			<view class="view-body-item">
				<!-- 视频封面 -->
				<image mode="aspectFill" class="cover"  :src="videoitem.video_cover"></image>
				<!-- 视频详情（作者 发布时间 标题） -->
				<view class="view-body-item-message">
					<!-- 作者头像 -->
					<!-- 在电影模块中不需要 -->
					<image class="user" mode="aspectFit" :src="videoitem.user.user_imgurl"></image>
					<!-- 作品标题  作者名  发布时间 -->
					<!-- 在电影模块中不需要作者名称和发布时间 -->
					<view class="text">
						<text class="title">{{videoitem.video_title}}</text>
							<view class="author">
								<text class="author-name">{{videoitem.user.user_name}}</text>
								<text class="author-time">{{videoitem.video_time}}</text>
							</view>
					</view>
				</view>
			</view>
		
		</view>
	</view>
</template>

<script>
	export default {
		name:"cover",
		props:['videoitem'],
		data() {
			return {
				
			};
		},
		mounted() {
			// setTimeout(()=>{console.log(this.videoitem);},2000)
		
		}
	}
</script>

<style lang="scss">
	.view-body{
		// display: flex;
		padding: 20rpx 0 20rpx 40rpx;
		// 每一个视频包含封面和详情
		.view-body-item{

			// 视频封面
			.cover{
				border-radius: 4%;
				width: 540rpx;
				height: 400rpx;
				// padding-right: 40rpx;
			}
			// 视频详情
			.view-body-item-message{
				display: flex;
				// 头像
				.user{
					width: 100rpx;
					height: 100rpx;
					border-radius: 50%;
				}
			
			}
		}
	
	
	}
	
</style>