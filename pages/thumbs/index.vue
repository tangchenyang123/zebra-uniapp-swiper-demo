<template>
	<view class="demo-swiper">
		<demo-block title="基础用法">
			<z-swiper v-if="swiperThumbsReady" ref="zSwiper" :options="options">
				<z-swiper-item v-for="(item,index) in list" :key="index">
					<image class="image" :src="item" mode="aspectFill">
					</image>
				</z-swiper-item>
			</z-swiper>
			<z-swiper ref="zSwiperThumbs" :options="optionsThumbs">
				<z-swiper-item v-for="(item,index) in list" :key="index">
					<image class="thumbImage" :src="item" mode="aspectFill">
					</image>
				</z-swiper-item>
			</z-swiper>
		</demo-block>
		<demo-block title="自动播放">
			<z-swiper v-if="swiperThumbsAutoplayReady" ref="zSwiperAuto" :options="optionsAuto">
				<z-swiper-item v-for="(item,index) in list" :key="index">
					<image class="image" :src="item" mode="aspectFill">
					</image>
				</z-swiper-item>
			</z-swiper>
			<z-swiper ref="zSwiperThumbsAuto" :options="optionsThumbsAuto">
				<z-swiper-item v-for="(item,index) in list" :key="index">
					<image class="thumbImage" :src="item" mode="aspectFill">
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
		data() {
			return {
				optionsThumbs: {
					spaceBetween: 10,
					slidesPerView: 4,
					freeMode: true,
					watchSlidesProgress: true,
					thumbs: {
						use: true
					}
				},
				options: {
					spaceBetween: 10,
					thumbs: {
						swiper: true
					}
				},
				optionsThumbsAuto: {
					spaceBetween: 10,
					slidesPerView: 4,
					freeMode: true,
					watchSlidesProgress: true,
					thumbs: {
						use: true
					}
				},
				optionsAuto: {
					spaceBetween: 10,
					thumbs: {
						swiper: true
					},
					autoplay: true
				},
				list: [
					'https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe1.jpg',
					'https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe2.jpg',
					'https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe3.jpg',
					'https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe4.jpg',
					'https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe5.jpg',
				],
				swiperThumbsReady: false,
				swiperThumbsAutoplayReady: false
			}
		},
		onReady() {
			this.$refs.zSwiperThumbs.setSwiperOn("init", (swiperThumbs) => {
				this.swiperThumbsReady = true;
				setTimeout(() => {
					this.$refs.zSwiper.setSwiperOn("_swiper", (swiper) => {
						swiper.params.thumbs.swiper = swiperThumbs;
					})
				}, 0)
			});
			this.$refs.zSwiperThumbsAuto.setSwiperOn("init", (swiperThumbs) => {
				this.swiperThumbsAutoplayReady = true;
				setTimeout(() => {
					this.$refs.zSwiperAuto.setSwiperOn("_swiper", (swiper) => {
						swiper.params.thumbs.swiper = swiperThumbs;
					})
				}, 0)
			});
		}
	}
</script>

<style scoped lang="scss">
	.demo-swiper {
		.image {
			height: 300rpx;
			width: 100%;
		}

		.thumbImage {
			height: 150rpx;
			width: 100%;
		}
	}
</style>
