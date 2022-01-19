<template>
	<view class="demo-swiper">
		<demo-block title="切换效果-方块">
			<view class="demo-swiper-cube">
				<z-swiper effect="cube" :loop="false" :showIndicators="false" customStyle="height:400rpx;width:400rpx;">
					<z-swiper-item>
						<image class="image" src="https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe1.jpg"
							mode="aspectFill">
						</image>
					</z-swiper-item>
					<z-swiper-item>
						<image class="image" src="https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe2.jpg"
							mode="aspectFill">
						</image>
					</z-swiper-item>
					<z-swiper-item>
						<image class="image" src="https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe3.jpg"
							mode="aspectFill">
						</image>
					</z-swiper-item>
					<z-swiper-item>
						<image class="image" src="https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe4.jpg"
							mode="aspectFill">
						</image>
					</z-swiper-item>
					<z-swiper-item>
						<image class="image" src="https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe5.jpg"
							mode="aspectFill">
						</image>
					</z-swiper-item>
				</z-swiper>
			</view>
		</demo-block>
		<demo-block title="阴影">
			<view class="demo-swiper-cube">
				<z-swiper effect="cube" cube-shadow :loop="false" :showIndicators="false"
					customStyle="height:400rpx;width:400rpx;">
					<z-swiper-item>
						<image class="image" src="https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe1.jpg"
							mode="aspectFill">
						</image>
					</z-swiper-item>
					<z-swiper-item>
						<image class="image" src="https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe2.jpg"
							mode="aspectFill">
						</image>
					</z-swiper-item>
					<z-swiper-item>
						<image class="image" src="https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe3.jpg"
							mode="aspectFill">
						</image>
					</z-swiper-item>
					<z-swiper-item>
						<image class="image" src="https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe4.jpg"
							mode="aspectFill">
						</image>
					</z-swiper-item>
					<z-swiper-item>
						<image class="image" src="https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe5.jpg"
							mode="aspectFill">
						</image>
					</z-swiper-item>
				</z-swiper>
			</view>
		</demo-block>
		<demo-block title="自动播放">
			<view class="demo-swiper-cube">
				<z-swiper effect="cube" cube-shadow autoplay="2000" :loop="false" :showIndicators="false"
					customStyle="height:400rpx;width:400rpx;">
					<z-swiper-item>
						<image class="image" src="https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe1.jpg"
							mode="aspectFill">
						</image>
					</z-swiper-item>
					<z-swiper-item>
						<image class="image" src="https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe2.jpg"
							mode="aspectFill">
						</image>
					</z-swiper-item>
					<z-swiper-item>
						<image class="image" src="https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe3.jpg"
							mode="aspectFill">
						</image>
					</z-swiper-item>
					<z-swiper-item>
						<image class="image" src="https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe4.jpg"
							mode="aspectFill">
						</image>
					</z-swiper-item>
					<z-swiper-item>
						<image class="image" src="https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe5.jpg"
							mode="aspectFill">
						</image>
					</z-swiper-item>
				</z-swiper>
			</view>
		</demo-block>
		<demo-block title="纵向">
			<view class="demo-swiper-cube">
				<z-swiper effect="cube" cube-shadow vertical :loop="false" :showIndicators="false"
					customStyle="height:400rpx;width:400rpx;">
					<z-swiper-item>
						<image class="image" src="https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe1.jpg"
							mode="aspectFill">
						</image>
					</z-swiper-item>
					<z-swiper-item>
						<image class="image" src="https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe2.jpg"
							mode="aspectFill">
						</image>
					</z-swiper-item>
					<z-swiper-item>
						<image class="image" src="https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe3.jpg"
							mode="aspectFill">
						</image>
					</z-swiper-item>
					<z-swiper-item>
						<image class="image" src="https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe4.jpg"
							mode="aspectFill">
						</image>
					</z-swiper-item>
					<z-swiper-item>
						<image class="image" src="https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe5.jpg"
							mode="aspectFill">
						</image>
					</z-swiper-item>
				</z-swiper>
			</view>
		</demo-block>
	</view>
</template>

<script>
	import DemoBlock from '../../components/DemoBlock/DemoBlock.vue';
	export default {
		components: {
			DemoBlock
		},
	}
</script>

<style scoped lang="scss">
	.demo-swiper {
		&-cube {
			height: 600rpx;
			width: 600rpx;
			display: flex;
			align-items: center;
			justify-content: center;
			overflow: hidden;
		}

		.image {
			height: 400rpx;
			width: 100%;
		}
	}
</style>
