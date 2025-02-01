<script setup lang="ts">
import Player from "./modules/player/player.vue";
import Navigation from "./modules/navigation/navigation.vue";
</script>

<template>
  <main class="flex justify-between flex-col min-h-screen bg-neutral-900">
    <Navigation />
    <Player />
  </main>
</template>

