<template>
	<div class="header_nav">
		<div class="page-content">
			<el-row :gutter="20" align="middle" type="flex">
				<el-col :span="5">
					<div class="grid-content bg-purple">
						<img src="../assets/logo.png" alt="LOGO" class="logo">
					</div>
				</el-col>
				<el-col :span="19">
					<div class="nav-item">
						<span :class="[index == active ? 'active' : '']" v-for="(item, index) in nav_list" :key="index" v-html="item.name"></span>
					</div>
				</el-col>
			</el-row>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'header_nav',
		data () {
			return {
				nav_list: [
					{name: '首页', path: '/'},
					{name: '企业介绍', path: '/'},
					{name: '企业服务', path: '/'},
					{name: '新闻中心', path: '/'},
					{name: '合作商家', path: '/'},
					{name: '联系我们', path: '/'}
				],
				active: 0
			}
		}
	}
</script>

<style scoped>
	.header_nav {
		width: 100%;
		position: sticky;
		top: 0;
		z-index: 2;
		background-color: #011222;
	}
	.logo {
		width: 124px;
	}
	.nav-item {
		font-size: 14px;
		color: #fff;
		text-align: right;
		-webkit-user-select: none;
	}
	.nav-item .active, .nav-item span:hover {
		color: #00BCD4;
	}
	.nav-item span {
		cursor: pointer;
		margin-left: 65px;
	}
	.align-r {
		text-align: right;
	}
</style>
