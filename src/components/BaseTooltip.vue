<script setup>
import { computed, ref } from 'vue'

defineProps({
  text: {
    type: String,
    required: true,
  },
})
const isShown = ref(false)

const classes = computed(() => {
  return [
    'bg-gray-600',
    'bg-opacity-80',
    'rounded-sm',
    'text-white',
    'text-xs',
    'whitespace-nowrap',
    'p-2',
    'absolute',
    'top-14',
    'left-1/2',
    'transform',
    '-translate-x-1/2',
  ]
})
const toggle = () => {
  isShown.value = !isShown.value
}
</script>

<template>
  <div class="relative">
    <div @mouseenter="toggle" @mouseleave="toggle" class="h-full">
      <slot />
    </div>
    <transition
      enter-active-class="duration-300"
      enter-from-class="opacity-0"
      enter-to-class="opacity-100"
      leave-active-class="duration-75"
      leave-from-class="opacity-100"
      leave-to-class="opacity-0"
    >
      <div v-show="isShown" :class="classes">{{ text }}</div>
    </transition>
  </div>
</template>
