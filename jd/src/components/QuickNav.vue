<template>

	<div class="quick-nav clear">
		<router-link :to="item.url" class="quick-nav-item left" v-for="(item,index) in nav" :key="index">
			<img :src="item.image" />
			<div class="title" v-text="item.title"></div>
		</router-link>
	</div>

</template>

<script>
	export default {
		data() {
			return {
				nav: [{
					image: require("@/assets/images/1.png"),
					title: '京东超市',
					url: '#'
				}, {
					image: require("@/assets/images/2.png"),
					title: '京东超市',
					url: '#'
				}, {
					image: require("@/assets/images/3.png"),
					title: '京东超市',
					url: '#'
				}, {
					image: require("@/assets/images/4.png"),
					title: '京东超市',
					url: '#'
				}, {
					image: require("@/assets/images/5.png"),
					title: '京东超市',
					url: '#'
				}, {
					image: require("@/assets/images/6.png"),
					title: '京东超市',
					url: '#'
				}, {
					image: require("@/assets/images/7.png"),
					title: '京东超市',
					url: '#'
				}, {
					image: require("@/assets/images/8.png"),
					title: '京东超市',
					url: '#'
				}, {
					image: require("@/assets/images/9.png"),
					title: '京东超市',
					url: '#'
				}, {
					image: require("@/assets/images/10.png"),
					title: '京东超市',
					url: '#'
				}],

			};
		}
	}
</script>

<style>
	.quick-nav {
		padding-bottom: 0.2rem;
	}
	
	.quick-nav-item {
		text-align: center;
		width: 20%;
	}
	
	.quick-nav-item img {
		width: 0.8rem;
		height: 0.8rem;
		margin-top: 0.2rem;
	}
	
	.quick-nav-item .title {
		margin-top: 0.06rem;
		font-size: 0.24rem;
		color: #666;
	}
</style>