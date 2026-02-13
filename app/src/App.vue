<template>
  <div>
    <StandBy @click = "post" class="card" v-for="chuck in animals" :key="chuck.name" :animal="chuck"/>
    <div class="party">
      <h2>
        Current party
      </h2>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import StandBy from '@/components/StandBy.vue';

const animals = ([
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
function post(){
  console.log("cheese")
}
</script>

<style scoped>
.party{
  border: 3px solid black;
  border-radius: 8px;
  display: flex;
  align-self: flex-end;
}
</style>