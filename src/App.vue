<template>
  <div id="app">
    <Wrapper msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import Wrapper from './components/Wrapper.vue'

export default {
  name: 'app',
  components: {
    Wrapper
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
