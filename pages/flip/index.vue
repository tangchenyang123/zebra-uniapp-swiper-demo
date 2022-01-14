<template>
	<view class="demo-swiper">
		<demo-block title="切换效果-3D翻转">
			<view class="demo-swiper-flip">
				<z-swiper effect="flip" :loop="false" :showIndicators="false" customStyle="height:400rpx;width:400rpx;">
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
		<demo-block title="自动切换">
			<view class="demo-swiper-flip">
				<z-swiper effect="flip" autoplay="2000" :loop="false" :showIndicators="false"
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
			<view class="demo-swiper-flip">
				<z-swiper effect="flip" vertical :loop="false" :showIndicators="false"
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
		}
	}
</script>

<style scoped lang="scss">
	.demo-swiper {
		.image {
			height: 400rpx;
			width: 100%;
		}

		.demo-swiper-flip {
			height: 400rpx;
			width: 600rpx;
			display: flex;
			align-items: center;
			justify-content: center;
		}
	}
</style>
