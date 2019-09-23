<template>
	<div id="app">
		<headerNav/>
		<router-view />
		<footerNav/>
	</div>
</template>

<script>
	import headerNav from '@/components/header_nav'
	// import main from '@/components/main'
	import footerNav from '@/components/footer_nav'
	export default {
		name: 'App',
		data () {
			return {
				
			}
		},
		created() {
			
		},
		components: {
			headerNav, footerNav
		}
	}
</script>

<style>
	* {
		margin: 0;
		padding: 0;
		outline: none;
		appearance: none;
	}
	#app {
		width: 100%;
		min-width: 1200px;
	}
	.page-content {
		width: 1200px;
		margin: 0 auto;
		position: relative;
	}
</style>
