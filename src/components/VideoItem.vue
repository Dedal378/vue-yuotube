<script setup>
import VideoItemThumbnail from './VideoItemThumbnail.vue';
import VideoItemInfo from './VideoItemInfo.vue';
import { defineProps } from 'vue';

defineProps({
  index: {
    type: Number,
    requeue: true,
    default: 1,
  },
})
</script>

<template>
  <a class="mb-7 group" href="#">
    <VideoItemThumbnail :index="index" />

    <VideoItemInfo :index="index" />
  </a>
</template>
