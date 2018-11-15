<template>
	<div id="" class="text">
		<textarea placeholder="press enter to send message">

		</textarea>
	</div>
</template>
<script type="text/javascript">
// import name from './name'
export default {
	name: 'inputWindow',
	components: {

	}
}

</script>
<style lang="less" scoped>
.text {
	/*height: 30%;*/
	border-top: solid 1px #ddd;
	background-color: #fff;
	box-sizing: border-box;
	/*width: 100%;*/
	/*margin-left: -5px;*/
	textarea {
		// padding: 10px;
		// padding-left: 10px;
		height: 100%;
		width: 100%;
		border: none;
		outline: none;
		font-family: "Micrsofot Yahei";
		resize: none;
	}
}

</style>
