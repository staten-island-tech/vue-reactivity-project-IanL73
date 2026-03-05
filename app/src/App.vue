<template>
  <div>
    <StandBy @click="recruit(chuck)" class="card" v-for="chuck in animals" :key="chuck.name" :animal="chuck"></StandBy>
    <div class="party">
      <h2>
        Current party
      </h2>
      <button @click="clear()">clear party</button>
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
  if(animalsinparty.value.length !== 6) {
    let alreadyin = animalsinparty.value.some((element) => element === guy)
    if (alreadyin === false){
    animalsinparty.value.push(guy)
  }}
}
function dismiss(guy) {
  let guyIndex = animalsinparty.value.findIndex((element) => element === guy)
  animalsinparty.value.splice(guyIndex, 1)
}
function clear() {
  animalsinparty.value = []
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