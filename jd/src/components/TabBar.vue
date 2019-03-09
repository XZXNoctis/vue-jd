<template>
	<div class="tab-bar">
		<ul class="flex">
			<li class="flex-item" :class="{active:navIndex==index}" @click="goTo(index,item.url);" v-for="(item,index) in nav" :key="index">
				<!--<router-link :to="item.url">
					<span :class="item.icon"></span>
					<div class="title" v-text="item.title"></div>
				</router-link>-->
				<span :class="item.icon"></span>
				<div class="title" v-text="item.title"></div>
			</li>
		</ul>
	</div>
</template>

<script>
	export default {

		data() {
			return {
				navIndex: 0,
				nav: [{
					title: '首页',
					icon: 'fa fa-home',
					url: '/'
				}, {
					title: '分类',
					icon: 'fa fa-list',
					url: '/category'
				}, {
					title: '搜索',
					icon: 'fa fa-search',
					url: '/search'
				}, {
					title: '购物车',
					icon: 'fa fa-shopping-cart',
					url: '/shopping'
				}, {
					title: '我的',
					icon: 'fa fa-user',
					url: '/user'
				}]
			};
		},methods:{
			goTo(index,url){
				this.navIndex = index;
				this.$router.push(url);
			}
		}

	}
</script>

<style>
	.tab-bar {
		margin: 0;
		padding: 0;
		height: 1rem;
		position: fixed;
		left: 0;
		bottom: 0;
		z-index: 31;
		box-sizing: border-box;
		width: 100%;
		list-style: none;
		background-color: #fff;
		box-shadow: 0 0 10px 0 hsla(0, 6%, 58%, .6);
		-webkit-box-shadow: 0 0 10px 0 hsla(0, 6%, 58%, .6);
		-moz-box-shadow: 0 0 10px 0 hsla(0, 6%, 58%, .6);
		font-size: 0.24rem;
		text-align: center;
		color: #70727c;
		padding-top: 0.1rem;
		box-sizing: border-box;
	}
	
	.tab-bar .fa {
		font-size: 0.48rem;
	}
	.tab-bar .active{
		color: #f23030;
	}
	.tab-bar .active a{
		color: #f23030;
	}
</style>