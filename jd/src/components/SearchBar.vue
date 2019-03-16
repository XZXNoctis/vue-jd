<template>

	<div class="search-bar flex" v-bind:class="{fixed:isFixed}">
		<div class="category"></div>
		<div class="search-form flex-item">
			<span class="jd-icon"></span>
			<input type="text" />

		</div>
		<div class="login">登录</div>
	</div>

</template>

<script>
	export default {
		data: function() {
			return {
				isFixed:false
			};
		},
		methods: {},
		props: [],
		watch: {},
		computed: {},
		created(){
			window.onscroll = (e)=>{
				var scrollTop = document.documentElement.scrollTop||document.body.scrollTop;
				if(scrollTop>20){
					this.isFixed = true;
				}else{
					this.isFixed = false;
				}
			}
		}
	}
</script>

<style scoped="scoped">
	.search-bar {
		height: 0.88rem;
		position: fixed;
		width: 100%;
		top: 0px;
		left: 0px;
		z-index:9999;
	}
	
	.fixed{
		background-color: #e43130;
	}
	
	.category {
		margin: 0.28rem 0 0 0.30rem;
		width: 0.40rem;
		height: 0.36rem;
		display: block;
		background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACgAAAAgAgMAAAAdw9KTAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAMUExURUdwTP///////////waf0AoAAAADdFJOUwDjSYAlncUAAAAbSURBVBjTY5j/Hwq+MdTDmH+RmUgK6AuGhcsAU5tyB6Ji+x0AAAAASUVORK5CYII=) no-repeat;
		background-size: 100% 100%;
	}
	
	.search-form {
		border: none;
		height: 0.6rem;
		overflow: hidden;
		font-size: 0.24rem;
		padding-top: 0.14rem;
		padding-left: 0.2rem;
		padding-right: 0.2rem;
		position: relative;
	}
	
	.jd-icon {
		width: 0.4rem;
		height: 0.3rem;
		background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACgAAAAeBAMAAACs80HuAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAwUExURUdwTOk7Puo7PfE+SP9SUuo7Peo8Pu0/Qeo7Peo7Peo7Pek7Peo7Pes8Pus8P+k7PaLYf6IAAAAPdFJOUwCjwREGj1sg9Hrd6bFINxDM6d8AAAD3SURBVCjPY2AAAv3/nxnk////sUo1nQEOoIIgoOaARfD/WmyC/wNQBL+lzZQCCn5FEfwCZJX2//8/AV2Qoej//3YMQWb9/x8xBBkq/v8vwBBk/f8/AUOQ/f9/AQxBhvX/N2AKnv//AVMwHsjBEJz//zs2lVgE5bFpx2pR//8FUMEvcEE+mOPX/2+AC/JAvcnyH6gDJvj+/w8DEM0G0gEVZN8PDfpqkA6o4O3//5tBtGX//98OEEHmJGAkXWBgCNQC0t9Abv4aKrMewmYAR6sAAzyKfydABX8yIASFGSCCjQ/ggr+mg61WOjgXnHwmKSnpiM4FO5EBAIlo6/K7pNY1AAAAAElFTkSuQmCC) no-repeat;
		background-size: 0.4rem 0.3rem;
		margin: 0.16rem 0.16rem 0 0.3rem;
		position: absolute;
		z-index: 9999;
		float: left;
	}
	
	.search-form input {
		outline: none;
		width: 100%;
		font-size: 0.24rem;
		height: inherit;
		border-radius: 0.3rem;
		padding-left: 1rem;
		box-sizing: border-box;
		border: none;
		background-color: #FFFFFF;
	}
	
	.login {
		width: 0.8rem;
		line-height: 0.88rem;
		display: inline-block;
		color: #fff;
		font-size: 0.28rem;
	}
</style>