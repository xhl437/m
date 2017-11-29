<template>
	<div class="detailsize">
		<div class="g-action-container mt10" @click="">灰色&nbsp;&nbsp;均码</div>
		<div class="g-section g-country g-brank">

			<a href="/v4/brand/5e3b3b57f4cc4ab7b67d2dc39134bd2b">
				<div class="g-brank-t">
					<div class="b_logo"><img src="http://img1.ujipin.com/8cbd4df177d1920fbdf314003421d4eb?UCloudPublicKey=ucloudjiawoyong@ujipin.cn14466281690001077321672&amp;Expires=1511496085&amp;Signature=0j0S6pekyCmRqocG40BnFq1keeQ=&amp;format=JPEG"></div>
					<div class="b_name">
						<div class="brand">日光生活</div>
						<div class="name"><span>中国台湾</span><em>最实惠最优质的日系家居</em></div>
					</div>
				</div>
				<div class="g-brank-more">查看在售商品216件</div>
			</a>
		</div>

		<div class="g-section g-attribute">
			<div class="t">商品属性</div>
			<div class="g-attr-box">
				<table width="100%" border="0" cellpadding="0" cellspacing="0">

					<tr>
						<td class="titles">材质</td>
						<td class="con">棉</td>
					</tr>
					<tr>
						<td class="titles">尺寸</td>
						<td class="con">直径48cm 高30cm </td>
					</tr>
					<tr>
						<td class="titles">净重</td>
						<td class="con">990g</td>
					</tr>
				</table>
			</div>
			<div class="more"><span></span></div>
		</div>

	</div>

</template>
<script>
	import axios from 'axios'
	import Swiper from 'swiper'
	export default {
		name: 'detailsize',
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
					
					that.datas = res.data
					
				})
			}
		},
		created() {
			this.getBanners()
		}

	}
	
	
	
</script>
<style lang="scss">
	td, th {
	    display: table-cell;
	    vertical-align: inherit;
	}
	
	a {
		text-decoration: none;
		color: #4F494B;
	}
	i, em {
	    font-style: normal;
	}
	
   
	.g-action-container:after {
	    content: "";
	    float: right;
	    margin-top: 15px;
	    width: 22px;
	    height: 22px;
	    background: url("https://ss3.bdstatic.com/70cFv8Sh_Q1YnxGkpoWK1HF6hhy/it/u=756318008,2510646187&fm=27&gp=0.jpg") no-repeat center;
	    background-size: 100%;
	}

	.g-brank:after {
    top: 35px;
}

.g-brank:after {
    content: '';
    position: absolute;
    right: 16px;
    top: 16px;
    width: 22px;
    height: 22px;
    background: url("https://ss3.bdstatic.com/70cFv8Sh_Q1YnxGkpoWK1HF6hhy/it/u=756318008,2510646187&fm=27&gp=0.jpg") no-repeat;
    background-size: 100%;
}






	
	
	.g-action-container {
		line-height: 52px;
		font-size: 13px;
		background: #fff;
		padding: 0 16px 0 16px;
		position: relative;
	}
	
	.mt10 {
		margin-top: 10px;
	}
	
	.g-country {
		position: relative;
		padding-top: 0;
		a{
			display: block;
			.g-brank-t {
				padding: 16px;
				overflow: hidden;
				.b_logo {
					width: 53px;
					height: 53px;
					border-radius: 50%;
					float: left;
					margin-right: 16px;
					img {
						border-radius: 50%;
						 width: 100%;
					}
				}
				
				.b_name{
					.brand {
					    font-size: 14px;
					    margin-bottom: 8px;
					    padding-top: 7px;
					    color: #4F494B;
					}
					
					.name {
					    font-size: 14px;
					    height: 18px;
					    color: #B3B3B3;
					    overflow: hidden;
					    white-space: nowrap;
					    text-overflow: ellipsis;
					    width: 70%;
					    span {
						    font-size: 12px;
						    margin-right: 8px;
						    padding-left: 18px;
						    position: relative;
						    display: inline-block;
						    line-height: 18px;
						     em {
								    font-size: 12px;
								}
						    
						}
					    
					}
				} 
				
			}
			.g-brank-more {
			    height: 44px;
			    line-height: 44px;
			    text-align: center;
			    color: #4F494B;
			    border-top: 1px solid #E6E6E6;
			}
			
		}
	}
	
	.g-section {
		background: #fff;
		margin-top: 10px;
		padding-top: 8px;
	}
	
	.g-attribute{
	    
	    .titles {
					    width: 50px;
					    text-align: center;
					    border-right: 1px solid #EDEDED;
					}
					td {
					    padding: 13px 5px;
					    line-height: 20px;
					}
	    .t {
		    color: #4F494B;
		    font-size: 17px;
		    line-height: 38px;
		    padding-left: 16px;
		}
		.g-attr-box{
			 table {
			    table-layout: fixed;
			    word-wrap: break-word;
			    border-top: 1px solid #EDEDED;
			    tr {
				    border-bottom: 1px solid #EDEDED;
				    
					
				    
				}
			    
			}
			
		}
		.more {
		    height: 48px;
		    text-align: center;
		    display: none;
		    border-top: 1px solid #EDEDED;
		    -webkit-tap-highlight-color: rgba(0,0,0,0);
		}
	    
	}
	
	
</style>