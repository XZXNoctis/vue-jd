<template>

	<div class="search-bar">
		<div class="category"></div>
		<div class="search-from">
			<input type="" name="" id="" value="" />
		
		</div>
		<div class="login"></div>
	</div>

</template>

<script>
	export default {
		data: function() {
			return {};
		},
		methods: {},
		props: [],
		watch: {},
		computed: {},
		created: function() {},
	}
</script>

<style>
	.search-bar {
		height: 44px;
		background-color: red;
		position: relative;
	}
	.search-bar .category,.search-bar .login{
		width: 50px;
		height: 44px;
		background-color: blue;
		position: absolute;
		top: 0px;
		left: 0px;
	}
	
	.search-bar .login{
		right: 0px;
		left: auto;
	}
	
	.search-from{
		width: 100%;
		padding: 0px 50px;
		box-sizing: border-box;
		padding-top: 7px;
	}
	.search-from input{
		width: 100%;
		height: 30px;
		box-sizing: border-box;
		border-radius: 15px;
		background-color: #FFFFFF;
	}
	
</style>