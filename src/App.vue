<template>
  <div id="app">
    <results></results>
  </div>
</template>

<script>
import Results from './components/Results'

export default {
  name: 'app',
  components: {
    Results
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
