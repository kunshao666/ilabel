<template>
	<view class="page">
		<view class="top-panel">
			<view class="publisher">
				<image class="avatar" src="../../static/logo.png"></image>
				<view class="desc">
					<view class="nickname">王二胖</view>
					<view class="company">天津卓朗科技发展有限公司</view>
				</view>
			</view>
			<view class="task-title">标注一篇文章是否是政策</view>
		</view>
		<view class="task-stat">
			<view class="stat">
				<view class="value">999</view>
				<view class="label">参与人数</view>
			</view>
			<view class="stat">
				<view class="value">79%</view>
				<view class="label">任务进度</view>
			</view>
			<view class="avatars">
				<image class="avatar" src="../../static/logo.png"></image>
				<image class="avatar" src="../../static/logo.png"></image>
				<image class="avatar" src="../../static/logo.png"></image>
			</view>
		</view>
		<view class="task-desc">

			通过阅读文章的标题和正文来标注一篇文章是否是政策，目标分类一共有三类 ：
			1. 是政策
			2. 非政策
			3. 不确定

			通过下面的样本图片来学习一下标注标准。

		</view>
		<view class="task-images"></view>
		<view class="button">开始标注</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			};
		}
	}
</script>

<style lang="less" scoped>
	.top-panel {
		width: 100%;
		height: 338upx;
		background: #FF5458;
		color: #fff;
		position: fixed;
		top: 0upx;
		flex-direction: column;

		.publisher {
			margin: 30upx;

			.avatar {
				width: 100upx;
				height: 100upx;
				border-radius: 50%;
			}

			.desc {
				flex-direction: column;
				margin: 0upx 25upx;

				.nickname {
					font-size: 30upx;
					font-family: PingFang-SC-Bold;
					font-weight: bold;
				}

				.company {
					margin-top: 12upx;
					font-size: 24upx;
					font-family: PingFang-SC-Regular;
					font-weight: 400;
				}
			}
		}

		.task-title {
			margin: 10upx 30upx;
			font-size: 32upx;
			font-family: PingFang-SC-Bold;
			font-weight: bold;
			color: rgba(255, 255, 255, 1);
		}


	}

	.top-panel:after {
		content: "";
		width: 100%;
		height: 80upx;
		background: #FF5458;
		color: #fff;
		position: fixed;
		top: 298upx;
		border-radius: 50%;
	}

	.box {
		width: 690upx;
		background: #fff;
		box-shadow: 0upx 6upx 24upx 0upx rgba(0, 0, 0, 0.06);
		border-radius: 20upx;
		z-index: 999;
		margin: 12upx auto;
	}

	.task-stat {
		.box;
		height: 220upx;
		margin-top: 256upx;
		padding: 69upx 75upx;
		justify-content: space-between;

		.stat {
			flex-direction: column;
			width: 110upx;
			height: 80upx;

			.value {
				font-size: 46upx;
				font-family: CenturyGothic;
				font-weight: 400;
				color: rgba(255, 84, 88, 1);
				justify-content: center;
			}

			.label {
				font-size: 24upx;
				font-family: PingFang-SC-Medium;
				font-weight: 500;
				color: rgba(177, 182, 186, 1);
				margin-top: 24upx;
				justify-content: center;
			}
		}

		.avatars {
			height: 80upx;
			width: 190upx;
			flex-direction: row-reverse;
			padding-left: 25upx;
			
			.avatar {
				width: 80upx;
				height: 80upx;
				border-radius: 50%;
				border: 1upx solid #fff;
				margin-left: -25upx;
			}
		}
	}

	.task-desc {
		.box;
		padding: 40upx;
		text-align: justify;
		font-size: 24upx;
		font-family: PingFang-SC-Medium;
		font-weight: 500;
		color: rgba(51, 51, 51, 1);
	}

	.task-images {
		.box;
		flex: 1;
	}

	.button {
		width: 100%;
		height: 98upx;
		background: #FF5458;
		font-size: 30upx;
		font-family: PingFang-SC-Medium;
		font-weight: 500;
		color: #fff;
		justify-content: center;
		align-items: center;
	}
</style>
