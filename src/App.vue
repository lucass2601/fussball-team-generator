<script setup>
import { ref } from 'vue';

import Configuration from './components/Configuration.vue'

const playerList = ref([])

const updatePlayers = players => {
  playerList.value = players
}

</script>

<template>
  <header>
    <section class="hero is-success">
      <div class="hero-body">
        <p class="title">
          Fußball Team Generator ⚽️
        </p>
        <p class="subtitle">
          Durch die Anzahl der Spieler werden alle möglichen Teamvariationen ausgerechnet und visualisiert.
        </p>
      </div>
    </section>
  </header>
  <main>
    <div class="container">
      <configuration @addPlayer="updatePlayers"></configuration>
    </div>
  </main>
  <footer>

  </footer>
</template>

<style scoped>

</style>
