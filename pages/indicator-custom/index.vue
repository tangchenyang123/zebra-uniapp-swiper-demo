<template>
	<view class="demo-swiper">
		<demo-block title="自定义">
			<z-swiper @change="onChange" :show-indicators="false">
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
				<template #indicator>
					<view class="custom-indicator">{{ current + 1 }}/5</view>
				</template>
			</z-swiper>
			<z-swiper @change="onChange1" :show-indicators="false" ref="zSwiper">
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
				<template #indicator>
					<view class="custom-indicator-list">
						<view
							:class="['custom-indicator-list-item',index == current1?'custom-indicator-list-item-active':'']"
							v-for="(item,index) in 5" :key="index" @click="changSwiper(index)">
							{{index+1}}
						</view>
					</view>
				</template>
			</z-swiper>
			<z-swiper @change="onChange2" :show-indicators="false">
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
				<template #indicator>
					<view class="custom-indicator-list1">
						<view
							:class="['custom-indicator-list-item1',index == current2?'custom-indicator-list-item1-active':'']"
							v-for="(item,index) in 5" :key="index">
						</view>
					</view>
				</template>
			</z-swiper>
			<z-swiper @change="onChange3" :show-indicators="false">
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
				<template #indicator>
					<view class="custom-indicator-list2">
						<template v-for="(item,index) in 5">
							<view :key="index" v-if="index == current3 - 2"
								class="custom-indicator-list2-bullet custom-indicator-list2-bullet-prev-prev">

							</view>
							<view :key="index" v-else-if="index == current3 - 1"
								class="custom-indicator-list2-bullet custom-indicator-list2-bullet-prev">

							</view>
							<view :key="index" v-else-if="index == current3"
								class="custom-indicator-list2-bullet custom-indicator-list2-bullet-active">

							</view>
							<view :key="index" v-else-if="index == current3 + 1"
								class="custom-indicator-list2-bullet custom-indicator-list2-bullet-next">

							</view>
							<view :key="index" v-else-if="index == current3 + 2"
								class="custom-indicator-list2-bullet custom-indicator-list2-bullet-next-next">

							</view>
						</template>
					</view>
				</template>
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
		data() {
			return {
				current: 0,
				current1: 0,
				current2: 0,
				current3: 0
			}
		},
		methods: {
			onChange(index) {
				this.current = index;
			},
			onChange1(index) {
				this.current1 = index;
			},
			onChange2(index) {
				this.current2 = index;
			},
			onChange3(index) {
				this.current3 = index;
			},
			changSwiper(index) {
				if (index != this.current1) {
					this.$refs.zSwiper.swipeTo(index);
				}
			},
		}
	}
</script>

<style scoped lang="scss">
	.demo-swiper {
		.image {
			height: 300rpx;
			width: 100%;
		}

		.custom-indicator {
			position: absolute;
			right: 30rpx;
			bottom: 30rpx;
			padding: 4rpx 10rpx;
			font-size: 24rpx;
			color: #FFFFFF;
			background: rgba(0, 0, 0, 0.1);
		}

		.custom-indicator-list {
			position: absolute;
			bottom: 30rpx;
			left: 0;
			width: 100%;
			display: flex;
			align-items: center;
			justify-content: center;

			.custom-indicator-list-item {
				width: 40rpx;
				height: 40rpx;
				text-align: center;
				line-height: 40rpx;
				font-size: 24rpx;
				color: #000;
				opacity: 1;
				background: rgba(0, 0, 0, 0.2);
				border-radius: 50%;
				margin: 0 8rpx;

				&-active {
					color: #fff;
					background: #007aff;
				}
			}
		}

		.custom-indicator-list1 {
			position: absolute;
			bottom: 30rpx;
			left: 0;
			width: 100%;
			display: flex;
			align-items: center;
			justify-content: center;

			.custom-indicator-list-item1 {
				margin: 0 5rpx;
				background-color: #e8f5ff;
				width: 20rpx;
				height: 10rpx;
				opacity: 1;
				border-radius: 5rpx;
				transition: opacity .3s, background-color .3s, width .3s;

				&-active {
					background-color: #3eb2f3;
					width: 35rpx;
				}
			}
		}

		.custom-indicator-list2 {
			position: absolute;
			bottom: 30rpx;
			left: 0;
			width: 100%;
			display: flex;
			align-items: center;
			justify-content: center;

			.custom-indicator-list2-bullet {
				margin: 0 8rpx;
				position: relative;
				width: 16rpx;
				height: 16rpx;
				border-radius: 50%;
				background-color: #e8f5ff;
				opacity: 1;
				transition: .2s width, .2s height, .2s background-color, .2s opacity, .2s transform;

				&-active {
					transform: scale(1);
					opacity: 1;
					background-color: #3eb2f3;
				}

				&-prev {
					transform: scale(.66);
				}

				&-prev-prev {
					transform: scale(.33);
				}

				&-next {
					transform: scale(.66);
				}

				&-next-next {
					transform: scale(.33);
				}
			}
		}
	}
</style>
