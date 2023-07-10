<template>
    <div>
        <ul class="list">
            <li v-for="(fruit, index) in arrayOfFruits" v-bind:key="index">{{ fruit }}</li>
        </ul>
        <p>{{ name.firstname }} {{ name.lastname }}</p>
        <p>{{ age }}</p>
        <p>{{ reversing() }}</p>
     
        <ul class="list">
            <li v-for="(movie, index) in arrayOfMovies" :key="index">
            Title : {{ movie.title }} / Date : {{ movie.date }}
            </li>
        </ul>
        <button v-on:click="deleteMovie">Delete Movie</button>
        <button v-on:click="modifieTitle">Modifie Title</button>
        <button v-on:click="changeTitleHeader">Change Title Header</button>
   <slot>Patientez</slot>
   <slot name="info"></slot>
    </div>
</template>
<script>

import {bus} from '../../main'

export default {
    name : 'FruitList',
    data() {
        return {
            arrayOfFruits : ['pomme', 'poire', 'fraise', 'banane']
        }
    },
    props : {
        age : {
            type : Number,
            required : true
        },
        name : {
            type : Object
        },
        arrayOfMovies : {
            type: Array
        }
    },
    methods : {
        reversing : function() {
            return this.name.firstname.split('').reverse().join('')
        },
        deleteMovie : function() {
            return this.$emit('delete-movie')
        },
        modifieTitle : function(){
            return this.$emit('modifie-title', 'Je suis un nouveau titre')
        },
        changeTitleHeader : function() {
            bus.$emit('change-title-header', "J'ai changé mon titre du header")
        }
    }
}

</script>
<style scoped src="./FruitList.css">
</style>