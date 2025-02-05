<script setup lang="ts">
defineProps({
  isPlaying: Boolean,
});

const emit = defineEmits(["togglePlay"]);

const handleTogglePlay = () => {
  emit("togglePlay");
};
</script>

<template>
  <section class="bg-gradient-to-b from-sky-500 p-10 flex flex-col gap-5 ">
    <div
      class="w-full max-w-2xl flex gap-5 justify-center items-end mx-auto flex-col md:flex-row"
    >
      <img src="/images/The-Beatles.png" alt="" class="w-32 md:w-64" />
      <div class="flex flex-col gap-3">
        <span class="text-neutral-100">Álbum</span>
        <span class="text-neutral-100 font-bold text-5xl">
          Abbev Road (Remastered)
        </span>
        <span class="text-neutral-200">
          The Beatles • 1969 • 17 canciones, 47 min 29 s
        </span>
      </div>
    </div>
    <section class="w-full max-w-2xl mx-auto">
      <button
        @click="handleTogglePlay"
        class="hover:bg-green-500 hover:scale-110 bg-green-400 p-2 rounded-full transition-all duration-75 cursor-pointer"
      >
        <img
          v-if="isPlaying === true"
          src="/icons/player/pause.png"
          width="24"
          height="24"
          alt="Player pause"
        />

        <img
          v-if="isPlaying === false"
          src="/icons/player/play.png"
          width="24"
          height="24"
          alt="Player play"
        />
      </button>
    </section>
  </section>
</template>
