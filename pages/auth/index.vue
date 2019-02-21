<template>
	<view class="page">
		<open-data type="userAvatarUrl" class="avatar"></open-data>
		<open-data class="nickname" type="userNickName"></open-data>
		<button open-type="getUserInfo" class="button">前往爱标注</button>
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
	.page {
		background: #fff;
		* {
			display: flex;
		}
	}
	.avatar {
		width: 140upx;
		height: 140upx;
		border-radius: 50%;
		overflow: hidden;
		margin: 405upx auto 42upx auto;
	}

	.nickname {
		height: 34upx;
		font-size: 34upx;
		font-family: PingFang-SC-Heavy;
		font-weight: 800;
		color: rgba(51, 51, 51, 1);
		margin: 0upx auto;
	}

	.button {
		width: 690upx;
		height: 88upx;
		background: rgba(9, 187, 7, 1);
		border: 1upx solid rgba(2, 148, 0, 1);
		border-radius: 10upx;
		margin: 130upx auto 0upx auto;
		font-size: 34upx;
		font-family: PingFang-SC-Bold;
		font-weight: bold;
		color: rgba(255, 255, 255, 1);
		justify-content: center;
		align-items: center;
	}
</style>
