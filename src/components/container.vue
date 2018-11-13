<template>
	<div id="container">
		<!-- div# -->
		<listBar></listBar>
	</div>
</template>
<script type="text/javascript">
	import listBar from './listBar'
	export default {
		name: 'container',
		components: {
			listBar,
		}
	}
</script>
<style type="text/css">
	#container {
		width: 800px;
		height: 580px;
		border: solid 1px #eee;
		border-radius: 3px;
		margin: 0 auto;
	}
</style>