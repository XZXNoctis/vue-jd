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

		<div class="product-list clear">

			<product v-for="(item,index) in products"
					 :id="item.id"
					 :image="item.image"
					 :title="item.title"
					 :price="item.price"></product>

		</div>

		<div style="height: 1000px;"></div>
	</div>
</template>

<script>
	import SearchBar from "@/components/SearchBar.vue";
	import QuickNav from "@/components/QuickNav.vue";
	import Product from "@/components/Product.vue";
	import Swiper from "swiper";
	import "swiper/dist/css/swiper.css";
	export default {
		name: 'home',
		data() {
			return {
				products: [{
					id: 1,
					image: require("@/assets/images/product1.jpg"),
					title: "TP-LINK TL-WDR5620 1200M 5G双频智能无线路由器 四天线智能wifi 稳定穿墙高速家用路由器",
					price: 115
				}, {
					id: 2,
					image: require("@/assets/images/product2.jpg"),
					title: "满199减120三只松鼠 夏威夷果160g 零食坚果炒货孕妇坚果每日坚果干果休闲零食送开口器 160g",
					price: 35.8
				},{
					id: 3,
					image: require("@/assets/images/product1.jpg"),
					title: "TP-LINK TL-WDR5620 1200M 5G双频智能无线路由器 四天线智能wifi 稳定穿墙高速家用路由器",
					price: 205
				}, {
					id: 4,
					image: require("@/assets/images/product2.jpg"),
					title: "满199减120三只松鼠 夏威夷果160g 零食坚果炒货孕妇坚果每日坚果干果休闲零食送开口器 160g",
					price: 38.8
				}]
			}
		},
		components: {
			SearchBar,
			QuickNav,
			Product
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
		background-color: yellow!important;
	}
	
	#swiper-container {
		width: 100%;
	}
	
	#swiper-container img {
		width: 100%;
	}
</style>