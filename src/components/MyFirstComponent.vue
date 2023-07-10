<template>
    <div>
        <button @click="toggleOne">Onglet 1</button>
        <button @click="toggleTwo">Onglet 2</button>
        <texte-1 v-if="toggle1"></texte-1>
        <texte-2 v-if="toggle2"></texte-2>
    </div>
</template>
<script>

//import components
import Texte1 from './Texte1.vue';
import Texte2 from './Texte2.vue';

export default {
    name : "MyFirstComponent",
    data() {
        return {
            txt : "Hello World",
            toggle1 : true,
            toggle2 : false,
        }
    },
    components : {
        'texte-1' : Texte1,
        'texte-2' : Texte2
    },
    methods : {
toggleOne : function() {
    this.toggle1 = true,
    this.toggle2 = false
},
toggleTwo : function() {
    this.toggle1 = false,
    this.toggle2 = true
},

    }
}
</script>
<style></style>