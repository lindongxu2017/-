<template>
	<div class="footer_nav">
		<div class="page-content">
			<el-row style="padding-bottom: 70px;">
				<el-col :span="7">
					<div class="col-content">
						<div class="cell-title">联系我们</div>
						<div class="cell-info">
							<!-- <div class="icon-wapper"></div> -->
							<img src="@/assets/phone.png" class="icon">
							<div class="text">手机: 0755-33100002</div>
						</div>
						<div class="cell-info">
							<!-- <div class="icon-wapper qq"></div> -->
							<img src="@/assets/qq.png" class="icon">
							<div class="text">QQ: <span>971689800</span></div>
						</div>	
						<div class="cell-info">
							<!-- <div class="icon-wapper email"></div> -->
							<img src="@/assets/mail.png" class="icon">
							<div class="text">邮箱: <span>xkq@qinhantangtop.com</span></div>
						</div>
						<div class="cell-info">
							<!-- <div class="icon-wapper site"></div> -->
							<img src="@/assets/web.png" class="icon">
							<div class="text">网站: <span>www.qinhantangtop.com</span></div>
						</div>
					</div>
				</el-col>
				<el-col :span="7" :offset="2">
					<div class="col-content">
						<div class="cell-title no-before"></div>
						<div class="cell-info">
							<img src="../assets/location.png" alt="ICON" class="icon">
							<div class="text">Address:</div>
							<div class="text">深圳市龙岗区坂田五和大道南3号富奇创意大厦601</div>
						</div>
					</div>
				</el-col>
				<el-col :span="5" :offset="3">
					<div class="col-content">
						<div class="cell-title">发送邮件</div>
						<div class="cell-info">
							<el-input placeholder="你的名字" v-model="form.name">
								<img style="width: 16px; margin: 11px 5px 0;" src="@/assets/phone_2.png" slot="suffix">
							</el-input>
							<el-input placeholder="你的邮箱" v-model="form.email">
								<img style="width: 16px; margin: 11px 5px 0;" src="@/assets/mai_2.png" slot="suffix">
							</el-input>
							<el-input placeholder="内容" type="textarea" v-model="form.content"></el-input>
							<el-button class="confirm" type="info" @click.native="send">发送邮件</el-button>
						</div>
					</div>
				</el-col>
			</el-row>
		</div>
		<div class="record">
			<div class="page-content">
				<el-row>
					<el-col :span="7" v-if="is_top" @click.native="route">
                        <span class="info">粤ICP备15058459号-1</span>
                    </el-col>
					<el-col :span="7" v-else @click.native="route">
                        <span class="info">粤ICP备15058459号-2</span>
                    </el-col>
					<el-col :span="8" :offset="1">
						<div class="links">
							<span>支持</span>
							<span>联系我们</span>
							<span>隐私政策</span>
						</div>
					</el-col>
					<el-col :span="7" :offset="1" style="text-align: right;">版权所有@深圳市勤瀚堂电子商务公司</el-col>
				</el-row>
			</div>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'footer_nav',
		data() {
			return {
				form: {
					name: '',
					email: '',
					content: '',
				},
                is_top: false
			}
		},
        mounted () {
            if (location.href.indexOf('www.qinhantangtop.com') > -1) {
                this.is_top = true
            } else {
                this.is_top = false
            }
        },
		methods: {
			send () {
				this.form = {
					name: '',
					email: '',
					content: ''
				}
			},
            route () {
                location.href = 'http://www.beian.miit.gov.cn'
            }
		}
	}
</script>
<style>
	.el-input, .el-textarea {
		width: 264px;
		margin-bottom: 14px;
	}
	.el-textarea__inner {
		height: 97px;
		resize: none;
	}
	.el-input__inner, .el-textarea__inner {
		background-color: #181828;
		border-color: #2C3A4C;
		color: #99A9B5;
	}
	.el-input.is-active .el-input__inner, .el-input__inner:focus, .el-input__inner:hover, .el-textarea__inner:focus, .el-textarea__inner:hover {
		border-color: #049DB3;
	}
	.el-input__inner::-webkit-input-placeholder, .el-textarea__inner::-webkit-input-placeholder {
		color: #494A59;
	}
	.el-input__inner:-moz-placeholder, .el-textarea__inner:-moz-placeholder {
		color: #494A59；
	}
	.el-input__inner::-moz-placeholder, .el-textarea__inner::-moz-placeholder {
		color: #494A59；
	}
	.el-input__inner:-ms-input-placeholder, .el-textarea__inner:-ms-input-placeholder {
		color: #494A59；
	}
	.el-button {
		width: 264px;
		background-color: #394050;
		color: #99A9B5;
		border-color: #394050;
	}
	.el-button--info:focus, .el-button--info:hover, .el-button--info.is-active {
		background: rgba(44,58,76,0.5);
	}
</style>
<style scoped>
	.footer_nav {
		width: 100%;
		overflow: hidden;
		background-color: #072A40;
		padding: 50px 0 0;
		color: #99A9B5;
	}
	.col-content {
		/* padding: 0 15px; */
	}

	.cell-title {
		margin-bottom: 42px;
		color: #fff;
		font-size: 16px;
		font-weight: bold;
		height: 20px;
		line-height: 20px;
		display: inline-block;
		position: relative;
	}
	.cell-title.no-before {
		opacity: 0;
	}
	.cell-title:before {
		content: '';
		position: absolute;
		right: -15px;
		bottom: -2px;
		transform: rotate(-45deg);
		width: 0;
		border: 5px solid;
		border-color: transparent #F50057 transparent transparent;
	}

	.cell-info {
		margin-bottom: 10px;
		/* display: inline-block; */
		white-space: normal;
	}
	
	.icon-wapper {
		width: 17px;
		height: 17px;
		vertical-align: middle;
		margin-right: 10px;
		display: inline-block;
		background-image: url('../assets/sprite.png');
		background-repeat: no-repeat;
		background-size: 100%;
		overflow: hidden;
	}
	.icon-wapper.qq {
		background-position: 0 -31px;
	}
	.icon-wapper.email {
		background-position: 0 -63px;
	}
	.icon-wapper.site {
		background-position: 0 -95px;
	}

	.icon {
		width: 17px;
		height: 17px;
		vertical-align: middle;
		margin-right: 10px;
	}

	.text {
		font-size: 14px;
		vertical-align: middle;
		display: inline-block;
		line-height: 25px;
	}

	.text span {
		color: #00BCD4;
	}
	.record {
		background-color: #181828;
		height: 100px;
		color: #99A9B5;
		font-size: 14px;
		box-sizing: border-box;
		padding-top: 40px;
	}
	.links {
		font-size: 0;
		vertical-align: middle;
		display: inline-block;
	}
	.links > span {
		display: inline-block;
		padding: 0 30px;
		border-right: 1px solid #2C2A3E;
		font-size: 14px;
		cursor: pointer;
	}
    .info {
        cursor: pointer;
    }
</style>
