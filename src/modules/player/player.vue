<script setup lang="ts">
import { ref } from "vue";

const remaining = ref<number>(0);
const secondsOfDuration = 140;

const isPlaying = ref<boolean>(false);

const minutesRemaining = Math.floor(secondsOfDuration / 60);
const secondsRemaining = secondsOfDuration % 60;

const durationMinutes = Math.floor(secondsOfDuration / 60);
const durationSeconds = secondsOfDuration % 60;

const handleTogglePlay = () => {
  isPlaying.value = !isPlaying.value;
};
</script>

<template>
  <footer
    class="bg-neutral-950 grid grid-cols-3 justify-between items-center p-3"
  >
    <section>
      <div class="flex gap-2 hover:bg-neutral-800 w-fit p-2 rounded-sm">
        <img src="/images/The-Beatles.png" alt="" class="w-full max-w-15" />
        <div class="flex flex-col justify-center">
          <span class="text-neutral-100 font-semibold">
            Here Comes The Sun - Remastered 2009
          </span>
          <p class="text-neutral-100 text-sm">The Beatles</p>
        </div>
      </div>
    </section>
    <section class="flex justify-center gap-2 flex-col">
      <div class="flex justify-center gap-3 items-center">
        <button
          class="hover:bg-neutral-800 hover:ring-4 ring-neutral-100/25 hover:scale-105 bg-neutral-800 p-1 w-fit h-fit rounded-full transition-all duration-75 cursor-pointer"
        >
          <img
            src="/icons/player/shuffle.png"
            width="18"
            height="18"
            alt="player start"
          />
        </button>
        <button
          class="hover:bg-neutral-800 hover:ring-4 ring-neutral-100/25 hover:scale-105 bg-neutral-800 p-2 rounded-full transition-all duration-75 cursor-pointer"
        >
          <img
            src="/icons/player/player-start.png"
            width="24"
            height="24"
            alt="player start"
          />
        </button>
        <button
          @click="handleTogglePlay()"
          class="hover:bg-neutral-800 hover:ring-4 ring-neutral-100/25 hover:scale-105 bg-neutral-800 p-2 rounded-full transition-all duration-75 cursor-pointer"
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
        <button
          class="hover:bg-neutral-800 hover:ring-4 ring-neutral-100/25 hover:scale-105 bg-neutral-800 p-2 rounded-full transition-all duration-75 cursor-pointer"
        >
          <img
            src="/icons/player/player-end.png"
            width="24"
            height="24"
            alt="player end"
          />
        </button>
        <button
          class="hover:bg-neutral-800 hover:ring-4 ring-neutral-100/25 hover:scale-105 bg-neutral-800 p-1 w-fit h-fit rounded-full transition-all duration-75 cursor-pointer"
        >
          <img
            src="/icons/player/repeat.png"
            width="18"
            height="18"
            alt="player start"
          />
        </button>
      </div>
      <div class="flex gap-2 items-center justify-center">
        <span class="text-neutral-400 text-sm font-semibold whitespace-nowrap">
          {{ minutesRemaining }}:{{ secondsRemaining }}
        </span>
        <input type="range" class="w-full accent-white" :value="remaining" />
        <span class="text-neutral-400 text-sm font-semibold whitespace-nowrap">
          {{ durationMinutes }}:{{ durationSeconds }}
        </span>
      </div>
    </section>
  </footer>
</template>
