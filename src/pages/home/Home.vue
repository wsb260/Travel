<template>
	<div>
		<home-header></home-header>
		<home-swiper></home-swiper>
		<home-icons></home-icons>
	</div>
</template>

<script>
	import HomeHeader from './components/Header'
	import HomeSwiper from './components/Swiper'
	import HomeIcons from './components/Icons'
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
			HomeSwiper,
			HomeIcons
		},
		created() { // 生命周期函数

		}
	}
</script>

<style>

</style>