<template>
  <div id="app">
    <button v-on:click="sbt">访问跨域</button>

    <img src="./assets/logo.png">
    <router-view/>
  </div>
</template>

<script>
import axios from 'axios'
import VueAxios from 'vue-axios'

export default {
  name: 'App'
}

new Vue({
  el: '#app',
  data: {
    message: 'abdd'
  },
  methods: {
    sbt: function() {
      this.axios.get('/api/project/5ed359902945ea2cfa292b98', {

      }).then(function(response){
        console.log(response);
      });
    }
  }
})
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
