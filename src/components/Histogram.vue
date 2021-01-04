<template>
  <div>
    <table>
      <tr>
        <td>Roll #: </td>
        <th v-for="(num, index) in possible_rolls" :key="index">
          <h1>{{ num }}</h1>
        </th>
      </tr>
      <tr>
        <td>Theoretical Probability: </td>
        <td v-for="(num, index) in possible_rolls" :key="index">
          <h2>{{ get_theoretical(num).toFixed(2) }}</h2>
        </td>
      </tr>
      <tr>
        <td>Experimental Probability: </td>
        <td v-for="(num, index) in possible_rolls" :key="index">
          <HistoColumn 
            :theoretical="get_theoretical(num)" 
            :experimental="get_experimental(nums, num) || 0"
          />
        </td>
      </tr>
    </table>
  </div>
</template>


<script>
import HistoColumn from './HistoColumn.vue'

export default {
  name: 'Histogram',
  props: {
    nums: Array
  },
  data() {
    return {
      possible_rolls: [2,3,4,5,6,7,8,9,10,11,12]
    }
  },
  methods: {
    get_theoretical: (Num) => {
      switch (Num) {
        case 2: return 1/36;
        case 3: return 2/36;
        case 4: return 3/36;
        case 5: return 4/36;
        case 6: return 5/36;
        case 7: return 6/36;
        case 8: return 5/36;
        case 9: return 4/36;
        case 10: return 3/36;
        case 11: return 2/36;
        case 12: return 1/36;
        default: return 0;
      }
    },
    get_experimental: (List, Num) => {
      let num_all_rolls = List.length
      let specific_rolls = List.filter(X => X == Num)
      let num_specific_rolls = specific_rolls.length
      return num_specific_rolls / num_all_rolls
    }
  },
  components: {
    HistoColumn
  }
}
</script>


<style lang="less">

td, th  {
  padding: 13px;
  border: 1px solid black;
}


</style>




