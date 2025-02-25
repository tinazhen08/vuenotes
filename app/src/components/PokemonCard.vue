<template>
    <div>
        <router-link :to="pkmnPath" class="card">
            <h2>{{ pokemon.name }}</h2>
            <h3>{{ id }}</h3>
            <slot></slot>
        </router-link>
    </div>
</template>

<script setup>
import { computed } from 'vue';
const props = defineProps({
    pokemon: Object,
    id: Number
})

const pkmnPath = computed(()=>{
    return `/pokemon/${props.id}` 
})
</script>

<style scoped>

</style>