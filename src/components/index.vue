<template>
	<div class="hello">
		<div class="section">
			<img class="img-bg" src="../assets/screen_1.jpg">
			<div class="section-content">				
				<div class="page-content">
					<div class="cell-title">E-MERCHANT OF TWINKLE</div>
					<div class="cell-subtitle">致力于成为一家为企业智慧经营全面赋能的数据实现科技公司</div>
					<div class="cell-tips">A CREATIVE & DIGITALAGENCY</div>
				</div>
			</div>
		</div>
		<div class="section">
			<img class="img-bg" src="../assets/screen_2.jpg">
			<div class="section-content-normal">
				<div class="page-content full">
					<div class="section-title">
						<div class="title-en">ABOUT US</div>
						<div class="title-cn">关于我们</div>
					</div>
					<div class="about-us-intro">
						<div class="short-line"></div>
						<div class="text">							
							<div class="intro-title">全方位技术赋能整合公司</div>
							<div class="intro-text">为企业提供开发、运营、推广、督导培训等一站式商务解决方案和网络营销服务，协助品牌商家打通全球商务销售链条，完善销售渠道，通过互联网快速提升企业品牌价值。</div>
						</div>
					</div>
				</div>
			</div>
		</div>
		<div class="section">
			<div class="flex-wrap">
				<div class="card-item">
					<img src="@/assets/view_bg.jpg">
					<div class="card-content">
						<img src="@/assets/view.png">
						<div class="card-title">视觉设计</div>
						<div class="card-subtitle">美是一种生产力，美也是一种竞争力，为企业解决问题而设计——产品视觉和体验，网站交互设计、图标设计、移动应用UI、ICON设计等。</div>
					</div>
				</div>
				<div class="card-item center">
					<img src="@/assets/system_bg.jpg">
					<div class="card-content">
						<img src="@/assets/system_icon.png">
						<div class="card-title">系统研发</div>
						<div class="card-subtitle">支持小程序、APP系统开发，为客户链接线上用户，提供更加垂直和专业的行业解决方案，满足企业的业务需求。</div>
					</div>
				</div>
				<div class="card-item">
					<img src="@/assets/sales_bg.jpg">
					<div class="card-content">
						<img src="@/assets/sales_icon.png">
						<div class="card-title">整合营销</div>
						<div class="card-subtitle">我们倡导现代企业通过改善经营管理，建立起完善的服务价值链，以“软性”延伸价值去实现消费者满意目标。</div>
					</div>
				</div>
			</div>
		</div>
		<div class="section">
			<div class="work">
				<div class="page-content full">
					<div class="section-title">
						<div class="title-en">OUR WORKS</div>
						<div class="title-cn">产品研发</div>
					</div>
					<div class="product-wrapper">
						<div class="item">
							<img src="../assets/bg_1.jpg">
							<div class="product-content">
								<img class="product-logo" src="@/assets/logo_reverse.png">
								<div class="product-name">医美系统研发</div>
								<div class="product-intro">基于人工智能大数据体系，在智能精准营销、人脉极速裂变、用户精准画像、资源高效管理的模式下，打造出低成本获客、高品质成交、超便捷运营的智能医美系统。</div>
								<div class="check-more">了解更多</div>
							</div>
						</div>
						<div class="item">
							<img src="../assets/product_bg_1.jpg">
							<div class="product-content">
								<img class="product-logo" src="@/assets/logo_reverse.png">
								<div class="product-name" style="margin-top: -12px;">物业研发</div>
								<div class="product-intro">依据物业管理人员日常工作而设计、贴近其工作流程，使整个管理工作更加系统、规范，大大提高了物业管理人员工作质量和工作效率。</div>
								<div class="check-more">了解更多</div>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
		<div class="section">
			<div class="qr-code">
				<div class="page-content full qr-flex-wrap">
					<div class="scanning">
						<div class="qr-title">扫码关注</div>
						<div class="qr-intro">
							<div>* Personal data will be encrypted</div>
							<div>扫描右侧二维码，关注公司最新动态</div>
						</div>
					</div>
					<img src="@/assets/qr_code.png">
				</div>
			</div>
		</div>
		<div class="scroll-top" v-if="scrolltop > windowH" @click="scrollToTop">
			<span class="el-icon-arrow-up"></span>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'HelloWorld',
		data() {
			return {
				scrolltop: 0,
				windowH: 900
			}
		},
		mounted() {
			const self = this
			this.windowH = window.screen.height
			window.onscroll = function () {
				self.scrolltop = document.documentElement.scrollTop||document.body.scrollTop
			}
		},
		methods: {
			scrollToTop () {
				document.body.scrollTop = 0
				document.documentElement.scrollTop = 0
			}
		}
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	.full {
		height: 100%;
	}
	.section {
		font-size: 0;
		position: relative;
	}
	.img-bg {
		width: 100%;
	}
	.section-content, .section-content-normal {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		left: 0;
	}
	.section-content {
		display: flex;
		flex-direction: column;
		justify-content: center;
	}
	.cell-title {
		font-size: 87px;
		font-family: HelveticaNeue-Bold;
		font-weight: bold;
		color: rgba(255,255,255,1);
		line-height: 1;
		margin-bottom: 70px;
	}
	.cell-subtitle {
		font-size:35px;
		font-family:PingFang-SC-Bold;
		font-weight:bold;
		color:rgba(255,255,255,1);
		line-height: 1;
		margin-bottom: 20px;
	}
	.cell-tips {
		font-size:24px;
		font-family:HelveticaNeueLTPro-ThEx;
		font-weight:normal;
		color:rgba(255,255,255,1);
		line-height: 1;
	}
	.section-title {
		position: absolute;
		top: 15%;
		width: 100%;
		color:rgba(223,229,232,1);
		text-align: center;
	}
	.section-title .title-en {
		font-size: 36px;
		font-family:HelveticaNeue-Bold;
		font-weight:bold;
		color:rgba(223,229,232,1);
		letter-spacing: 2px;
		line-height: 1;
		margin-bottom: 15px;
	}
	.section-title .title-cn {
		font-size:30px;
		font-family:PingFang-SC-Regular;
		font-weight:400;
		color:rgba(223,229,232,1);
		line-height: 1;
	}
	.about-us-intro {
		position: absolute;
		top: 45%;
		display: flex;
		width: 45%;
		line-height: 50px;
		color:rgba(255,255,255,1);
	}
	.short-line {
		width: 125px;
		height: 0px;
		background-color: rgba(163,231,240,1);
		margin-top: 30px;
	}
	.text {
		flex: 1;
		padding-left: 70px;
	}
	.intro-title {
		font-size: 35px;
		font-family:PingFang-SC-Regular;
		font-weight:400;
		color:rgba(255,255,255,1);
		margin-bottom: 40px;
	}
	.intro-text {
		font-size:12px;
		font-family:PingFang-SC-Regular;
		font-weight:400;
		color:rgba(255,255,255,1);
		line-height:24px;
		opacity:0.6;
	}
	.flex-wrap {
		display: flex;
	}
	.card-item {
		flex: 1;
		position: relative;
		display: inline-block;
		font-size: 0;
	}
	.card-item.center {
		width: 34.7%;
	}
	.card-item img {
		width: 100%;
		height: 100%;
	}
	.card-content {
		position: absolute;
		width: 100%;
		height: 100%;
		display: flex;
		flex-direction: column;
		justify-content: space-around;
		align-items: center;
		top: 0;
		left: 0;
		padding: 5% 12%;
		box-sizing: border-box;
	}
	.card-content img {
		width: 90px;
		height: 90px;
	}
	.card-title {
		font-size: 28px;
		font-family:PingFang-SC-Bold;
		font-weight:bold;
		color:rgba(255,255,255,1);
		line-height:50px;
	}
	.card-subtitle {
		font-size: 16px;
		text-align: center;
		font-family:PingFang-SC-Regular;
		font-weight:400;
		color:rgba(240,243,242,1);
		line-height:28px;
	}
	.work {
		height: 1085px;
		background-color: #14354A;
	}
	.product-wrapper {
		position: absolute;
		top: 33%;
		font-size: 0;
		width: 100%;
	}
	.product-wrapper .item {
		width: 50%;
		display: inline-block;
		position: relative;
	}
	.product-wrapper .item > img {
		width: 100%;
		height: 100%;
	}
	.product-content {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		left: 0;
		box-sizing: border-box;
		padding: 60px;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}
	.product-logo {
		width: 80px;
		height: 76px;
		margin-left: -10px;
		margin-bottom: 15px;
	}
	.product-name {
		font-size:60px;
		font-family:PingFang-SC-Bold;
		font-weight:bold;
		color:rgba(255,255,255,1);
		line-height: 1;
		letter-spacing: 5px;
	}
	.product-intro {
		font-size:21px;
		font-family:PingFang-SC-Regular;
		font-weight:400;
		color:rgba(255,255,255,1);
		line-height:27px;
		margin-bottom: 25px;
	}
	.check-more {
		width: 155px;
		line-height: 45px;
		font-size: 16px;
		font-family:PingFang-SC-Bold;
		color:rgba(255,255,255,1);
		border:2px solid rgba(255, 255, 255, 1);
		border-radius:45px;
		text-align: center;
		user-select: none;
		cursor: pointer;
	}
	.qr-code {
		height: 208px;
		background-color: rgba(0,188,212,1);
		box-sizing: border-box;
		padding: 38px 0 33px;
	}
	.qr-flex-wrap {
		display: flex;
		justify-content: space-between;
	}
	.scanning {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}
	.qr-flex-wrap > img {
		width: 137px;
	}
	.qr-title {
		font-size:30px;
		font-family:PingFang-SC-Bold;
		font-weight:bold;
		color:rgba(255,255,255,1);
	}
	.qr-intro > div:first-child {
		font-size:14px;
		font-family:SourceSansPro-Regular;
		font-weight:400;
		color:rgba(240,243,242,1);
		opacity:0.46;
	}
	.qr-intro > div:last-child {
		font-size:16px;
		font-family:PingFang-SC-Regular;
		font-weight:400;
		color:rgba(255,255,255,1);
	}
	.scroll-top {
		position: fixed;
		right: 137px;
		bottom: 200px;
		background-color: #06060F;
		border-radius: 2px;
		width: 50px;
		height: 50px;
		color: #99A9B5;
		text-align: center;
		line-height: 47px;
	}
	.scroll-top:hover {
		opacity: 0.7;
		cursor: pointer;
	}
</style>
