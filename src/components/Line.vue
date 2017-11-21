<template>
	<div>
		<h1>{{ title }}</h1>
    	<charts :options="datas"></charts>
	</div>
</template>

<script>
	export default {
		mane: 'Line',
		data () {
			return {
				title: 'Line'
			}
		},
		components : {
		    charts: require('vue-echarts')
		}
	}
</script>

<style scoped>
	
</style>