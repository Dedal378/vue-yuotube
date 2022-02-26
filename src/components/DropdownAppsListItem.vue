<script setup>
import BaseIcon from './BaseIcon.vue'

const props = defineProps({
  label: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <li>
    <a class="flex items-center px-3 py-2 text-sm hover:bg-gray-100" href="#">
      <BaseIcon name="play" class="h-6 w-6 mr-3 text-red-500" />
      <span>{{ props.label }}</span>
    </a>
  </li>
</template>
