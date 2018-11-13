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
    let that = this;
    that.headSrc = require('../assets/images/1.jpg');
    that.userName = 'youzi';
  },
  methods: {

  }
}

</script>
<style type="text/css">
#outer {
	float: left;
	margin-left: 10px;
	margin-top: 10px;
}
img {
	height: 50px;
	widows: 50px;
	vertical-align: middle;
	border-radius: 5px;
}
p {
	margin-left: 15px;
	display: inline-block;
	/* text-align: center; */
	vertical-align: middle;
}

</style>
