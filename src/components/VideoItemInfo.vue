<script setup>
import { defineProps } from 'vue'
import BaseIcon from './BaseIcon.vue'

defineProps({
  index: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <div class="flex items-start mt-3">
    <img alt="image" class="mr-3 rounded-full w-9 h-9" :src="`https://picsum.photos/seed/avatar${index}/68`" />

    <div class="text-xs whitespace-nowrap">
      <span class="font-semibold text-gray-800">Video title 1</span>

      <div class="flex items-center mt-1">
        <span class="mb-1">Channel name 1</span>
        <BaseIcon name="check" class="h-3.5 w-3.5 ml-1" />
      </div>

      <div>
        <span>1k views</span>
        &middot;
        <span>1 day ago</span>
      </div>
    </div>

    <button
      class="ml-auto p-0.5 -mt-1 opacity-0 group-hover:opacity-100 text-gray-500 hover:text-gray-700 focus:outline-none"
    >
      <BaseIcon name="dotsVertical" class="h-5 w-5" />
    </button>
  </div>
</template>
