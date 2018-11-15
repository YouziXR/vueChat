<template>
  <div id="app">
    <!-- <img src="./assets/logo.png"> -->
    <!-- <router-view/> -->
    <container></container>
  </div>
</template>

<script>
import container from './components/container'
export default {
  name: 'App',
  components: {
    container,
  }
}
</script>

<style>
* {
  /*border: 1px solid #eee;*/
}
#app {
  background-image: url('./assets/images/bg.jpg');
  width: 1366px;
  height: 768px;
  font-family: 'Microsoft YaHei, Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  padding-top: 20px;
  margin-top: -20px;
  padding-left: 20px;
  margin-left: -20px;
  /*margin-top: 10px;*/
}
/* #app::-webkit-scrollbar {
  display: none;
} */
</style>
