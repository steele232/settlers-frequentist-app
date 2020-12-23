<template>
  <div>
    <div v-for="(num, index) in nums" :key="index">
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
  components: {
    RollItem
  }
}
</script>


<style>
</style>




