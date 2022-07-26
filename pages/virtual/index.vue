<template>
	<view class="demo-swiper">
		<demo-block title="基础用法">
			<z-swiper ref="zSwiper" v-model="list" :options="options">
				<z-swiper-item v-for="(item,index) in list" :key="index">
					<image class="image" :src="item.url" mode="aspectFill">
					</image>
					<!-- <video :enable-progress-gesture="false" class="image" :src="item.url">
					</video> -->
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
						addSlidesBefore: 1,
						addSlidesAfter: 1,
						slides: []
					},
				},
				list: []
			}
		},
		mounted() {
			let list = [];
			for (var i = 0; i < 100; i += 1) {
				// for (var j = 0; j < 3; j++) {
				// 	list.push({
				// 		show: false,
				// 		url: `https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe${j+1}.jpg`,
				// 		// url: `https://cdn.zebraui.com/zebra-swiper/demos/video/video${j+1}`,
				// 		id: i + j + ""
				// 	})
				// }
				list.push({
					show: false,
					url: `https://picsum.photos/200/300?id=${i}`,
					// url: `https://cdn.zebraui.com/zebra-swiper/demos/video/video${j+1}`,
					id: i
				})
				// }
			}
			this.options.virtual.slides = [...list];
		}
	}
</script>

<style scoped lang="scss">
	.demo-swiper {
		image {
			will-change: transform
		}

		.image {
			width: 100%;
			height: 300rpx;
		}
	}
</style>
