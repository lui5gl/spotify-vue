<script setup lang="ts">
import { ref } from "vue";
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
    <main class="flex flex-col gap-5">
      <section class="bg-gradient-to-b from-sky-500 pt-10">
        <div
          class="w-full max-w-2xl flex gap-5 justify-center items-end mx-auto"
        >
          <img src="/images/The-Beatles.png" alt="" class="w-full max-w-64" />
          <div class="flex flex-col gap-3">
            <p class="text-neutral-100">Álbum</p>
            <p class="text-neutral-100 font-bold text-5xl">
              Abbev Road (Remastered)
            </p>
            <p class="text-neutral-200">
              The Beatles • 1969 • 17 canciones, 47 min 29 s
            </p>
          </div>
        </div>
      </section>

      <section class="w-full max-w-2xl mx-auto">
        <button
          @click="handleTogglePlay"
          class="hover:bg-green-500 hover:scale-110 bg-green-400 p-2 rounded-full transition-all duration-75 cursor-pointer"
        >
          <img
            v-if="isPlaying === true"
            src="/icons/player/play.png"
            width="24"
            height="24"
            alt="player play"
          />

          <img
            v-if="isPlaying === false"
            src="/icons/player/pause.png"
            width="24"
            height="24"
            alt="player pause"
          />
        </button>
      </section>

      <section class="w-full max-w-2xl mx-auto">
        <table class="text-neutral-400 w-full grid-cols-3">
          <thead>
            <td>#</td>
            <td>Título</td>
            <td>
              <img
                src="/icons/player/clock.png"
                alt="Duration"
                width="16"
                height="16"
              />
            </td>
          </thead>
        </table>
      </section>
    </main>
    <Player :is-playing="isPlaying" @toggle-play="handleTogglePlay" />
  </main>
</template>

