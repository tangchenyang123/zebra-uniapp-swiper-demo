<template>
	<view class="demo-swiper">
		<demo-block title="切换效果-淡入">
			<z-swiper effect="fade" :loop="false" :showIndicators="false">
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
		</demo-block>
		<demo-block title="自动播放">
			<z-swiper effect="fade" :loop="false" autoplay="2000" :showIndicators="false">
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
		</demo-block>
		<demo-block title="纵向">
			<z-swiper effect="fade" :loop="false" vertical :showIndicators="false" customStyle="height: 300rpx;">
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
			height: 300rpx;
			width: 100%;
		}
	}
</style>
