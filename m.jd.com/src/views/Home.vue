<template>
	<div class="home">
		<search-bar></search-bar>

		<!-- Swiper -->
		<div class="swiper-container" id="swiper-container">
			<div class="swiper-wrapper">
				<div class="swiper-slide"><img src="@/assets/images/1.jpg" /> </div>
				<div class="swiper-slide"><img src="@/assets/images/2.jpg" /> </div>
				<div class="swiper-slide"><img src="@/assets/images/3.jpg" /> </div>
				<div class="swiper-slide"><img src="@/assets/images/4.jpg" /> </div>
			</div>
			<!-- Add Pagination -->
			<div class="swiper-pagination"></div>
		</div>
		
		
		<quick-nav></quick-nav>
		
		<div style="height: 1000px;"></div>
	</div>
</template>

<script>
	import SearchBar from "@/components/SearchBar.vue";
	import QuickNav from "@/components/QuickNav.vue";
	import Swiper from "swiper";
	import "swiper/dist/css/swiper.css";
	export default {
		name: 'home',
		components: {
			SearchBar,
			QuickNav
		},
		mounted() {
			/**
			 * 1. cnpm install --save swiper
			 * 2. 引入css 、Swiper
			 * 3. 复制这个html结构
			 * 4. 实例化Swiper
			 * 5. 优化样式
			 * 参考例子：https://www.swiper.com.cn/demo/100-space-between.html
			 * **/

			new Swiper('#swiper-container', {
				spaceBetween: 0,
				pagination: {
					el: '.swiper-pagination',
					clickable: true,
				},
				autoplay: true,
				loop: true
			});
		}
	}
</script>

<style>
	body {
		background-color: black!important;
	}
	
	#swiper-container {
		width: 100%;
	}
	
	#swiper-container img {
		width: 100%;
	}
</style>