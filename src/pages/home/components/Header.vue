<template>
  <div class="header">
    <div class="header-left">
      	<div class="iconfont">&#xe624;</div>
    </div>
    <div class="header-input">
        <span class="iconfont">&#xe632;</span> 输入城市景点游玩主题
    </div>
    <div class="header-right">
         城市 <span class="iconfont arrow-icon">&#xe64a;</span> 
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  data () { // 选项 / 数据
    return {

    }
  },
  methods: { // 事件处理器

  },
  components: { // 定义组件

  },
  created () { // 生命周期函数

  }
}
</script>

<style lang="stylus" scoped="scoped">
/*在css样式中引用css文件,想用@符号,要加~符号,@这里代表src文件夹*/
@import "~@/assets/styles/varibles.styl";
.header{
	line-height: .86rem;
	display: flex;
	background: $bgColor;/*在.styl文件里进行全局配置*/
	color:#FFFFFF;
	align-items: center;
}
.header-left{
	width: 0.64rem;
}
.header-input{
	line-height:.64rem;
	margin-left:.2rem;
	flex:1;
	background: #fff;
	border-radius: .1rem;
	color:#ccc;
}
.header-right{
	width: 1.24rem;
	.arrow-icon{
		font-size:.2rem;
	}
}
</style>
