<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
  
 <my-first-component></my-first-component>
  </div>
</template>

<script>

import MyFirstComponent from './components/MyFirstComponent.vue';

export default {
  name: 'App',
  components: {
      'my-first-component' : MyFirstComponent
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
