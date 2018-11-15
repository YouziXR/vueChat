<template>
	<textarea placeholder="press enter to send message">
		</textarea>
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
/* box-sizing: border-box; */
/*width: 100%;*/
/*margin-left: -5px;*/
textarea {
	/* height: 30%; */
	border-bottom-right-radius: 4px; 
	background-color: #fff;
	/* padding: 10px; */
	/* padding-left: 10px; */
	height: 30%;
	width: 99%;
	/* margin: 90px; */
	margin-left: -1px;
	border-top: none;
	border-left: none;
	border-right: 3px solid #fff;
	border-bottom:5px solid #fff;
	outline: none;
	font-family: "Micrsofot Yahei";
	resize: none;
}

</style>
