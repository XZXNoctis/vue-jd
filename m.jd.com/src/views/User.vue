<template>
	
	<div id="user">
		<h1>个人中心</h1>
		
		<router-view></router-view>
		
		
		<div>
			<!--
				1. 直接放入路径
				2. 通过路由名称(params、query都可以传递参数)
				3. 通过path跳转(只有query可以传递参数)
			-->
			<router-link to="/user/info">信息</router-link> |
			<router-link :to="{name:'shop',params:{id:1},query:{user:'admin'} }">店铺</router-link> |
			<router-link :to="{path:'/user/like',params:{id:1},query:{user:'admin'} }">喜欢</router-link> |
			
		</div>
		<!--
			通过编程式进行导航
		-->
		<button @click="$router.push('/user/info')" >信息</button>
		<button @click="$router.push({name:'shop',params:{id:1},query:{user:'admin'} })">店铺</button>
		<button @click="$router.push({path:'/user/like',params:{id:1},query:{user:'admin'} });">喜欢</button>
		
	</div>
	
</template>

<script>
</script>

<style>
	
	a,button{
		margin: 0px 5px;
		font-size: 20px;
	}
</style>