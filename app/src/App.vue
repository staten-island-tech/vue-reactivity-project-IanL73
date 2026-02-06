<template>
  <div>
    <h2>Hello World! :D</h2>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const animals = ref([
  { name: 'Leo', species: 'Lion', weight: 420 },
  { name: 'Ella', species: 'Elephant', weight: 5000 },
  { name: 'Max', species: 'Dog', weight: 30 },
  { name: 'Whiskers', species: 'Cat', weight: 4 },
  { name: 'Bubbles', species: 'Fish', weight: 0.5 },
  { name: 'Charlie', species: 'Horse', weight: 500 },
  { name: 'Hoppy', species: 'Rabbit', weight: 3 },
  { name: 'Tweety', species: 'Bird', weight: 0.2 },
  { name: 'Gerry', species: 'Giraffe', weight: 1200 },
  { name: 'Bella', species: 'Bear', weight: 300 },
])
</script>

<style scoped>

</style>