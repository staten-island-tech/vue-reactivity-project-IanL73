<template>
  <div>
    <StandBy @click="recruit(chuck)" class="card" v-for="chuck in animals" :key="chuck.name" :animal="chuck"></StandBy>
    <div class="party">
      <h2>
        Current party
      </h2>
      <div class="josh">
        <!--Create seperate array that keeps track of this and v-for that array. God I'm so smart /j-->
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import StandBy from '@/components/StandBy.vue';

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
function recruit(guy) {
  console.log(guy.name)
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