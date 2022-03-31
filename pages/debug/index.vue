<template>
	<view class="debug-swiper">
		<view class="debug-content">
			<demo-block title="调试">
				<z-swiper ref="zSwiper" v-model="list" :options="options" :custom-style="{height:'300rpx'}">
					<z-swiper-item v-for="(item,index) in list" :key="index">
						<image class="image" :src="item.img" mode="aspectFill">
						</image>
					</z-swiper-item>
				</z-swiper>
			</demo-block>
		</view>
		<scroll-view style="height: 800rpx;" scroll-y="true">
			<view class="debug-button">
				<button class="button" size="mini" type="default" @click="updateData(1)">点击改变数据为一条</button>
				<button class="button" size="mini" type="default" @click="updateData(2)">点击改变数据为两条</button>
				<button class="button" size="mini" type="default" @click="updateData(6)">点击改变数据为六条</button>
			</view>
			<view class="debug-button">
				<button class="button" size="mini" type="default" @click="updateOptions(0)">修改方向（纵向）</button>
				<button class="button" size="mini" type="default" @click="updateOptions(1)">修改方向（横向）</button>
			</view>
			<view class="debug-button">
				<button class="button" size="mini" type="default" @click="updateOptions(2)">修改切换速度为10ms </button>
				<button class="button" size="mini" type="default" @click="updateOptions(3)">修改切换速度为300ms </button>
				<button class="button" size="mini" type="default" @click="updateOptions(4)">修改切换速度为1000ms </button>
			</view>
			<view class="debug-button">
				<button class="button" size="mini" type="default" @click="updateOptions(5)">禁用Swiper</button>
				<button class="button" size="mini" type="default" @click="updateOptions(6)">启用Swiper</button>
			</view>
			<view class="debug-button">
				<button class="button" size="mini" type="default" @click="updateOptions(7)">修改slidesPerView为1</button>
				<button class="button" size="mini" type="default" @click="updateOptions(8)">修改slidesPerView为2</button>
				<button class="button" size="mini" type="default" @click="updateOptions(9)">修改slidesPerView为3</button>
			</view>
			<view class="debug-button">
				<button class="button" size="mini" type="default" @click="updateOptions(10)">获取activeIndex</button>
				<button class="button" size="mini" type="default" @click="updateOptions(11)">获取realIndex</button>
			</view>
		</scroll-view>

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
					// loop: true,
					// slidesPerView: 3,
					// centeredSlides: true,
					// spaceBetween: 14
					effect: "cards",
					
				},
				list: [{
					img: 'https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe1.jpg'
				}, {
					img: 'https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe2.jpg'
				}, {
					img: 'https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe3.jpg'
				}],
			}
		},
		methods: {
			updateData(number) {
				let data = [];
				for (var i = 0; i < number; i++) {
					data.push({
						img: `https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe${i+1}.jpg`
					})
				}
				this.list = data
			},
			updateOptions(number) {
				switch (number) {
					case 0:
						this.$set(this.options, 'direction', 'vertical')
						break;
					case 1:
						this.$set(this.options, 'direction', 'horizontal')
						break;
					case 2:
						this.$set(this.options, 'speed', 10);
						break;
					case 3:
						this.$set(this.options, 'speed', 300);
						break;
					case 4:
						this.$set(this.options, 'speed', 1000);
						break;
					case 5:
						this.$refs.zSwiper.swiper.disable();
						break;
					case 6:
						this.$refs.zSwiper.swiper.enable();
						break;
					case 7:
						this.$set(this.options, 'slidesPerView', 1);
						break;
					case 8:
						this.$set(this.options, 'slidesPerView', 2);
						break;
					case 9:
						this.$set(this.options, 'slidesPerView', 3);
						break;
					case 10:
						uni.showToast({
							title: `activeIndex:${this.$refs.zSwiper.swiper.activeIndex}`,
							icon: "none"
						})
						break;
					case 11:
						uni.showToast({
							title: `realIndex:${this.$refs.zSwiper.swiper.realIndex}`,
							icon: "none"
						})
						break;
				}
			}
		}
	}
</script>

<style scoped lang="scss">
	.debug-swiper {

		.debug-button {
			padding: 20rpx;
			display: flex;
			justify-content: flex-start;
			flex-wrap: wrap;

			.button {
				margin: 0;
				padding: 0 10rpx;
			}
		}

		.image {
			height: 300rpx;
			width: 100%;
		}
	}
</style>
