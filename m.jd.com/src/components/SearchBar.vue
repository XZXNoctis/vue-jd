<template>

	<div class="search-bar flex" :class="{isFixed:isFixed}">
		<div class="category">
			<span class="icon"></span>
		</div>
		<div class="search-from  flex-item">
			<span class="icon"></span>
			<input type="" name="" id="" value="" />
		</div>
		<div class="login">
			登录
		</div>
	</div>

</template>

<script>
	export default {
		data: function() {
			return {
				isFixed: false
			};
		},
		methods: {},
		props: [],
		watch: {},
		computed: {},
		created() {},
		mounted() {
			/**
			 *  function(){} 
			 * 
			 *   改成箭头函数,好处就是this仍然会继续指向vue.js不会乱指。
			 * 
			 *  ()=>{}
			 * 
			 * 
			 * **/
			// 监听滚动事件
			window.onscroll = () => {
				// 获取滚动的高度
				var scrollTop = document.documentElement.scrollTop || document.body.scrollTop;
				if(scrollTop > 40) {
					this.isFixed = true;
				} else {
					this.isFixed = false;
				}
			}
		}
	}
</script>

<style>
	.search-bar {
		height: 0.88rem;
		width: 100%;
		position: fixed;
		z-index: 9999;
	}
	
	.search-bar.isFixed {
		background-color: #e43130;
	}
	
	.search-bar .category,
	.search-bar .login {
		width: 1rem;
		height: 0.88rem;
	}
	
	.search-bar .category .icon {
		margin: 0.28rem 0 0 0.3rem;
		width: 0.4rem;
		height: 0.36rem;
		display: block;
		background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACgAAAAgAgMAAAAdw9KTAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAMUExURUdwTP///////////waf0AoAAAADdFJOUwDjSYAlncUAAAAbSURBVBjTY5j/Hwq+MdTDmH+RmUgK6AuGhcsAU5tyB6Ji+x0AAAAASUVORK5CYII=) no-repeat;
		background-size: 100% 100%;
	}
	
	.search-bar .login {
		color: #fff;
		font-size: 0.28rem;
		text-align: center;
		line-height: 0.88rem;
	}
	
	.search-from {
		padding-top: 0.14rem;
		position: relative;
	}
	
	.search-from .icon {
		width: 0.4rem;
		height: 0.3rem;
		background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACgAAAAeBAMAAACs80HuAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAwUExURUdwTOk7Puo7PfE+SP9SUuo7Peo8Pu0/Qeo7Peo7Peo7Pek7Peo7Pes8Pus8P+k7PaLYf6IAAAAPdFJOUwCjwREGj1sg9Hrd6bFINxDM6d8AAAD3SURBVCjPY2AAAv3/nxnk////sUo1nQEOoIIgoOaARfD/WmyC/wNQBL+lzZQCCn5FEfwCZJX2//8/AV2Qoej//3YMQWb9/x8xBBkq/v8vwBBk/f8/AUOQ/f9/AQxBhvX/N2AKnv//AVMwHsjBEJz//zs2lVgE5bFpx2pR//8FUMEvcEE+mOPX/2+AC/JAvcnyH6gDJvj+/w8DEM0G0gEVZN8PDfpqkA6o4O3//5tBtGX//98OEEHmJGAkXWBgCNQC0t9Abv4aKrMewmYAR6sAAzyKfydABX8yIASFGSCCjQ/ggr+mg61WOjgXnHwmKSnpiM4FO5EBAIlo6/K7pNY1AAAAAElFTkSuQmCC) no-repeat;
		background-size: 0.4rem 0.3rem;
		margin: 0.16rem 0.16rem 0 0.3rem;
		position: absolute;
		z-index: 1;
	}
	
	.search-from input {
		width: 100%;
		height: 0.6rem;
		padding-left: 1.36rem;
		box-sizing: border-box;
		border-radius: 0.3rem;
		background-color: #FFFFFF;
		border: none;
	}
</style>