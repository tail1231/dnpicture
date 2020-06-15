<template>
	<view class="idea-page">
		<view class="idea-list">
			<block v-for="(item,index) in ideaList" :key='index'>
				<view class="idea-item">
					<view class="idea-hd" :style="{backgroundColor:item.theme}">
						<view class="left">
							<view class="lhd">
								<view class="title">{{item.title}}</view>
								<view class="desc">{{item.desc}}</view>
							</view>
							<view class="lbd">
								<image src="../../static/images/book.png" mode=""></image> <text>{{item.type}}</text>
							</view>
						</view>
						<view class="right">
							<image :src="item.imgUrl" mode=""></image>
						</view>
					</view>
					<view class="idea-bd">
						<view class="idea-num">新意指数：{{item.ideaNum}}</view>
						<view class="down-btn" :style="{backgroundColor:item.theme}">下载素材</view>
					</view>
				</view>
			</block>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				ideaList: [{
						id: 1,
						type: '创意锁屏',
						title: '改变锁屏的手电筒和相机',
						desc: '他可以将锁屏灯和相机按钮变成一个大灯笼和经典相机，看起来特别好玩。',
						imgUrl: "../../static/images/item1.jpg",
						ideaNum: 99, //新意指数
						theme: '#DEB05A'
					},
					{
						id: 2,
						type: '捷径',
						title: '3D Touch 电子秤',
						desc: '可以快速利用屏幕检测物体的重量哈，放个苹果试一试喽~',
						imgUrl: "../../static/images/item2.jpg",
						ideaNum: 89, //新意指数
						theme: '#AC89CB'
					},
					{
						id: 3,
						type: '跑马灯壁纸',
						title: '超级炫酷的跑马灯锁屏',
						desc: '设置到手机上有一种蹦迪的感觉呐！',
						imgUrl: "../../static/images/item3.jpg",
						ideaNum: 99, //新意指数
						theme: '#DC858B'
					},
					{
						id: 4,
						type: '口罩',
						title: '给头像加口罩',
						desc: '疫情期间，人人戴口罩，快给自己的头像加个口罩吧',
						imgUrl: "../../static/images/item4.jpg",
						ideaNum: 99, //新意指数
						theme: '#DEB05A'
					},
					{
						id: 5,
						type: '时间',
						title: '时间进度',
						desc: '直观看到自己生命所剩余的百分比，今年的百分比等信息，促进你养成珍惜时间的好习惯~',
						imgUrl: "../../static/images/item5.jpg",
						ideaNum: 99, //新意指数
						theme: '#AC89CB'
					}
				]
			}
		}
	}
</script>

<style lang="scss">
	page {
		width: 100%;
		height: 100%;
		background-color: #f1f1f1;
		padding: 20rpx 30rpx;
	}

	.idea-page {
		.idea-list {
			.idea-item {
				margin-bottom: 40rpx;
				.idea-hd {
					display: flex;
					justify-content: space-between;
					padding: 20rpx;
					color: #fff;
					border-top-left-radius: 16rpx;
					border-top-right-radius: 16rpx;

					.left {
						.lhd {
							margin-bottom: 15rpx;
							.title {
								font-size: 30rpx;
							}

							.desc {
								margin-top: 8rpx;
								font-size: 24rpx;
								width: 420rpx;
								line-height: 40rpx;
							}
						}

						.lbd {
							display: flex;
							align-items: center;
							height: 60rpx;
							width: 210rpx;
							padding-left: 10rpx;
							background: linear-gradient(to left, rgba(102, 255, 230,0), rgba(115, 211, 255, 1)); /* 标准的语法（必须放在最后） */
							
							image {
								margin-right: 10rpx;
								width: 40rpx;
								height: 40rpx;
							}
							text {
								font-size: 24rpx;
							}
						}
					}

					.right {
						width: 160rpx;
						height: 160rpx;

						image {
							display: block;
							width: 100%;
							height: 100%;
						}
					}
				}
				.idea-bd {
					display: flex;
					justify-content: space-between;
					align-items: center;
					background-color: #fff;
					padding: 25rpx;
					border-bottom-left-radius: 16rpx;
					border-bottom-right-radius: 16rpx;
					.idea-num {
						
					}
					.down-btn {
						color: #fff;
						height: 60rpx;
						line-height: 60rpx;
						width: 140rpx;
						border-radius: 8rpx;
						text-align: center;
					}
				}
			}
		}
	}
</style>
