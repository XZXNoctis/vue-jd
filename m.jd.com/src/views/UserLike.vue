<template>
	<h1>用户喜欢</h1>
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