<template>
	
	<div class="product">
		<!--https://item.m.jd.com/product/3668211.html?pps=reclike.FO4O605%3AFOFO4O37F8F33O13O6%3ACOF0415O2443O1FO8O7FFF5021813FOFO00226A83F53DE68050-->
		<h1>商品详情页{{$route.params.id}}</h1>
	</div>
	
</template>

<script>
	
	export default{
		
		data(){
			return {};
		},
		created(){
			// 当前路由
			console.log(this.$route);
			console.log(this.$router);
		}
		
	}
	
</script>

<style>
</style>