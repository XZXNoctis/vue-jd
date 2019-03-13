<template>

	<div class="product">
		<div style="background-color: #FFFFFF;">
			<router-link :to="'/product/'+id">
				<div class="product-image">
					<img v-bind:src="image">
				</div>
				<div class="product-title" v-text="title"></div>
			</router-link>
			<div class="product-info clear">
				<div class="product-price">￥ <span v-text="price"></span> </div>
				<div class="product-simlar">看相似</div>
			</div>
			<div class="product-info clear">
			</div>
		</div>

	</div>

</template>

<script>
	export default {
		data() {
			return {};
		},
		props: {
			id: {
				type: Number,
				default: 0,
			},
			image: {
				type: String,
				default: require("@/assets/images/default.png")
			},
			title: {
				type: String,
				default: '商品标题'
			},
			price: {
				type: Number,
				default: 0
			}
		}
	}
</script>

<style>
	.product {
		width: 50%;
		float: left;
		padding: 0 2px 4px 0;
		box-sizing: border-box;
	}
	
	.product a {
		display: block;
	}
	
	.product-list .product:nth-child(2n) {
		padding: 0 0 4px 2px;
	}
	
	.product-image {
		width: 100%;
	}
	
	.product-image img {
		width: 100%;
	}
	
	.product-title {
		background-color: #FFFFFF;
		box-sizing: border-box;
		height: 0.6rem;
		font-size: 0.26rem;
		overflow: hidden;
		text-overflow: ellipsis;
		display: -webkit-box;
		-webkit-line-clamp: 2;
		-webkit-box-orient: vertical;
		word-break: break-word;
		color: #232326;
		margin-top: 0.1rem;
		line-height: 0.32rem;
		margin-bottom: 0.06rem;
		padding: 0 0.08rem;
	}
	
	.product-info {
		height: 0.44rem;
		font-size: 0.26rem;
		overflow: hidden;
		position: relative;
	}
	
	.product-info .product-price {
		color: #f23030;
		display: inline-block;
		padding: 0 0.1rem 0 0.08rem;
		position: relative;
		top: 1px;
		height: 0.5rem;
		line-height: 0.5rem;
	}
	
	.product-info .product-price span {
		font-size: 0.32rem;
	}
	
	.product-simlar {
		display: block;
		position: absolute;
		top: 0;
		right: 0.16rem;
		text-align: center;
		color: #686868;
		font-size: 0.24rem;
		width: 0.98rem;
		height: 0.42rem;
		line-height: 0.42rem;
		box-sizing: border-box;
		border: 1px solid #bfbfbf;
		border-radius: 4px;
	}
</style>