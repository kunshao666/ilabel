<script>
	export default {
		onLaunch: function () {
			console.log('App Launch')
		},
		onShow: function () {
			console.log('App Show')
		},
		onHide: function () {
			console.log('App Hide')
		}
	}
</script>

<style>
	/*每个页面公共css */
	view {
		box-sizing: border-box;
		display: flex;
	}
	.page {
		width: 750upx;
		height: 100%;
		background: #F6F7F9;
		flex-direction: column;
		position: fixed;
		top: 0px;
		bottom: 0px;
	}
</style>
