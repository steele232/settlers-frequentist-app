<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.JS SICK-App"/>
    <Hello name="Jonathan"/>
    <Hello name="Timothy"/>
    <Hello name="Mom"/>
    <Hello name="Sara"/>
    <h1>SOMETHING OBVIOUS!!</h1>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Hello from './components/Hello.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Hello
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
