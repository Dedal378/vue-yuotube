<script setup>
import { onMounted, ref } from 'vue'

const searchInput = ref(null)
const classes = [
  'px-3',
  'w-full',
  'border',
  'border-gray-300',
  'shadow-inner',
  'rounded-bl-sm',
  'rounded-tl-sm',
  'focus:border-blue-700',
  'focus:outline-none',
]

onMounted(() => {
  if (window.innerWidth < 640) {
    searchInput.value.focus()
  }
})
</script>

<template>
  <input ref="searchInput" :class="classes" placeholder="Search" type="text" />
</template>
