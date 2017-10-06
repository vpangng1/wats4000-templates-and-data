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
}
.results {
  width: 75%;
  margin: 0 auto;
  text-align: left;
  background: #fff;
  padding: 2rem;
}
a {
  cursor: pointer;
}
html, body {
  margin: 0;
  padding: 0;
  background: #e8e8e8;
}
</style>
