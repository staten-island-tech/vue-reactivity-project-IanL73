<template>
  <div>
    <StandBy @click="recruit(chuck)" class="card" v-for="chuck in animals" :key="chuck.name" :animal="chuck"></StandBy>
    <div class="party">
      <h2>
        Current party
      </h2>
      <div class="josh">
        <PartyMember @click="dismiss(charles)" class="card" v-for="charles in animalsinparty" :key="charles.name" :animal="charles"></PartyMember>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import StandBy from '@/components/StandBy.vue';
import PartyMember from './components/PartyMember.vue';
import { animals } from './stores/PartyStore';
import { animalsinparty } from './stores/PartyStore';

function recruit(guy) {
  animalsinparty.value.push(guy)
}
function dismiss(guy) {
  console.log(guy.species)
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