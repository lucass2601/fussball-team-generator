<script setup>
import PlayerItem from './PlayerItem.vue'

const props = defineProps(['playerList'])

</script>

<template>
    <player-item v-for="(player, index) in props.playerList" :key="index" :player_name="player" />
</template>

<style scoped>

</style>
