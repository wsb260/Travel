<template>
	<div>
		<div class="recommend-title">热销推荐</div>
		<ul>
			<li class="item border-bottom" v-for="(item,index) of recommendList" :key="index">
				<img class="item-img" :src="item.imgUrl" alt="img" />
				<div class="item-info">
					<p class="item-title">{{item.title}}</p>
					<p class="item-desc">{{item.desc}}</p>
					<button class="item-button">查看详情</button>
				</div>
			</li>
		</ul>
	</div>
</template>

<script>
	export default {
		name: 'recommend',
		data() {
			return {
				recommendList: [{
					id: '0001',
					imgUrl: '/static/item_1.jpg',
					title: '金海湖风景区',
					desc: '浪费的景区乐园'
				}, {
					id: '0002',
					imgUrl: '/static/item_2.jpg',
					title: '北京国际鲜花港',
					desc: '浪费的景区乐园'
				}, {
					id: '0003',
					imgUrl: '/static/item_3.jpg',
					title: '北京欢乐谷',
					desc: '浪费的景区乐园'
				}, {
					id: '0004',
					imgUrl: '/static/item_4.jpg',
					title: '北京欢乐水魔方',
					desc: '浪费的景区乐园'
				}, {
					id: '0005',
					imgUrl: '/static/item_5.jpg',
					title: '古北水镇',
					desc: '浪费的景区乐园'
				}, {
					id: '0006',
					imgUrl: '/static/item_6.jpg',
					title: '北京野生动物园',
					desc: '浪费的景区乐园'
				}, {
					id: '0007',
					imgUrl: '/static/item_7.jpg',
					title: '水立方嬉水乐园',
					desc: '浪费的景区乐园'
				}]
			}
		}
	}
</script>

<style lang="stylus" scoped="scoped">
	@import '~@styles/mixins.styl';
	.recommend-title {
		line-height: .4rem;
		background: #eee;
		text-align: left;
		text-indent: .2rem;
		margin-top: .2rem;
		padding: .1rem 0;
	}
	
	.item {
		display: flex;
		height: 1.9rem;
	}
	
	.item-img {
		width: 1.7rem;
		height: 1.7rem;
		padding: .1rem;
	}
	
	.item-info {
		flex: 1;
		padding: .1rem;
		min-width: 0;
	}
	
	.item-title {
		line-height: .54rem;
		font-size: .32rem;
		ellipsis()
	}
	
	.item-desc {
		line-height: .4rem;
		color: #CCCCCC;
		ellipsis()
	}
	
	.item-button {
		line-height: .44rem;
		background: #ff9300;
		padding: 0 .16rem;
		border-radius: .06rem;
		margin-top: .2rem;
		color: #fff;
	}
</style>