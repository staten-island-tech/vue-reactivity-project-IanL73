<template>
    <div>
        <h2>{{ animal.name }}</h2>
        <h3>{{ animal.species }}</h3>
        <slot></slot>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const props = defineProps({
    animal:{
        type:Object,
        required: true,
    }
})
</script>

<style scoped>
div{
    display:flex;
    justify-content:space-around;
    align-items:center;
    height: 200px;
    width: 150px;
    border: 3px solid red;
    margin: 5px;
    border-radius: 12px;
}
</style>