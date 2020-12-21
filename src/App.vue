<template>
  <div id="app">
    <page-header/>    
    <div class="contents">
      <level-slider class="level-slider"/>
      <bp-task-cards class="bp-task-cards"/>
    </div>
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
  background-color: #2c3e50;
}

.contents {
  display: flex;
  justify-content: center;
  align-items: center;
  align-content: center;
  /* padding: 126px; */
  height: 100vh;
}

.level-slider { 
  flex-basis: 30%; 
}

.bp-task-cards { 
  flex-basis: 20%; 

}
</style>
