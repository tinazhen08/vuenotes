<template>
    <div>
        <h2>{{ message }}</h2>
        <h3>{{ count }}</h3>
    </div>
</template>

<script setup>
defineProps({
    message: String,
    count: Number,
})
</script>

<style scoped>

</style>