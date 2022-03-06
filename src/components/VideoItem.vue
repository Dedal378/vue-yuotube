<script setup>
import VideoItemThumbnail from './VideoItemThumbnail.vue'
import VideoItemInfo from './VideoItemInfo.vue'

defineProps({
  index: {
    type: Number,
    requeue: true,
    default: 1,
  },
})
</script>

<template>
  <a class="mb-7 group">
    <VideoItemThumbnail :index="index" />

    <VideoItemInfo :index="index" />
  </a>
</template>
