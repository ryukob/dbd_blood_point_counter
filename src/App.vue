<template>
  <div id="app">
    <page-header/>
    <level-slider/>
    <bp-task-cards/>
  </div>
</template>

<script>
import BpTaskCards from './components/BpTaskCards.vue'
import HelloWorld from './components/HelloWorld'
import LevelSlider from './components/LevelSlider.vue'
import PageHeader from './components/PageHeader.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    PageHeader,
    BpTaskCards,
    LevelSlider,
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
