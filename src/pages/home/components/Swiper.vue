<template>
	<div class="wrapper">
		<swiper :options="swiperOption">
			<!-- slides -->
			<swiper-slide v-for="item of swiperList" :key="item.id">
				<img class="swiper-img" :src="item.imgUrl" />
			</swiper-slide>
			<div class="swiper-pagination" slot="pagination"></div>
			<!--<div class="swiper-button-prev" slot="button-prev"></div>-->
			<!--<div class="swiper-button-next" slot="button-next"></div>-->
			<!--<div class="swiper-scrollbar" slot="scrollbar"></div>-->
		</swiper>
	</div>
</template>

<script>
	export default {
		name: 'HomeSwiper',
		data() {
			return {
				swiperOption: {
					pagination:'.swiper-pagination',
					loop:true
				},
				swiperList:[{
					id:'0001',
					imgUrl:'/static/swiper_1.jpg'
				},{
					id:'0002',
					imgUrl:'/static/swiper_2.jpg'
				},{
					id:'0003',
					imgUrl:'/static/swiper_3.jpg'
				}]
			}
		}
	}
</script>

<style lang="stylus" scoped="scoped">
	.wrapper>>>.swiper-pagination-bullet-active{
		background: #FFFFFF;
	}
	.wrapper{
		width: 100%;
		height:2rem;
		background: #eee;
	}
	.swiper-img {
		width: 100%;
	}
	
</style>