<template>
	<view class="page">
		<view class="carousal">
			<image src="../../static/logo.png"></image>
		</view>
		<view class="tabs">
			<view class="tab" :class="{current: currentTaskStatus=='INPROGRESS'}" @tap="currentTaskStatus='INPROGRESS'">
				<view class="title">进行中</view>
				<view class="underline" v-if="currentTaskStatus=='INPROGRESS'"></view>
			</view>
			<view class="tab" :class="{current: currentTaskStatus=='COMIING'}" @tap="currentTaskStatus='COMIING'">
				<view class="title">即将上架</view>
				<view class="underline" v-if="currentTaskStatus=='COMIING'"></view>
			</view>
			<view class="tab" :class="{current: currentTaskStatus=='COMPLETE'}" @tap="currentTaskStatus='COMPLETE'">
				<view class="title">已结束</view>
				<view class="underline" v-if="currentTaskStatus=='COMPLETE'"></view>
			</view>
		</view>
		<view class="task-list">
			<view class="task" v-for="(t, i) in tasks" :key="i" @tap="gotoTask(t)">
				<image class="logo" src="../../static/logo.png"></image>
				<view class="task-desc">
					<view class="title">{{t.title}}</view>
					<view class="labels">
						<view class="label">100</view>
						<view class="label">文本</view>
					</view>
					<view class="progress-bar">
						<view class="progress" :style="'width:' + t.progress"></view>
					</view>
				</view>
				<view class="button">领取</view>
			</view>
		</view>
		<tabbar active="hall"></tabbar>
	</view>
</template>

<script>
	import tabbar from "../../components/tabbar.vue"
	export default {
		data() {
			return {
				title: 'Hello',
				currentTaskStatus: "INPROGRESS",
				tasks: [{
						logo: "",
						title: "标注一篇文本是否是政策1标注一篇文本是否是政策1标注一篇文本是否是政策1",
						labels: [],
						progress: "33%"
					},
					{
						logo: "",
						title: "标注一篇文本是否是政策2",
						labels: [],
						progress: "45%"
					}, {
						logo: "",
						title: "标注一篇文本是否是政策2",
						labels: [],
						progress: "45%"
					}, {
						logo: "",
						title: "标注一篇文本是否是政策2",
						labels: [],
						progress: "45%"
					}, {
						logo: "",
						title: "标注一篇文本是否是政策2",
						labels: [],
						progress: "45%"
					}, {
						logo: "",
						title: "标注一篇文本是否是政策2",
						labels: [],
						progress: "45%"
					}, {
						logo: "",
						title: "标注一篇文本是否是政策2",
						labels: [],
						progress: "45%"
					}
				]
			}
		},
		components: {
			tabbar
		},
		onLoad() {

		},
		methods: {
			gotoTask(task) {
				uni.navigateTo({
					url:"/pages/task/index"
				})
			}
		}
	}
</script>

<style lang="less" scoped>
	.font-medium {
		font-family: PingFang-SC-Medium;
		font-weight: 500;
	}

	.page {
		justify-content: flex-end;
	}

	.carousal {
		width: 100%;
		height: 360upx;

		image {
			width: 100%;
			height: 100%;
		}
	}

	.tabs {
		width: 100%;
		height: 122upx;
		padding-left: 59upx;

		.tab {
			height: 57upx;
			font-size: 28upx;
			color: rgba(180, 183, 185, 1);
			margin: auto 62upx auto 0upx;
			flex-direction: column;
			.font-medium;

			.title {
				align-items: flex-end;
				margin-bottom: 19upx;
			}

			.underline {
				width: 40upx;
				height: 6upx;
				background: rgba(255, 84, 88, 1);
				border-radius: 3upx;
				margin: auto;
			}
		}

		.current {
			font-size: 34upx;
			font-family: PingFang-SC-Heavy;
			font-weight: 800;
			color: rgba(51, 51, 51, 1);
		}
	}

	.task-list {
		flex: 1;
		flex-direction: column;
		overflow-y: scroll;

		.task {
			background: #fff;
			width: 690upx;
			min-height: 180upx;
			box-shadow: 0upx 6upx 24upx 0upx rgba(0, 0, 0, 0.06);
			border-radius: 20upx;
			margin-bottom: 24upx;
			padding: 30upx;

			.logo {
				width: 120upx;
				height: 120upx;
				border-radius: 10upx;
				margin-right: 30upx;
			}

			.task-desc {
				flex: 1;
				flex-direction: column;

				.title {
					width: 360upx;
					;
					font-size: 28upx;
					.font-medium;
					color: rgba(51, 51, 51, 1);
					height: 36upx;
					align-items: center;
					overflow: hidden;
					text-overflow: ellipsis;
					white-space: nowrap;
					display: block;

				}

				.labels {
					font-size: 24upx;
					.font-medium;
					color: rgba(198, 202, 206, 1);
					flex: 1;

					.label {
						height: 36upx;
						margin: auto 10upx auto 0upx;
					}
				}

				.progress-bar {
					width: 360upx;
					height: 6upx;
					background: rgba(233, 236, 238, 1);
					border-radius: 3upx;

					.progress {
						width: 275upx;
						height: 6upx;
						background: rgba(255, 84, 88, 1);
						border-radius: 3upx;
					}
				}
			}

			.button {
				width: 90upx;
				font-size: 30upx;
				.font-medium;
				color: rgba(255, 84, 88, 1);
				margin: auto;
			}
		}

		margin: 0px auto;
	}

	
</style>
