<template>
	<div id="container">
		<!-- div# -->
		<listBar></listBar>
		<chatWindow></chatWindow>

	</div>
</template>
<script type="text/javascript">
import listBar from './listBar'
import chatWindow from './chatWindow'

export default {
	name: 'container',
	components: {
		listBar,
		chatWindow,
	}
}

</script>
<style type="text/css">
#container {
	width: 800px;
	height: 580px;
	/*border: solid 1px #eee;*/
	/*border-radius: 3px;*/
	margin: 0 auto;
	margin-top: 20px;
}

</style>
