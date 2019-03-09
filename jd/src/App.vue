<template>
	<div id="app">
		<router-view/>
	</div>
</template>
<script>
</script>
<style>
	html {
		font-size: calc(100vw/7.5);
	}
	
	body {
		margin: 0;
		font-family: "arial, helvetica, sans-serif";
		font-size: 0.14rem;
		color: #333;
	}
	
	html,
	body,
	#app {
		width: 100%;
		height: 100%;
	}
	
	.left{
		float: left;
	}
	.right{
		float: right;
	}
	
	.clear:after{
		display: block;
		content: "";
		clear: both;
	}
	
	.flex{
		display:-webkit-flex;
		display: flex;
	}
	
	.flex-item{
		-webkit-flex: 1;
		flex: 1;
	}
	
	a{
		text-decoration: none;
		color: #333333;
	}
	
		ul,
	ol {
		margin: 0;
		padding: 0;
		list-style: none;
	}
	
</style>