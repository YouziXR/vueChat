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
		background-image: url('../assets/images/bg.jpg');
		/*padding: 90px;*/
		padding-left: 20px;
		margin-left: -20px;
		margin-top: -30px;
		padding-top: 30px;
		margin-right: -20px;
		padding-right: 20px;
		width: 800px;
		height: 580px;
		border: solid 1px #eee;
		border-radius: 3px;
		margin: 0 auto;
		margin-top: 20px;
	}
</style>