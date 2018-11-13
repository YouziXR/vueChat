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
  font-family: 'Microsoft YaHei, Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  overflow-y: hidden;
  /*margin-top: 10px;*/
}
</style>
