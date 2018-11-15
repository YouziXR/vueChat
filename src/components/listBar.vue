<template>
  <div id="listBar">
    <headPhoto></headPhoto>
    <input type="text" name="searchUser" placeholder="press enter to search user" v-model.lazy="searchVal">
    <chatList></chatList>
  </div>
</template>
<script type="text/javascript">
import headPhoto from './headPhoto'
import chatList from './chatList'
export default {
  name: 'listBar',
  components: {
    headPhoto,
    chatList
  },
  data() {
  	return {
  		searchVal: '',
  	}
  },
  watch: {
  	searchVal: function (value) {
      console.log(`searchVal: ${value}`);
      console.log(`searchVal: ${this.searchVal}`);
    }
  }
}

</script>
<style type="text/css">
#listBar {
  /*border: solid 1px #eee;*/
  /*overflow: hidden;*/
  /*display: inline-block;*/
  float: left;
  box-sizing: border-box;
  height: 100%;
  width: 30%;
  background-color: rgba(46, 50, 56, 0.8);
  color: #ddbdff;
  border-radius: 5px 0 0 5px;
  /*font-size: 1.2em;*/
}
input {
	color: #ff748c;
	padding: 10px;
	box-sizing: border-box;
	width: 90%;
	height: 30px;
	border-radius: 3px;
	background-color: #26292E;
	border: 0.5px solid #3A3A3A;
  margin-bottom: 10px;
  outline: none;
}

</style>