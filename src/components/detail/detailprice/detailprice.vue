<template>
	<div class="price">
		<div class="g-t">
			<div class="g-title" isupass="0">
				<h1> {{datas.goods_name}} </h1>
	
			</div>
			<div class="g-price">
				<span class="price-now"> {{datas.goods_price}} </span>
				<span class="price-origin"> {{datas.market_price}} </span>
				<span class="sales">已售  {{datas.sold_number}} 件</span>
			</div>
			<div class="g-guarantee g-guarantee-rule">
				<span  v-for="da in datas.services" >{{da.desc}}</span>
			</div>
		</div>
	</div>

</template>
<script>
	import axios from 'axios'
	import Swiper from 'swiper'
	export default {
		name: 'detailprice',
		props: ['url'],
		data() {
			return {
				datas: []
			}
		},
		methods: {
			getBanners() {
				let that = this
				axios.get(this.url, {
					params: { _t: Date.now() }
				}).then((res) => {
					
					that.datas = res.data.data
					
				})
			}
		},
		created() {
			this.getBanners()
		}

	}
</script>
<style lang="scss">
	.g-t{background:#fff;}
	
	.g-guarantee span:before {
	    content: "\25CF";
	    display: inline-block;
	    margin-top: -6px;
	    text-align: center;
	    vertical-align: middle;
	    width: 13px;
	    height: 18px;
	}
	
	.g-title {
		padding: 0 8px 0 16px;
		margin-top:20px;
		padding-top:20px;
		h1 {
			font-size: 17px;
			color: #4F494B;
			line-height: 24px;
		}
	}
	
	.g-price {
		font-size: 21px;
		color: #E74C3C;
		padding: 16px 8px 16px 16px;
		
		.price-origin {
			font-size: 13px;
			color: #BEBDBB;
			padding-left: 8px;
			text-decoration: line-through;
		}
		.sales {
			font-size: 13px;
			color: #BEBDBB;
			margin-top: 7px;
			float: right;
		}
	}
	
	.g-guarantee-rule {
		padding-right: 16px;
	}
	
	.g-guarantee {
		line-height: 23px;
		color: #828282;
		span {
			display: inline-block;
			margin: 6px 0 6px 16px;
			margin-left: 16px;
		}
	}
	
	.g-guarantee-rule:after {
	    content: "";
	    float: right;
	    margin-top: 8px;
	    width: 22px;
	    height: 22px;
	    background: url("https://ss3.bdstatic.com/70cFv8Sh_Q1YnxGkpoWK1HF6hhy/it/u=756318008,2510646187&fm=27&gp=0.jpg") no-repeat center;
	    background-size: 100%;
	}

	
	h1{
		font-weight: normal;
	}
	

	
</style>