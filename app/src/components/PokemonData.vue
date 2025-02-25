<template>
    <div>
        <h2>{{ pokemon.name }}</h2>
        <div class="abbilities">
            <h5 v-for="stat in stats" :key="stat">{{ stat.base_stat }}</h5>
        </div>
    </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';
import { useRoute } from 'vue-router';

const route = useRoute();
const pokemon = ref("");
async function getPokemon(){
  let res = await fetch(`https://pokeapi.co/api/v2/pokemon/${route.params.id}/`);
  let data = await res.json()
  pokemon.value = data
}

onMounted(()=> {
  getPokemon();
});
</script>

<style scoped>

</style>