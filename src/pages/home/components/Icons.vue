<template>
	<div>
		<swiper>
			<swiper-slide v-for="(page,index) of pages" :key="index">
				<div class="icons">
					<div class="icon" v-for="item of page" :key="item.id">
						<img class="icon-img-content" :src="item.imgUrl" />
						<p class="icon-desc">{{item.desc}}</p>
					</div>
				</div>
			</swiper-slide>
		</swiper>
	</div>
</template>

<script>
	export default {
		name: 'icons',
		data(){
			return {
				iconList:[{
					id:'0001',
					imgUrl:'/static/icon_1.png',
					desc:'景点门票'
				},{
					id:'0002',
					imgUrl:'/static/icon_2.png',
					desc:'必游榜单'
				},{
					id:'0003',
					imgUrl:'/static/icon_3.png',
					desc:'夏日玩水'
				},{
					id:'0004',
					imgUrl:'/static/icon_4.png',
					desc:'一日游'
				},{
					id:'0005',
					imgUrl:'/static/icon_5.png',
					desc:'动植物园'
				},{
					id:'0006',
					imgUrl:'/static/icon_6.png',
					desc:'故宫'
				},{
					id:'0007',
					imgUrl:'/static/icon_7.png',
					desc:'主题乐园'
				},{
					id:'0008',
					imgUrl:'/static/icon_8.png',
					desc:'Q+精选'
				},{
					id:'0009',
					imgUrl:'/static/icon_9.png',
					desc:'欢乐谷'
				},{
					id:'0010',
					imgUrl:'/static/icon_10.png',
					desc:'周边游'
				}]
			}
		},
		computed:{
			pages(){//数据分页
				const pages = [];
				this.iconList.forEach((item,index)=>{
					const page = Math.floor(index/8);
					if(!pages[page]){
						pages[page] = [];
					}
					pages[page].push(item);
				});
				return pages;
			}
		}
	}
</script>

<style lang="stylus" scoped="scoped">
	@import '~@styles/varibles.styl';
	@import '~@styles/mixins.styl';
	.icons {
		width: 100%;
		height: 3rem;
		box-sizing: border-box;
		display: flex;
		flex-wrap: wrap;
	}
	
	.icon {
		width: 25%;
		height: 1.5rem;
		padding-top: .1rem;
		text-align: center;
		box-sizing: border-box;
	}
	
	.icon-img-content {
		width: 1.1rem;
		height: 1.1rem;
	}
	
	.icon-desc {
		color: $darkTextColor;
		line-height: .3rem;
		ellipsis()
	}
</style>