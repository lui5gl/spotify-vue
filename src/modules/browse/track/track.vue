<script setup lang="ts">
defineProps({
  id: Number,
  title: String,
  duration: String,
  artists: Array,
});
</script>

<template>
  <tr
    class="text-neutral-100 [&>td]:py-4 hover:cursor-pointer hover:bg-neutral-800 rounded-sm"
  >
    <td class="text-right px-2">{{ id }}</td>
    <td class="px-2">
      {{ title }}
    </td>
    <td class="px-2">{{ duration }}</td>
  </tr>
</template>
