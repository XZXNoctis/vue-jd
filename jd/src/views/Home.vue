<template>

	<div id="index">
		<search-bar></search-bar>
		<!--<h1>京东首页</h1>
		-->
		<div style="height: 1000px;background-color: yellow;"></div>
		
		<tab-bar></tab-bar>
	</div>

</template>

<script>
	import SearchBar from "@/components/SearchBar.vue";
	import TabBar from "@/components/TabBar.vue";

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
			TabBar
		}
	}
</script>

<style>

</style>