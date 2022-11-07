<script setup>
import { ref } from 'vue';

import PlayerList from '../components/PlayerList.vue'

const emit = defineEmits(['addPlayer'])

const new_player = ref('')
const players = ref([])

const addPlayer = () => {
    if (!players.value.includes(new_player.value)) players.value.push(new_player.value)
    new_player.value = ""
    emit('addPlayer', players)
}

</script>

<template>

    <br>

    <form @submit.prevent="addPlayer">
        <input class="input is-medium" v-model="new_player" type="text" placeholder="Name des Spielers eingeben">
    </form>

    <br>

    <player-list :playerList="players"></player-list>

    <button class="button is-info" style="width: 100%;">Teams generieren</button>

</template>

<style scoped>

</style>
