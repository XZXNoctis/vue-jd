<template>
	<h1>用户的店铺</h1>
</template>

<script>
	
	export default{
		
		
		created(){
			console.log(this.$route.params);
			console.log(this.$route.query);
		}
	}
	
</script>

<style>
</style>