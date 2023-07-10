<template>
  <div id="app">
   
    <primary-header></primary-header>
    <button @click="openModal">Open Modal</button>
    <modal-component v-bind:toggleModal="toggleModal" v-bind:openModal = "openModal"></modal-component>
  <!-- <h1>{{primaryTitle}}</h1>
 <my-first-component></my-first-component>
 <fruit-list v-bind:name="name" v-bind:age="age" :arrayOfMovies="arrayOfMovies" v-on:delete-movie="handleDeleteMovie" v-on:modifie-title="handleModifieTitle($event)">

<p>Envoyez</p>
<template v-slot:info>
  <h1>Le contenu du slot nommé</h1>
</template>
</fruit-list> -->
  </div>
</template>

<script>

//import components
// import MyFirstComponent from './components/MyFirstComponent.vue';
// import FruitList from './components/FruitList/FruitList.vue';
import PrimaryHeader from './components/Header.vue';
import Modal from './components/Modal.vue';

export default {
  name: 'App',
  components: {
      // 'my-first-component' : MyFirstComponent,
      // 'fruit-list' : FruitList,
      'primary-header' : PrimaryHeader,
      'modal-component' : Modal
  },
  data() {
    return {
      name : {
        firstname : 'Camille',
        lastname : 'Dupond'
      },
      age : 35,
      arrayOfMovies : [
        {title : 'Avatar', date : 2010},
        {title : 'Inception', date : 2009},
        {title : 'Seven', date : 1995}
      ],
      primaryTitle : "Je suis un Titre",
      toggleModal : false
    }
  },
  methods : {
    handleDeleteMovie: function() {
      return this.arrayOfMovies.pop()
    },
handleModifieTitle : function(newTitle) {
  this.primaryTitle = newTitle
},
openModal : function() {
  this.toggleModal = !this.toggleModal
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
