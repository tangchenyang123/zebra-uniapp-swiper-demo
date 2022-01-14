<template>
	<view class="demo-swiper">
		<demo-block title="切换效果-3D流">
			<view class="demo-swiper-coverflow">
				<z-swiper effect="coverflow" :loop="false" :showIndicators="false" customStyle="height:400rpx;"
					:width="200">
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
			<view class="demo-swiper-coverflow">
				<z-swiper effect="coverflow" autoplay="2000" :loop="false" :showIndicators="false"
					customStyle="height:400rpx;" :width="200">
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
			<view class="demo-swiper-coverflow">
				<z-swiper effect="coverflow" vertical :loop="false" :showIndicators="false" customStyle="height:600rpx;"
					:height="200">
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
		.image {
			height: 400rpx;
			width: 100%;
		}
	}
</style>
