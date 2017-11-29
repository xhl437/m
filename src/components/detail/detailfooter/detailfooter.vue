<template>
	<nav class="bar bar-tab detail-footer">
		<a class="tab-item external price-nowing" href="#" >
			总价{{banners.goods_price}}
		</a>
		
		<a class="tab-item external red" href="#">
			立即购买
		</a>
	</nav>
	
</template>
<script>
	import axios from 'axios'
	import Swiper from 'swiper'
	export default {
		name: 'detailfooter',
		props: ['url'],
		data() {
			return {
				banners: []
			}
		},
		methods: {
			getBanners() {
				let that = this
				axios.get(this.url, {
					params: { _t: Date.now() }
				}).then((res) => {
					
					that.banners = res.data.data
				})
			}
		},
		created() {
			this.getBanners()
		},
		updated() {
			
		}

	}
	
</script>
<style>
	.detail-footer{z-index:10000;position:fixed;bottom:0;}
	.price-nowing{font-size:15px;}
	.bar-tab .red{background:#E74C3C;color:#fff;font-size:15px;}
</style>