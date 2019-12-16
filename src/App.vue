<template>
  <div id="app">
    <h1>{{ title }}</h1>
  </div>
</template>

<script>
  import { csv } from 'd3'

  export default {
    data() {
      return {
        title: 'Pointer!'
      }
    },
    created() {
      return csv('/data/pointer-raw.csv')
        .then(console.log)
    }
  }
</script>

<style>
  #app {
    background: white;
  }
</style>
