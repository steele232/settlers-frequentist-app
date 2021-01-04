
<template>
  <h2 :class="[experimental >= theoretical ? 'green' : 'red']"> 
    {{ experimental.toFixed(2) }}
  </h2>
</template>

<script>
export default {
  name: 'HistoColumn',
  props: {
    theoretical: Number,
    experimental: Number
  },
  data: () => {
    return {};
  },
  methods: {
    get_percent_string: (Probability) => {
      let percent = Probability * 100
      return percent.toString + '%'
    }
  },
  components: {
  }
}
</script>


<style lang="less">

* {
  box-sizing: border-box;
}

.green {
  background-color: #45e845;
}

.red {
  background-color: #ff9393;
}

</style>




