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
  name: 'App',
  methods: {
    sbt: function() {
      this.$http.get("/v1/restserver/ting?type=1&size=30&offset=0&method=baidu.ting.billboard.billList").then(m=>console.log(m));
      
      //this.axios.get('/api/project/5ed359902945ea2cfa292b98', {

      //}).then(function(response){
      //  console.log(response);
      //});
    }
  }
}

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
