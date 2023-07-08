<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
  
 <my-first-component></my-first-component>
 <fruit-list v-bind:name="name"></fruit-list>
  </div>
</template>

<script>

//import components
import MyFirstComponent from './components/MyFirstComponent.vue';
import FruitList from './components/FruitList/FruitList.vue';

export default {
  name: 'App',
  components: {
      'my-first-component' : MyFirstComponent,
      'fruit-list' : FruitList
  },
  data() {
    return {
      name : {
        firstname : 'Camille',
        lastname : 'Dupond'
      }
    }
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
