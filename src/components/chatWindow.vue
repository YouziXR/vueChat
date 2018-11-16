<template>
    <div id="chatWindow">
        <msgWindow class="msgWindow"></msgWindow>
        <inputWindow class="inputWindow"></inputWindow>
    </div>
</template>
<script type="text/javascript">
import msgWindow from './msgWindow'
import inputWindow from './inputWindow'
export default {
    name: 'chatWindow',
    components: {
    	msgWindow,
        inputWindow
    },
    data() {
    	return {
    	}
    },
    /*mounted: function () {
    	let that = this;
    	Bus.$on('currentMsg', function (userid, msg) {
    		that.message = msg.content;
    		that.sentTime = msg.sendTime.toLocaleString();
    	})
    }*/
}
</script>
<style type="text/css">
	#chatWindow {
        /*box-sizing: border-box;*/
		border: 1px solid #eee;
		border-radius: 0 5px 5px 0;
        box-sizing: border-box;
		width: 70%;
		height: 100%;
		float: right;
		margin-left: -5px;
        /*overflow: hidden;*/
	}
    /* .msgWindow {
        height: 65%;
        width: 99%;
    } */
    .inputWindow {
        /*height: 30%;*/
        /*width: 99%;*/
        box-sizing: border-box;
    }
</style>