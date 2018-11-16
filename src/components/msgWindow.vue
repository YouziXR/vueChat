<template>
	<div class="message">
		<ul>
			<li v-for="msg in message" :key="msg.userid">
				<p class="time">
					<span>
					{{ /*msg.sendTime.getMonth()+':'+ msg.sendTime.getDay() +'-'+msg.sendTime.getHours()+':'+ msg.sendTime.getMinutes()*/ msg.sendTime.toLocaleString() }}
					</span>
				</p>
				<div class="main">
					<img class="avatar" :src="head">
					<div class="text">
						{{ msg.content }}
					</div>
				</div>
			</li>
		</ul>
	</div>
</template>
<script type="text/javascript">
import Bus from './Bus.js'
export default {
	name: 'msgWindow',
	components: {

	},
	data() {
		return {
			// userid: null,
			head: '',
			message: [],
		}
	},
	mounted: function() {
		let that = this;
		Bus.$on('currentMsg', function(head, msg) {
			that.head = head;
			that.message = msg;
			// that.userid = userid;
			// console.log(that.userid);
			// that.sentTime = msg.sentTime.toLocaleString();
		})
	}
}

</script>
<style lang="less" scoped>
li {
	list-style: none;
}

.message {
	padding: 10px 15px;
	overflow-y: scroll;
	height: 66.8%;
	/* border-radius: 0 5px 0 0; */
	border-top-right-radius: 5px;
	/*border-bottom: 1px solid #eee;*/
	background-color: #eee;

	li {
		margin-bottom: 15px;
	}

	.time {
		margin: 7px 0;
		text-align: center;

		>span {
			display: inline-block;
			padding: 0 18px;
			font-size: 12px;
			color: #fff;
			border-radius: 2px;
			background-color: rgba(220, 220, 220, 1);
		}
	}

	.main {
		text-align: left;
		margin-bottom: -10px;
		.avatar {
			width: 35px;
			height: 35px;
			float: left;
			// margin: 0 10px 0 -10px;
			margin-right: 15px;
			margin-left: -40px;
			border-radius: 3px;
		}

		.text {
			// float: left;
			display: inline-block;
			position: relative;
			padding: 0 10px;
			max-width: ~'calc(100% - 40px)';
			min-height: 30px;
			line-height: 2.5;
			font-size: 13px;
			font-family: "Microsoft Yahei";
			text-align: left;
			word-break: break-all;
			background-color: #fafafa;
			border-radius: 4px;

			&:before {
				content: " ";
				position: absolute;
				top: 9px;
				right: 100%;
				border: 6px solid transparent;
				border-right-color: #fafafa;
			}
		}
	}

	.self {
		text-align: right;

		.avatar {
			float: right;
			margin: 0 0 0 10px;
		}

		.text {
			// float: right;
			background-color: #b2e281;

			&:before {
				right: inherit;
				left: 100%;
				border-right-color: transparent;
				border-left-color: #b2e281;
			}
		}
	}
}

</style>
