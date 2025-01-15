<template>
    <div>
        <h2 v-for="animal in animals" :key="animal">{{ animal }}</h2>
    </div>
</template>

<script setup>
const animals = ['Zebra', 'Ape', 'Panda', 'Dustin']
</script>

<style scoped></style>