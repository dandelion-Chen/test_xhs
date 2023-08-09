<template>
	<view class="content">
		<web-view
            src="https://t60.fat.klook.io/testXhsWebView"
            @message="getMessage"
        ></web-view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		onShareAppMessage() {
			uni.showModal({
				content: "onShareAppMessage"
			})
		},
		methods: {
			getMessage() {
				uni.showModal({
					content: "getMessage"
				})
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
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin: 200rpx auto 50rpx auto;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
