<template>
  <div>
    <span v-for="(num, index) in possible_rolls" :key="index">
      <span class="column">{{all_the_ones()}}</span>
    </span>
  </div>
</template>


<script>

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
    all_the_ones: () => {
      return 5
    }
  },
  components: {
  }
}
</script>


<style>

.column {
  padding: 40px;
  background-color: #EAEAFF
}

</style>




