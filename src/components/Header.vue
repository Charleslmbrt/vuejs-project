<template>
    <div class="header-top">{{ txt }}</div>
</template>
<script>

import {bus} from '../main'

export default {
    name : 'primary-header',
    data() {
        return {
            txt: 'Mon titre de base'
        }
    },
    beforeCreate() {
        console.log("Le composant va se crée")
    },
    created() {
        console.log("Le composant est crée")
        bus.$on('change-title-header', (data)=>{
            this.txt = data
        })
    }, 
    beforeMount() {
        console.log('Le composant va se monter dans le DOM')
    },
    mounted() {
        console.log('Le composant est intégré dans le DOM')
    },
    beforeUpdate() {
        console.log('Il va se mettre à jour')
    },
    updated() {
        console.log("Le composant s'est mis à jour")
    }
}
</script>
<style>
.header-top {
    position: fixed;
    height:50px;
    width:100%;
    color: white;
    background-color: #333;
    top:0;
    line-height:50px;
}
</style>