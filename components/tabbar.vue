<template>
	<view class="tabbar">
		<view class="active-task-ball">
			<view class="inner-ball">
				<image src="/static/task.png"></image>
				<view>当前</view>
			</view>
		</view>
		<view class="item">
			<image v-if="active=='hall'" class="icon" src="/static/hall-active.png"></image>
			<image v-else class="icon" src="/static/hall.png"></image>
			<view class="title" :class="{active: active=='hall'}">大厅</view>
		</view>
		<view class="active-task"></view>
		<view class="item" :class="{active: active=='my'}">
			<image v-if="active=='my'" class="icon" src="/static/my-active.png"></image>
			<image v-else class="icon" src="/static/my.png"></image>
			<view class="title" :class="{active: active=='my'}">我的</view>
		</view>
	</view>

</template>

<script>
	export default {
		data() {
			return {

			};
		},
		props: ["active"]
	}
</script>

<style lang="less" scoped>
	.tabbar {
		width: 100%;
		height: 98upx;
		justify-content: center;
		align-items: flex-end;
		background: #fff;
		box-shadow: 0upx 0upx 37upx 3upx rgba(32, 37, 40, 0.15);
		color: rgba(177, 182, 186, 1);
		margin-top: 13upx;

		.item {
			flex: 1;
			flex-direction: column;
			height: 98upx;
			z-index: 999;



			.icon {
				margin: auto;
				width: 40upx;
				height: 40upx;
			}

			.title {
				margin: auto;
				font-size: 22upx;

				height: 40upx;
				font-family: PingFang-SC-Medium;
				font-weight: 500;
			}
		}

		.active {
			color: rgba(255, 84, 88, 1);
		}

		.active-task {
			min-width: 98upx;
		}

	}

	.active-task-ball {
		position: fixed;
		width: 140upx;
		height: 140upx;
		min-width: 140upx;
		min-height: 140upx;
		background: rgba(255, 255, 255, 1);
		box-shadow: 0upx 0upx 37upx 3upx rgba(32, 37, 40, 0.15);
		border-radius: 50%;
		margin: auto;
		bottom: 12upx;

		.inner-ball {
			width: 120upx;
			height: 120upx;
			background: rgba(255, 84, 88, 1);
			border-radius: 50%;
			margin: auto;
			flex-direction: column;
			color: #fff;
			
			
			image {
				width: 44upx;
				height: 44upx;
				margin:23upx auto 0upx auto;
			}
			view {
				font-size: 22upx;
				font-family: PingFang-SC-Medium;
				font-weight: 500;
				height: 40upx;
				margin: 13upx auto;
			}
		}
	}
</style>
