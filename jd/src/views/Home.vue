<template>

	<div id="index">
		<search-bar></search-bar>
		<swiper></swiper>
		
		<div style="height: 1000px;background-color: yellow;"></div>
		
		<tab-bar></tab-bar>
	</div>

</template>

<script>
	import SearchBar from "@/components/SearchBar.vue";
	import TabBar from "@/components/TabBar.vue";
	import Swiper from "@/components/Swiper.vue";

	export default {
		data: function() {
			return {};
		},
		methods: {},
		props: [],
		watch: {},
		computed: {},
		components: {
			SearchBar,
			TabBar,
			Swiper
		}
	}
</script>

<style>

</style>