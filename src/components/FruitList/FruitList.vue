<template>
    <ul class="list">
<li v-for="(fruit, index) in arrayOfFruits" v-bind:key="index">{{ fruit }}</li>
    </ul>
</template>
<script>
export default {
    name : 'FruitList',
    data() {
        return {
            arrayOfFruits : ['pomme', 'poire', 'fraise', 'banane']
        }
    }
}

</script>
<style scoped src="./FruitList.css">
</style>