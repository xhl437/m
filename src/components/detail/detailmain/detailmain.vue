<template>
	<div class="detailmain">
		<div class="bj_fff">
			<div ref="container" class="detaimain app-swiper swiper-container  container">
		
				<div class="swiper-wrapper">
					<div class="swiper-slide" v-for="banner in banners"><img width="100%" :src="banner" /></div>
				</div>
		
				<div class="swiper-pagination swiper-pagination-clickable swiper-pagination-bullets bot">
					
				</div>
				
			</div>
			
			
		</div>
		
	</div>
	
	
</template>
<script>
	import axios from 'axios'
	import Swiper from 'swiper'
	export default {
		name: 'detailmain',
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
					
					that.banners = res.data.data.splash
				})
			}
		},
		created() {
			this.getBanners()
		},
		updated() {
			new Swiper(this.$refs.container, {
				loop: true,
				pagination:{
					el:'.swiper-pagination'
				}
			})
		}

	}
</script>
<style>
	.bot{bottom:20px;}
	.bj_fff{background:#fff;}
	
</style>



