<!-- FigureBlock.vue -->
<template>
  <figure class="space-y-2">
    <video
      v-if="src.endsWith('.mp4')"
      :src="src"
      class="w-full rounded-lg"
      autoplay
      loop
      muted
      playsinline
      controls
    ></video>
    <img v-else :src="src" :alt="title" class="w-full rounded-lg" />
    <figcaption v-if="caption" class="text-center text-gray-500 text-sm italic">
      {{ caption }}
    </figcaption>
  </figure>
</template>

<script setup lang="ts">
defineProps<{ title: string; src: string; caption?: string }>()
</script>
