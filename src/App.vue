<template>
  <div id="app">
    <page-header/>
    <hello-world/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import PageHeader from './components/PageHeader.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    PageHeader
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
  margin-top: 42px;
}
</style>
