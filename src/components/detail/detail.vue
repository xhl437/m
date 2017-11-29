<template>
	<div class="detail">
		
		<detailheader></detailheader>
		<detailmain  url="/ujp/api/v4/goods/30058"></detailmain>
		<detailprice  url="/ujp/api/v4/goods/30058"></detailprice>
		<detailsize url="/ujp/api/v4/goods/30058"></detailsize>
		<detaildetail url="/ujp/api/v4/goods/30058"></detaildetail>
		<detailmiblebox url="/ujp/api/v4/search/goods/recommend?sc=goods30058"></detailmiblebox>
		<detailsizeshop></detailsizeshop>
		<detailfooter url="/ujp/api/v4/goods/30058"></detailfooter>
	</div>
	
	
</template>
<script>
	import Detailfooter from './detailfooter/detailfooter'
	import Detailheader from './detailheader/detailheader'
	import Detailmain   from './detailmain/detailmain'
	import Detailprice   from './detailprice/detailprice'
	import Detailsize    from './detailsize/detailsize'
	import Detailmiblebox from './detailmiblebox/detailmiblebox'
	import Detaildetail    from './detaildetail/detaildetail'
	import Detailsizeshop  from './detailsizeshop/detailsizeshop'
	export default{
		name:'detail',
		components:{
			Detailheader,
			Detailmain,
			Detailprice,
			Detailsize,
			Detaildetail,
			Detailmiblebox,
			Detailsizeshop,
			Detailfooter
		},
		data(){
			return{
				
			}
		}
		
		
	}
	
	
</script>
<style>
	
</style>
