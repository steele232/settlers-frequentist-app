<template>
  <div class="cool-name">
    <h3>{{ name }}</h3>
  </div>
</template>

<script>
export default {
  name: 'Hello',
  props: {
    name: String
  }
}
</script>

<style>

.cool-name {
  background-color: black;
  color: white;
}

</style>


