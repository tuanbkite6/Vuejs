<template>
  <img alt="Vue logo" src="./assets/logo.png">
<<<<<<< HEAD
  <InformationList :users = "users" @update-user="uset = $event"/>
=======
  <app-user></app-user>
>>>>>>> 27fbbb4a95eddc8c7edc81d3321178c9b7bd6eb9
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import User from './components/UserCard.vue'
export default {
  name: 'App',
  components: {
    HelloWorld,
   appUser : User
  }
}
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
