<template>
	<div>
		<home-header></home-header>
		<home-swiper></home-swiper>
		<div>test</div>
	</div>
</template>

<script>
	import HomeHeader from './components/Header'
	import HomeSwiper from './components/Swiper'
	export default {
		name: '',
		data() { // 选项 / 数据
			return {

			}
		},
		methods: { // 事件处理器

		},
		components: { // 定义组件
			HomeHeader,
			HomeSwiper
		},
		created() { // 生命周期函数

		}
	}
</script>

<style>

</style>