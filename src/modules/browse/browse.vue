<script setup lang="ts">
import Cover from "./cover/cover.vue";
import Track from "./track/track.vue";

defineProps({
  isPlaying: Boolean,
});

const emit = defineEmits(["togglePlay"]);

const handleTogglePlay = () => {
  emit("togglePlay");
};

const playlist = [
  {
    id: 1,
    title: "Come Together - Remastered 2009",
    duration: "4:19",
    artists: ["The Beatles"],
  },
  {
    id: 2,
    title: "Something - Remastered 2009",
    duration: "3:02",
    artists: ["The Beatles"],
  },
  {
    id: 3,
    title: "Maxwell's Silver Hammer - Remastered 2009",
    duration: "3:27",
    artists: ["The Beatles"],
  },
  {
    id: 4,
    title: "Oh! Darling - Remastered 2009",
    duration: "3:27",
    artists: ["The Beatles"],
  },
  {
    id: 5,
    title: "Octopus's Garden - Remastered 2009",
    duration: "2:50",
    artists: ["The Beatles"],
  },
  {
    id: 6,
    title: "I Want You (She's So Heavy) - Remastered 2009",
    duration: "7:47",
    artists: ["The Beatles"],
  },
  {
    id: 7,
    title: "Here Comes The Sun - Remastered 2009",
    duration: "3:05",
    artists: ["The Beatles"],
  },
  {
    id: 8,
    title: "Because - Remastered 2009",
    duration: "2:45",
    artists: ["The Beatles"],
  },
  {
    id: 9,
    title: "You Never Give Me Your Money - Remastered 2009",
    duration: "4:02",
    artists: ["The Beatles"],
  },
  {
    id: 10,
    title: "Sun King - Remastered 2009",
    duration: "2:26",
    artists: ["The Beatles"],
  },
  {
    id: 11,
    title: "Mean Mr Mustard - Remastered 2009",
    duration: "1:06",
    artists: ["The Beatles"],
  },
  {
    id: 12,
    title: "Polythene Pam - Remastered 2009",
    duration: "1:12",
    artists: ["The Beatles"],
  },
  {
    id: 13,
    title: "She Came In Through The Bathroom Window - Remastered 2009",
    duration: "1:58",
    artists: ["The Beatles"],
  },
  {
    id: 14,
    title: "Golden Slumbers - Remastered 2009",
    duration: "1:31",
    artists: ["The Beatles"],
  },
  {
    id: 15,
    title: "Carry That Weight - Remastered 2009",
    duration: "1:36",
    artists: ["The Beatles"],
  },
  {
    id: 16,
    title: "The End - Remastered 2009",
    duration: "2:21",
    artists: ["The Beatles"],
  },
  {
    id: 17,
    title: "Her Majesty - Remastered 2009",
    duration: "0:25",
    artists: ["The Beatles"],
  },
];
</script>

<template>
  <main class="flex flex-col gap-5 my-20">
    <Cover :is-playing="isPlaying" @toggle-play="handleTogglePlay" />

    <section class="w-full max-w-2xl mx-auto mb-10">
      <table class="text-neutral-400 w-full grid-cols-3">
        <thead class="[&>td]:p-2 border-b-1 border-b-neutral-700">
          <td class="text-right px-2">#</td>
          <td class="px-2">Título</td>
          <td class="px-2">
            <img
              src="/icons/player/clock.png"
              alt="Duration"
              width="16"
              height="16"
            />
          </td>
        </thead>

        <tbody>
          <Track
            v-for="track in playlist"
            :key="track.id"
            :id="track.id"
            :title="track.title"
            :duration="track.duration"
            :artists="track.artists"
          />
        </tbody>
      </table>
    </section>
  </main>
</template>
