<template>
    <div>
        <ul class="list">
            <li v-for="(fruit, index) in arrayOfFruits" v-bind:key="index">{{ fruit }}</li>
        </ul>
        <p>{{ name.firstname }} {{ name.lastname }}</p>
        <p>{{ reversing() }}</p>
   
    </div>
</template>
<script>
export default {
    name : 'FruitList',
    data() {
        return {
            arrayOfFruits : ['pomme', 'poire', 'fraise', 'banane']
        }
    },
    props : ['name'],
    methods : {
        reversing : function() {
            return this.name.firstname.split('').reverse().join('')
        }
    }
}

</script>
<style scoped src="./FruitList.css">
</style>