<template>
	<view class="demo-swiper">
		<demo-block title="基础用法">
			<z-swiper>
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
		<demo-block title="自定义颜色">
			<z-swiper indicator-color="white">
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
		},
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
