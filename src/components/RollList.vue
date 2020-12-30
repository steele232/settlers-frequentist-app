<template>
  <div>
    <div v-for="(num, index) in deep_copy_and_reverse(nums)" :key="index">
      <RollItem :num="num"/>
    </div>
  </div>
</template>


<script>
import RollItem from './RollItem.vue'

export default {
  name: 'RollList',
  props: {
    nums: Array
  },
  methods: {
    deep_copy_and_reverse: (Nums) => {
      let deep_copy = [...Nums]
      return deep_copy.reverse()
    }
  },
  components: {
    RollItem
  }
}
</script>


<style>
</style>




