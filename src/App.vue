<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.JS SICK-App"/>
    <Hello name="Jonathan"/>
    <Hello name="Timothy"/>
    <Hello name="Mom"/>
    <Hello name="Sara"/>
    <RollItem num="12"/>
    <RollList v-bind:nums="[8,9,10]"/>
    <h1>SOMETHING OBVIOUS!!</h1>

  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Hello from './components/Hello.vue'
import RollItem from './components/RollItem.vue'
import RollList from './components/RollList.vue'

// let numsList = [8,9,10]

export default {
  name: 'App',
  props: {
    computed: {
      numsList() {
        return [8,9,10]
      }
    }
  },
  components: {
    HelloWorld,
    Hello,
    RollItem,
    RollList
  }
}
/*

  props: {
    computed: {
      
      return [8,9,10]
    }
  },
*/
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



