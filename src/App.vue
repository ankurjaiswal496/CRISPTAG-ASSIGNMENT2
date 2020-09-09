<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="convert string to upper case"/>
    <input type="text" v-model="message" />
  <h4>{{ message | uppercase }}</h4>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
vue.filter('uppercase', function (value) {
	return value.toUpperCase()
})

new Vue({
	el: '#app',
  data: {message: 'coligo.io'
  }
})

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
