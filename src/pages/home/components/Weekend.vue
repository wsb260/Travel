<template>
	<div>
		<div class="weekend-title">周末去哪</div>
		<ul>
			<li class="item" v-for="(item,index) of weekendList" :key="index">
				<div class="imgcontainer">
					<img class="item-img" :src="item.imgUrl" alt="img" />
				</div>
				<div class="item-info">
					<p class="item-title">{{item.title}}</p>
					<p class="item-desc">{{item.desc}}</p>
				</div>
				<a :href="item.href" class="item-fulllink"></a>
			</li>
		</ul>
	</div>
</template>

<script>
	export default {
		name: 'weekend',
		data() {
			return {
				weekendList: [{
					id: '0001',
					imgUrl: '/static/week_1.jpg',
					title: '北京必游TOP10',
					desc: '类北京必去的景点非这些地方莫属',
					href: 'http://piao.qunar.com/touch/toSku.htm?skuId=256&skuName=%E5%8C%97%E4%BA%AC%E5%BF%85%E6%B8%B8TOP10&cat=from_area%3Dts_sku%26from_index%3D0%26from_value%3D%25E5%258C%2597%25E4%25BA%25AC%25E5%25BF%2585%25E6%25B8%25B8TOP10%26dist_city%3D%25E5%258C%2597%25E4%25BA%25AC'
				}, {
					id: '0002',
					imgUrl: '/static/week_2.jpg',
					title: '寻找北京的皇城范儿',
					desc: '数百年的宫廷庙宇,至今依旧威严霸气',
					href: 'http://piao.qunar.com/touch/toSku.htm?skuId=47&skuName=%E5%AF%BB%E6%89%BE%E5%8C%97%E4%BA%AC%E7%9A%84%E7%9A%87%E5%9F%8E%E8%8C%83%E5%84%BF&cat=from_area%3Dts_sku%26from_index%3D1%26from_value%3D%25E5%25AF%25BB%25E6%2589%25BE%25E5%258C%2597%25E4%25BA%25AC%25E7%259A%2584%25E7%259A%2587%25E5%259F%258E%25E8%258C%2583%25E5%2584%25BF%26dist_city%3D%25E5%258C%2597%25E4%25BA%25AC'
				}]
			}
		}
	}
</script>

<style lang="stylus" scoped="scoped">
	.weekend-title {
		background: #EEEEEE;
		line-height: .4rem;
		padding: .1rem 0;
		text-indent: .2rem;
	}
	
	.item {
		position: relative;
		margin-bottom: .1rem;
		background: #FFFFFF;
	}
	
	.imgcontainer {
		width: 100%;
		height: 0;
		padding-bottom: 37.4%;
		background: #bcbcbc;
	}
	
	.item-img {
		width: 100%;
	}
	
	.item-info {
		padding: .14rem .2rem .2rem .2rem;
	}
	
	.item-fulllink {
		position: absolute;
		left: 0;
		top: 0;
		width: 100%;
		height: 100%;
	}
	
	.item-title {
		overflow: hidden;
		white-space: nowrap;
		text-overflow: ellipsis;
		padding-right: 1.4rem;
		font-size: .28rem;
		line-height: .48rem;
	}
	
	.item-desc {
		overflow: hidden;
		padding-right: 1.4rem;
		color: #616161;
		font-size: .24rem;
		line-height: .42rem;
		white-space: nowrap;
		text-overflow: ellipsis;
	}
</style>