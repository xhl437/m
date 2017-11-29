<template>
	<div class="detailmiblebox">

		<div class="g-section miblebox">
			<div class="t">热卖推荐</div>
			<div ref="container" class="swiper-container rs g-recommend swiper-container-horizontal swiper-container-free-mode">
				<div class="swiper-wrapper">

					<div class="swiper-slide swiper-slide-active mms" :banner="banner" v-for="banner in bannerx" :key="banner.id">
						<span class="pro-img" style="height: 114.328px;">
							<a href="/v4/goods/24587">
	            				<img :src="banner.thumbnail">
							</a>
						</span>

						<span class="pro-title">{{banner.goods_name}}</span>
						<span class="pro-price">{{banner.goods_price}}
							<span class="old-price">
								{{banner.market_price}}
							</span>
						</span>
					</div>

				</div>
			</div>
		</div>

	</div>

</template>
<script>
	import axios from 'axios'
	import Swiper from 'swiper'

	export default {
		name: 'detailmiblebox',
		props: ['url'],
		data() {
			return {
				bannerx: []
			}
		},
		methods: {
			getBanner() {
				let that = this
				axios.get(this.url, {
					params: { _t: Date.now() }
				}).then((res) => {

					that.bannerx = res.data.data.goods_list

					console.log(that.bannerx)

				})
			}
		},
		created() {
			this.getBanner()
		},
		updated() {
			
			var mySwiper = new Swiper('.rs',{
				
				loop:true,
				slidesPerView : 3,
				slidesPerGroup : 3,
			})
			
		}

	}
	
	
	
</script>
<style lang="scss">
	body,
	ul,
	li,
	p,
	a,
	h1,
	button,
	input,
	select,
	textarea {
		font-family: "Helvetica Neue", Helvetica, STHeiTi, Arial, sans-serif;
		font-size: 12px;
	}
	
	
	
	
	a {
		text-decoration: none;
		color: #4F494B;
	}
	
	img {
		width: 100%;
		border: 0;
		box-sizing: border-box;
	}
	
	img,
	a {
		vertical-align: top;
		-webkit-user-select: none;
		-webkit-tap-highlight-color: rgba(0, 0, 0, 0);
	}
	
	.miblebox {
		overflow: hidden;
		height: 240px;
		margin-bottom: 60px;
	}
	
	.g-section {
		background: #fff;
		margin-top: 10px;
		padding-top: 8px;
		
		.mms{
			width:114.333px!important;
			margin-right: 8px!important;
		}
		.t {
			color: #4F494B;
			font-size: 17px;
			line-height: 38px;
			padding-left: 16px;
		}
		.g-recommend {
			padding: 8px;
			.pro-img {
				height:110px;
				display: block;
			}
			.pro-title {
				padding: 8px 0;
				display: block;
				overflow: hidden;
				text-overflow: ellipsis;
				white-space: nowrap;
			}
			.pro-price {
				font-size: 13px;
				color: #E74C3C;
			}
			.old-price {
				color: #BEBDBB;
				text-decoration: line-through;
			}
		}
		.swiper-container {
			margin: 0 auto;
			position: relative;
			overflow: hidden;
			z-index: 1;
		}
	}
</style>