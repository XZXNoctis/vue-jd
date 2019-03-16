<template>

	<!-- Swiper -->
	<div class="swiper-container">
		<div class="swiper-wrapper">
			<div class="swiper-slide" v-for="(item,index) in images">
				<img :src="item.src" />
			</div>
			
		</div>
		<!-- Add Pagination -->
		<div class="swiper-pagination"></div>
	</div>

</template>

<script>
	
	import Swiper from "swiper";
	import "swiper/dist/css/swiper.css";
	
	export default {
		data(){
			return {
				images:[
					{url:'#',src:require("@/assets/images/1.jpg")},
					{url:'#',src:require("@/assets/images/2.jpg")},
					{url:'#',src:require("@/assets/images/3.jpg")},
					{url:'#',src:require("@/assets/images/4.jpg")}
				],
			}
		},
		mounted() {
			var swiper = new Swiper('.swiper-container', {
				loop:true,
				autoplay:true,
				pagination: {
					el: '.swiper-pagination',
					clickable: true,
				},
			});
		}
	}
</script>

<style>
	
	.swiper-container{}
	.swiper-container img{
		width: 100%;
	}

</style>