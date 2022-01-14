<template>
	<view class="demo-swiper">
		<demo-block title="切换效果-卡片式">
			<view class="demo-swiper-cards">
				<z-swiper effect="cards" :loop="false" :showIndicators="false"
					customStyle="height:640rpx;width:480rpx;">
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
			<view class="demo-swiper-cards">
				<z-swiper effect="cards" autoplay="2000" :loop="false" :showIndicators="false"
					customStyle="height:640rpx;width:480rpx;">
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
			<view class="demo-swiper-cards">
				<z-swiper effect="cards" vertical :loop="false" :showIndicators="false"
					customStyle="height:640rpx;width:480rpx;">
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
			height: 640rpx;
			width: 100%;
			border-radius: 12rpx;
		}

		.demo-swiper-cards {
			height: 700rpx;
			width: 100%;
			display: flex;
			align-items: center;
			justify-content: center;
		}
	}
</style>
