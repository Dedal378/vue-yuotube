<script setup>
import BaseIcon from './BaseIcon.vue'

defineProps({
  index: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <div class="relative">
    <img alt="image" :src="`https://picsum.photos/seed/image${index}/720/404`" />

    <span
      class="absolute opacity-0 group-hover:opacity-100 bg-opacity-60 top-0 right-0 bg-black text-white rounded-sm m-1 p-1"
    >
      <BaseIcon name="clock" class="h-5 w-5" />
    </span>
    <span
      class="absolute opacity-0 group-hover:opacity-100 bg-opacity-60 top-8 right-0 bg-black text-white rounded-sm m-1 p-1"
    >
      <BaseIcon name="menuVideo" class="h-5 w-5" />
    </span>
    <span
      class="absolute opacity-100 group-hover:opacity-0 duration-500 bottom-0 right-0 bg-black text-white rounded-sm m-1 p-1 text-xs font-semibold"
    >
      6:35
    </span>
  </div>
</template>
