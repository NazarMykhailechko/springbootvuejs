<template>
  <div id="app">
    <img src="./assets/logo.png" alt="">
    <login @register="register($event)"/>
    <h3>your login is {{data.login}}</h3>
    <h3>your password is {{data.password}}</h3>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Login from './components/Login.vue'

export default {
  name: 'App',
  data(){
    return {
      data: {
        login: '',
        password:''
      }

    }
  },
  components: {
    Login
  },
  methods:{
    register(data){
        this.data = data
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
