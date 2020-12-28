<template>
  <div id="app">
    <div class="top-histogram">
      Placeholder for Histogram
    </div>
    <div class="left-button-fields">
      <button>Placeholder 1</button>
      <button>Placeholder 2</button>
      <button>Placeholder 3</button>
      <button>Placeholder 4</button>
    </div>
    <div class="right-roll-list">
      <RollList :nums="global_list"/>
    </div>

  </div>
</template>

<script>
import RollList from './components/RollList.vue'

export default {
  name: 'App',
  data() {
    return {
      global_list: [1,2,3,4,5,6,7]
    }
  },
  props: {
  },
  components: {
    RollList
  }
}
</script>

<style>

* {
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
}

.top-histogram {
  padding: 10%;
  text-align: center;
  background-color: #EAEAEA;
}

.left-button-fields {
  width: 75%;
  float: left;
  padding: 40px;
}

.right-roll-list {
  width: 25%;
  float: right;
}


</style>



