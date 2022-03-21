<template>
	<view class="demo-swiper">
		<demo-block title="基础用法">
			<z-swiper v-model="list" :options="options">
				<z-swiper-item v-for="(item,index) in list" :key="index">
					<image class="image" :src="item" mode="aspectFill">
					</image>
				</z-swiper-item>
			</z-swiper>
		</demo-block>
		<button type="default" @click="updateData(2)">点击改变数据为两条</button>
		<button type="default" @click="updateData(6)">点击改变数据为六条</button>
		<button type="default" @click="updateData(1)">点击改变数据为一条</button>
		<demo-block title="基础用法">
			<z-swiper ref="zSwiper" v-model="list">
				<z-swiper-item v-for="(item,index) in list" :key="index">
					<image class="image" :src="item" mode="aspectFill">
					</image>
				</z-swiper-item>
			</z-swiper>
			<button type="default" @click="disableSwiper()">禁用</button>
			<button type="default" @click="enableSwiper()">启用</button>
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
					// loop: true,
					effect: 'cards',
				},
				list: [

				]
			}
		},
		methods: {
			updateData(number) {
				let data = [];
				for (var i = 0; i < number; i++) {
					data.push(`https://cdn.zebraui.com/zebra-ui/images/swipe-demo/swipe${i+1}.jpg`)
				}
				this.list = data
			},
			disableSwiper() {
				this.$refs.zSwiper.swiper.disable();
			},
			enableSwiper() {
				this.$refs.zSwiper.swiper.enable();
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
	}
</style>
