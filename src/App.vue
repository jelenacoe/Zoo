<template>
  <div id="app">
    <HelloWorld msg="Zivotinje"/>
    <animal-list msg="Lista Zivotinja"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import { AnimalList }from './components/AnimalList.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    AnimalList
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
