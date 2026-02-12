<template>
    <div @click ="post">
        <h2>{{ animal.name }}</h2>
        <h3>{{ animal.species }}</h3>
    </div>
</template>

<script setup>
import { ref } from 'vue';

defineProps({
    animal:{
        type:Object,
        required: true,
    }
})
function post(){
    console.log(animal.name)
}
</script>

<style scoped>
div{
    display:flex;
    flex-direction: column;
    justify-content:space-around;
    align-items:center;
    height: 200px;
    width: 150px;
    border: 3px solid black;
    margin: 5px;
    border-radius: 12px;
}
</style>