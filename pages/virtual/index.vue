<template>
	<view class="demo-swiper">
		<demo-block title="基础用法">
			<z-swiper ref="zSwiper" v-model="list" :options="options">
				<z-swiper-item v-for="(item,index) in list" :key="index">
					<!-- <image class="image" :src="item" mode="aspectFill">
					</image> -->
					<!-- <view class="image" :style=""> -->
					<image class="image" :src="item.url" mode="aspectFill">
					</image>
					<!-- {{item.url}} -->
					<!-- </view> -->
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
		data() {
			return {
				options: {
					virtual: {
						slides: [],
						addSlidesBefore: 1,
						addSlidesAfter: 1,
					},
				},
				list: []
			}
		},
		mounted() {
			let list = [];
			// for (var i = 0; i < 100; i += 1) {
				for (var j = 0; j < 8; j++) {
					list.push({
						show: false,
						url: `https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe${j+1}.jpg`
					})
				}
			// }
			this.options.virtual.slides = [...list];
			// this.list = [...list];
		}
	}
</script>

<style scoped lang="scss">
	.demo-swiper {
		.image {
			width: 100%;
			height: 300rpx;
			z-index: 100;
			will-change: left, transform;
		}
	}
</style>
