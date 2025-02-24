<template>
  <div>
    <PokemonCard v-for="(mon, index) in pokemon" :key="mon.name" :name="mon.name" :index="index"/>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';
import PokemonCard from '@/components/PokemonCard.vue';

const pokemon = ref("");
async function getPokemon(){
  let res = await fetch("https://pokeapi.co/api/v2/pokemon?limit=151");
  let data = await res.json()
  pokemon.value = data.results
}

onMounted(()=> {
  getPokemon();
});
</script>

<style scoped>

</style>