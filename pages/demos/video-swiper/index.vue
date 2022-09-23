<template>
	<view class="swiper-video">
		<z-swiper ref="zSwiper" v-model="videoList" :options="options" :custom-style="{height:'100%'}"
			@beforeInit="init">
			<z-swiper-item v-for="(item,index) in videoList" :key="index" :custom-style="{height:'100%'}">
				<view class="video-item" @click="videoClick(index)">
					<video :id="item.id" class="video-item-content" :src="item.url" :controls="controls" loop></video>
				</view>
			</z-swiper-item>
		</z-swiper>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				controls: false,
				videoList: [],
				videoContentList: [],
				number: 0,
				options: {
					direction: "vertical",
					// cssMode: true,
					virtual: {
						slides: []
					},
				},
				pageIndex: 1,
				pageSize: 10
			}
		},
		mounted() {
			uni.showModal({
				title: '提示',
				content: '开始',
				showCancel: false,
				success: (res) => {
					if (res.confirm) {
						this.play(0);
					}
				}
			});
		},
		onReady: function(res) {
			this.getVideoList(this.number);
		},
		methods: {
			getVideoList(number) {
				for (var i = 0 + number; i < 10 + number; i++) {
					this.options.virtual.slides.push({
						id: `video${i}`,
						url: `https://cdn.zebraui.com/zebra-swiper/demos/video/video${i+1-number}`,
						isPlay: false,
						isStop: false
					})
					this.videoContentList.push(uni.createVideoContext(`video${i}`))
				}
			},
			init() {
				this.$refs.zSwiper.swiper.on("slideNextTransitionStart", (swiper) => {
					console.log(swiper)
					this.pause(swiper.activeIndex - 1);
					this.play(swiper.activeIndex);
				})
				this.$refs.zSwiper.swiper.on("slidePrevTransitionStart", (swiper) => {
					this.pause(swiper.activeIndex + 1);
					this.play(swiper.activeIndex);
				})
				this.$refs.zSwiper.swiper.on("slideChange", (swiper) => {
					if (swiper.activeIndex == this.number + 8) {
						this.number += 10;
						this.getVideoList(this.number);
					}
				})
			},
			play(index) {
				this.videoList[index].isPlay = true;
				this.videoList[index].isStop = false;
				this.videoContentList[index].play();
			},
			pause(index) {
				console.log("下标", this.videoList, this.videoContentList, index)
				this.videoList[index].isPlay = false;
				this.videoList[index].isStop = true;
				this.videoContentList[index].pause();
			},
			videoClick(index) {
				if (this.videoList[index].isPlay) {
					this.pause(index)
				} else {
					this.play(index)
				}
			}
		}
	}
</script>

<style lang="scss" scoped>
	.swiper-video {
		height: 100vh;
		width: 100vw;

		.video-item {
			height: 100%;
			width: 100%;

			.video-item-content {
				height: 100vh;
				width: 100vw;
			}
		}
	}
</style>
