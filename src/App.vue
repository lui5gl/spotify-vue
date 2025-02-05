<script setup lang="ts">
import { ref } from "vue";
import Browse from "./modules/browse/browse.vue";
import Navigation from "./modules/navigation/navigation.vue";
import Player from "./modules/player/player.vue";

const isPlaying = ref<boolean>(false);

const handleTogglePlay = () => {
  isPlaying.value = !isPlaying.value;
};
</script>

<template>
  <main class="flex flex-col min-h-screen bg-neutral-900">
    <Navigation />
    <Browse :is-playing="isPlaying" @toggle-play="handleTogglePlay" />
    <Player :is-playing="isPlaying" @toggle-play="handleTogglePlay" />
  </main>
</template>
