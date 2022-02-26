<script setup>
import VideoItemThumbnail from './VideoItemThumbnail.vue'
import VideoItemInfo from './VideoItemInfo.vue'

// eslint-disable-next-line no-undef
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
