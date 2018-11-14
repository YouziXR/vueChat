<template>
  <div id="outer">
    <img v-bind:src="headSrc">
    <p>
      {{ userName }}
    </p>
  </div>
</template>
<script type="text/javascript">
// import name from 'name'
export default {
  name: 'headPhoto',
  components: {

  },
  data() {
    return {
      headSrc: /*require('../assets/images/1.jpg') */ '',
      userName: null,
    }
  },
  created: function() {
    // get user info
    // let that = this;
    this.headSrc = require('../assets/images/1.jpg');
    this.userName = 'youzi';
  },
  methods: {

  }
}

</script>
<style type="text/css">
#outer {
	float: left;
  /*width: 90%;*/
	margin-left: 5%;
	margin-top: 10px;
  margin-bottom: 5px;
  /*border: 1px solid #eee;*/
}
img {
	height: 50px;
	width: 50px;
	vertical-align: middle;
  /*padding-left: 10px;*/
  /*display: inline-block;*/
	border-radius: 5px;
}
p {
	display: inline-block;
  margin-left: 20px;
	 /*text-align: center; */
   /*vertical-align: middle;*/
   font-size: 20px;
}

</style>
