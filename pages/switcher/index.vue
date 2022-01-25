<template>
	<view class="demo-switcher">
		<demo-block title="基础用法">
			<z-swiper show-prev-button show-next-button>
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
		<demo-block title="插槽自定义">
			<z-swiper show-prev-button-slot show-next-button-slot>
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
				<template #pre-button>
					<view class="custom-switcher">
						prev
					</view>
				</template>
				<template #next-button>
					<view class="custom-switcher">
						next
					</view>
				</template>
			</z-swiper>
		</demo-block>
		<demo-block title="完全自定义">
			<z-swiper ref="zSwiper" :loop="true">
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
			<view class="custom-switcher-group">
				<button type="primary" size="mini" class="custom-switcher-group-button" @click="prev()">prev</button>
				<button type="primary" size="mini" class="custom-switcher-group-button" @click="next()">next</button>
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
		methods: {
			prev() {
				this.$refs.zSwiper.prev();
			},
			next() {
				this.$refs.zSwiper.next();
			}
		}
	}
</script>

<style scoped lang="scss">
	.demo-switcher {
		.image {
			height: 300rpx;
			width: 100%;
		}

		.custom-switcher {
			display: flex;
			align-items: center;
		}

		.custom-switcher-group {
			display: flex;
			align-items: center;
			justify-content: space-around;
		}
	}
</style>
