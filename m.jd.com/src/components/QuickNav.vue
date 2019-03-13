<template>

	<div class="quick-nav clear">

		<div class="nav-item left" v-for="(item,index) in nav" :key="index">
			<img :src="item.image">
			<div class="nav-title" v-text="item.title"></div>
		</div>

	</div>

</template>

<script>
	export default {
		data() {
			return {
				nav: [{
					image: require('@/assets/images/1.png'),
					title: '超市',
					url: '#'
				}, {
					image: require('@/assets/images/1.png'),
					title: '超市',
					url: '#'
				}, {
					image: require('@/assets/images/1.png'),
					title: '超市',
					url: '#'
				}, {
					image: require('@/assets/images/1.png'),
					title: '超市',
					url: '#'
				}, {
					image: require('@/assets/images/1.png'),
					title: '超市',
					url: '#'
				}, {
					image: require('@/assets/images/1.png'),
					title: '超市',
					url: '#'
				}, {
					image: require('@/assets/images/1.png'),
					title: '超市',
					url: '#'
				}, {
					image: require('@/assets/images/1.png'),
					title: '超市',
					url: '#'
				}, {
					image: require('@/assets/images/1.png'),
					title: '超市',
					url: '#'
				}, {
					image: require('@/assets/images/1.png'),
					title: '超市',
					url: '#'
				}]

			};
		}
	}
</script>

<style>
	.quick-nav {
		background-color: #FFFFFF;
		padding-bottom: 10px;
	}
	
	.nav-item {
		width: 20%;
		text-align: center;
	}
	
	.nav-item img {
		width: 42px;
		height: 42px;
		margin-top: 10px;
	}
	
	.nav-item .nav-title {
		font-size: 12px;
		line-height: 20px;
		color: #666666;
	}
</style>