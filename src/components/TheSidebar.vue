<script setup>
import { computed } from 'vue'
import SidebarContent from './SidebarContent.vue'

const props = defineProps({
  isOpen: {
    type: Boolean,
  },
})
const classes = computed(() => [
  props.isOpen ? 'xl:block' : 'hidden',
  'w-64',
  'max-h-screen',
  'overflow-auto',
  'fixed',
  'z-20',
  'top-0',
  'pt-12',
  'bg-white',
])
</script>

<template>
  <aside :class="classes">
    <SidebarContent />
  </aside>
</template>
