<template>
  <div id="app">
    <Routes msg="Welcome to Kamailio routes"/>
  </div>
</template>

<script>
import Routes from './components/Routes.vue'

export default {
  name: 'app',
  components: {
    Routes
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
