<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
import Home from '@/view/home'
export default {
  name: 'App',
  components: {
    Home
  }
}
</script>

<style>
@import './reset.css';

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
html,body {
  padding: 0;
  margin: 0;
}
</style>
