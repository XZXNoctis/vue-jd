<template>

	<div class="product">
		<div style="background-color: #FFFFFF;">
			<router-link :to="{path:'/product',query:{id:id}}">

				<div class="product-image">
					<img :src="image" />
				</div>
				<div class="product-title" v-text="title"></div>
			</router-link>
			<div class="product-inof clear">
				<div class="product-price left">￥ <span v-text="price"></span> </div>
				<div class="product-similar right">看相似</div>
			</div>
			<div class="product-inof clear">
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
				type: [String, Number],
				default: 0,
				required: true
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
	.product-list {
		background-color: red;
	}
	
	.product {
		width: 50%;
		padding: 0px 2px 4px 0;
		box-sizing: border-box;
		float: left;
	}
	
	.product a {
		display: block;
	}
	
	.product-list .product:nth-child(2n) {
		padding: 0px 0 4px 2px;
	}
	
	.product-image {
		width: 100%;
		background-color: #FFFFFF;
	}
	
	.product-image img {
		width: 100%;
	}
	
	.product-inof {
		height: 0.52rem;
	}
	
	.product-title {
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
		line-height: 0.32rem;
		padding: 0 0.08rem;
		margin-top: 0.1rem;
		margin-bottom: 0.06rem;
	}
	
	.product-price {
		color: #f23030;
		display: inline-block;
		padding: 0 0.1rem 0 0.08rem;
		position: relative;
		top: 0.02rem;
		height: 0.5rem;
		line-height: 0.5rem;
	}
	
	.product-price span {
		font-size: 0.32rem;
	}
	
	.product-similar {
		display: block;
		border: 1px solid #bfbfbf;
		border-radius: 4px;
		position: relative;
		top: 0;
		right: 0.16rem;
		text-align: center;
		color: #686868;
		font-size: 0.24rem;
		width: 0.98rem;
		height: 0.48rem;
		line-height: 0.5rem;
	}
</style>