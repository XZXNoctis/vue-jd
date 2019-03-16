<template>

	<div id="index">
		<search-bar></search-bar>
		<swiper></swiper>

		<quick-nav></quick-nav>

		<div class="product-list clear">

			<product v-for="(item,index) in products" :key="index" :id="item.id" :image="item.image" :title="item.title" :price="item.price"></product>

		</div>

		<tab-bar></tab-bar>
		<div style="height: 1000px;background-color: yellow;"></div>
	</div>

</template>

<script>
	import SearchBar from "@/components/SearchBar.vue";
	import TabBar from "@/components/TabBar.vue";
	import Swiper from "@/components/Swiper.vue";
	import QuickNav from "@/components/QuickNav.vue";
	import Product from "@/components/Product.vue";
	import axios from "axios";
	import qs from "qs";

	export default {
		data: function() {
			return {
				products: [],

			};
		},
		methods: {},
		props: [],
		watch: {},
		computed: {},
		components: {
			SearchBar,
			TabBar,
			Swiper,
			QuickNav,
			Product
		},
		created() {
			// 通过ajax请求获取的数据
			axios.get("/product.json", qs.stringify({
					id: 1,
					user: 'admin'
				}))
				.then(res => {
					this.products = res.data;
				})
				.catch(err => {})
				.finally(() => {});

			
			
			console.log(qs.stringify({
				id: 1,
				user: 'admin'
			}));
		}
	}
</script>

<style>

</style>