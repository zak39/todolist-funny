<template>
  <div id="app">
    <h1 class="title">📋 Todo List</h1>
    <Home />
  </div>
</template>

<script>
import Home from './Home.vue'

export default {
  name: 'App',
  components: {
    Home
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

.title {
  margin-bottom: 100px;
}
</style>
