<script setup>
import BaseIcon from './BaseIcon.vue'

defineProps({
  label: {
    type: String,
    required: true,
  },
  icon: {
    type: String,
  },
  withSubMenu: {
    type: Boolean,
  },
})
</script>

<template>
  <li>
    <a class="flex items-center px-4 py-2 text-sm hover:bg-gray-100" href="#">
      <BaseIcon v-if="icon" :name="icon" class="h-6 w-6 mr-3 text-gray-400" />
      <span>{{ label }}</span>
      <BaseIcon v-if="withSubMenu" name="arrow" class="h-5 w-5 text-gray-400 ml-auto" />
    </a>
  </li>
</template>
