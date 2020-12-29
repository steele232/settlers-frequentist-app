<template>
  <div id="app">
    <div class="top-histogram">
      <Histogram :nums="global_roll_list"/>
    </div>
    <div class="left-button-fields">
      <span v-for="(num, index) in possible_rolls" :key="index">
        <button class="num-button" v-on:click="global_roll_list.push(num)">{{num}}</button>
      </span>
    </div>
    <div class="right-roll-list">
      <RollList :nums="global_roll_list"/>
    </div>
  </div>
</template>

<script>
import RollList from './components/RollList.vue'
import Histogram from './components/Histogram.vue'

export default {
  name: 'App',
  data() {
    return {
      global_roll_list: [],
      possible_rolls: [2,3,4,5,6,7,8,9,10,11,12]
    }
  },
  methods: {
  },
  components: {
    RollList,
    Histogram
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
  /* text-align: center; */
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

.num-button {
  padding: 15px;
  margin: 10px;
  border-radius: 5px;
}

</style>



