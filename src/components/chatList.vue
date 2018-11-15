<template>
	<div id="chatlist">
		<button id="chatBtn" v-for="chatter in chatters" :key="chatter.userid" :class=" {active: currentID === chatter.userid} " @click="selectChatter(chatter.userid, chatter.message)">
			<img class="img" :src="chatter.head">
			<p class="p"> {{ chatter.name }} </p>
		</button>
	</div>
</template>
<script type="text/javascript">
import Bus from './Bus.js'
export default {
	name: 'chatList',
	components: {

	},
	data() {
		return {
			chatters: [],
			currentID: null,
		}
	},
	created: function() {
		// get chat list
		let firstUser = {
			userid: 1,
			name: 'ayou',
			head: require('../assets/images/2.png'),
			message: [{
				content: '1st test msg',
				sendTime: new Date(),
			}]
		}
		let secondUser = {
			userid: 2,
			name: 'ayou',
			head: require('../assets/images/3.jpg'),
			message: [{
					content: '2nd test msg',
					sendTime: new Date(),
				},
				{
					content: '3rd test msg',
					sendTime: new Date(),
				}
			]
		}
		this.chatters.push(firstUser);
		this.chatters.push(secondUser);
	},
	methods: {
		selectChatter: function(userid, message) {
			this.currentID = userid;
			Bus.$emit('currentMsg', userid, message);
		}
	}
}

</script>
<style type="text/css">
button {
	/*float: left;*/
	padding-top: 5px;
	border: none;
	width: 100%;
	outline: none;
	background-color: rgba(0, 0, 0, 0);
	/*font-size: 1em;*/
}

button:hover {
	background-color: rgba(255, 255, 255, 0.03);
}

button.active {
	background-color: rgba(255, 255, 255, 0.1);
}

.img {
	/*margin-top: 10px;*/
	margin-left: 5%;
	height: 40px;
	width: 40px;
	/*vertical-align: middle;*/
	float: left;
	/*padding-left: 10px;*/
	/*display: inline-block;*/
	border-radius: 5px;
}

.p {
	float: left;
	margin-top: 10px;
	display: inline-block;
	font-size: 16px;
	color: #ddbdff;
	/*margin-left: 20px;*/
	/*text-align: center; */
	/*vertical-align: middle;*/

}

</style>
