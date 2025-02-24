<template>
    <div>
        <div class="pokemon-card">
            <h2>{{ name }}</h2>
            <h3>{{ index }}</h3>
        </div>
    </div>
</template>

<script setup>
defineProps({
    name: String,
    index: Number
})
</script>

<style lang="scss" scoped>

</style>