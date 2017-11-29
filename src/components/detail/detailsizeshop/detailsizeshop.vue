<template>

	<div class="choice-attr-box block">
		<div class="attr-box">
			<div class="attr-con">
				<div class="summary bt_dedede">
					<div class="img"><img src="http://img1.ujipin.com/f84ca0770f97c21c11a5459c49a8c6d8?UCloudPublicKey=ucloudjiawoyong@ujipin.cn14466281690001077321672&amp;Expires=1511591919&amp;Signature=o1IXVLjqUcGeqBJlN4aMzjGREms=&amp;width=200&amp;iopcmd=thumbnail&amp;type=4&amp;format=JPEG"></div>
					<div class="main">
						<div class="titlea">[ 承载手艺人满满诚意 ] 日光生活 棉质编织提手收纳篮</div>
						<div class="price"><span class="now">¥109.00</span>
							<!-- <span class="old">¥90</span> --></div>
					</div>
				</div>
				<div class="properties">
					<div class="property color-classify bt_dedede">
						<div class="t">花色</div>
						<div class="items"><label key_value="彩色" key="花色">彩色</label><label key_value="灰色" key="花色" class="checked">灰色</label></div>
					</div>
					<div class="property color-classify bt_dedede">
						<div class="t">尺寸</div>
						<div class="items"><label key_value="均码" key="尺寸" class="checked">均码</label></div>
					</div>
				</div>
				<!-- <div class="property color-classify bt_dedede">
               <div class="t">颜色分类</div>
               <div class="items">
                   <label class="checked">颜色</label><label>颜色</label><label>颜色</label>
               </div>
           </div> -->

				<div class="property number bt_dedede" style="transform-origin: 0px 0px 0px; opacity: 1; transform: scale(1, 1);">
					<div class="t">数量</div>
					<div class="content clearfix pos">
						<div class="number-control">
							<button type="button" class="decrease over">-</button>
							<input type="tel" class="num" value="1" disabled="disabled">
							<button type="button" class="increase">+</button>
						</div>
						<div class="tips" style="display: none;">该商品库存被你买光啦！</div>
					</div>
				</div>
			</div>
			<div class="add-cart">加入购物袋</div>
			<div class="close_attr-box"></div>
		</div>
	</div>

</template>

<script>
	export default {
		name: 'detailsizeshop',
		data() {
			return {

			}
		}
	}
</script>

<style lang="scss">
	div {
		display: block;
	}
	
	button,
	select {
		text-transform: none;
	}
	
	button {
		overflow: visible;
	}
	
	.choice-attr-box {
		width: 90%;
		height: 90%;
		background: #fff;
		border-radius: 5px;
		position: fixed;
		left: 5%;
		top: 5%;
		z-index: 12;
		transition: all .3s;
		-webkit-transition: all .3s;
		display: none;
		.attr-box {
			width: 100%;
			height: 100%;
			position: relative;
			.attr-con {
				position: absolute;
				left: 0;
				top: 0;
				bottom: 90px;
				right: 0;
				overflow: auto;
				-webkit-overflow-scrolling: touch;
				.close_attr-box {
					position: absolute;
					right: 0;
					top: 0;
					width: 40px;
					height: 40px;
					background-size: 50%;
				}
				.add-cart {
					position: absolute;
					bottom: 20px;
					width: 90%;
					height: 50px;
					line-height: 50px;
					margin: 0 5%;
					font-size: 17px;
					background: #E74C3C;
					color: #fff;
					text-align: center;
					border-radius: 5px;
				}
				.number {
					.tips {
						float: left;
						color: #E74C3C;
						line-height: 24px;
					}
				}
				.summary {
					height: 90px;
					padding: 20px 16px;
					box-sizing: border-box;
					height: auto;
					.img {
						width: 90px;
						height: 90px;
						float: left;
					}
					.main {
						padding-left: 112px;
						.titlea {
							font-size: 17px;
							color: #4F494B;
							-webkit-line-clamp: 2;
							-webkit-box-orient: vertical;
							overflow: hidden;
							display: -webkit-box;
							height: 40px;
							line-height: 20px;
							padding-right: 20px;
						}
						.price {
							margin-top: 28px;
							.now {
								color: #E74C3C;
								font-size: 18px;
								margin-right: 8px;
							}
						}
					}
				}
				.bt_dedede {
					border-bottom: 1px solid #DEDEDE;
				}
				
				.property {
					padding: 20px 16px;
					overflow: hidden;
					.t {
						margin: 0 0 4px 0;
						font-size: 13px;
						color: #4F494B;
						display: block;
					}
					.pos{
						position:static;
						overflow: hidden;
					}
					.content {
						margin-top: 12px;
						.number-control {
							float: left;
							margin-right: 12px;
							.over {
								border: 1px solid #E6E6E6;
								color: #E6E6E6;
							}
							.decrease,
							.increase {
								float: left;
								-webkit-user-select: none;
								-ms-user-select: none;
								width: 24px;
								height: 24px;
								background: none;
								border: 1px solid #4F494B;
								color: #4F494B;
								border-radius: 3px;
								text-align: center;
							}
							.num {
								float: left;
								width: 30px;
								height: 24px;
								line-height: 24px;
								text-align: center;
								padding: 0 10px;
							}
						}
					}
				}
				.bt_dedede {
					border-bottom: 1px solid #DEDEDE;
				}
				.color-classify {
					.items {
						label {
							display: inline-block;
							padding: 9px 14px;
							border: 1px solid #4F494B;
							border-radius: 3px;
							text-align: center;
							margin: 12px 12px 0 0;
							color: #4F494B;
						}
						.checked {
							background: #E74C3C;
							border: 1px solid #E74C3C;
							color: #fff;
						}
					}
				}
			}
		}
	}
	
	.add-cart {
	    position: absolute;
	    bottom: 20px;
	    width: 90%;
	    height: 50px;
	    line-height: 50px;
	    margin: 0 5%;
	    font-size: 17px;
	    background: #E74C3C;
	    color: #fff;
	    text-align: center;
	    border-radius: 5px;
	}
	
	.close_attr-box {
	    position: absolute;
	    right: 0;
	    top: 0;
	    width: 40px;
	    height: 40px;
	    background: url("https://gss2.bdstatic.com/9fo3dSag_xI4khGkpoWK1HF6hhy/baike/w%3D268%3Bg%3D0/sign=6173e44ecefc1e17fdbf8b3772ab913e/d4628535e5dde711b23510aea6efce1b9c166186.jpg") center no-repeat;
	    background-size: 50%;
	}
	
	
	/*.block {
		display: block!important;
	}*/
</style>