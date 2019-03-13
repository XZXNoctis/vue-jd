<template>
	<div class="home">
		<search-bar></search-bar>

		<div style="height: 1000px;"></div>
	</div>
</template>

<script>
	import SearchBar from "@/components/SearchBar.vue";

	export default {
		name: 'home',
		components: {
			SearchBar: SearchBar
		}
	}
</script>

<style>
	body {
		background-color: black!important;
	}
</style>