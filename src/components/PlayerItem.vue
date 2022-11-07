<script setup>
defineProps(['player_name'])

</script>

<template>
    <span class="tag is-info is-large">
        {{ player_name }}
        <button class="delete"></button>
    </span>
</template>

<style scoped>

</style>
