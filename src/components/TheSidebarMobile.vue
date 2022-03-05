<script setup>
import { ref, toRefs, watch, nextTick } from 'vue'
import BaseIcon from './BaseIcon.vue'
import LogoMain from './LogoMain.vue'
import SidebarContent from './SidebarContent.vue'
import TheSidebarMobileOverlay from './TheSidebarMobileOverlay.vue'

const props = defineProps({
  isOpen: {
    type: Boolean,
    required: true,
  },
})

const mobileSidebar = ref()
const { isOpen } = toRefs(props)

defineEmits({
  close: null,
})

watch(isOpen, () => {
  nextTick(() => isOpen && mobileSidebar.value.focus()) //выражение выполнится, если isOpen не null и не undefined
})
</script>

<template>
  <transition
    enter-active-class="transition-opacity ease-linear duration-200"
    enter-from-class="opacity-0"
    enter-to-class="opacity-100"
    leave-active-class="transition-opacity ease-linear duration-200"
    leave-from-class="opacity-100"
    leave-to-class="opacity-0"
  >
    <TheSidebarMobileOverlay @click="$emit('close')" v-show="isOpen" />
  </transition>

  <transition
    enter-active-class="transition transform ease-in-out duration-200"
    enter-from-class="-translate-x-full"
    enter-to-class="translate-x-0"
    leave-active-class="transition transform ease-in-out duration-200"
    leave-from-class="translate-x-0"
    leave-to-class="-translate-x-full"
  >
    <aside
      v-show="isOpen"
      @keydown.esc="$emit('close')"
      tabindex="-1"
      ref="mobileSidebar"
      class="fixed z-40 w-64 max-h-screen overflow-auto bg-white outline-none"
    >
      <section class="flex items-center p-4 border-b sticky top-0 bg-white">
        <button @click="$emit('close')" class="ml-2 mr-6 focus:outline-none">
          <BaseIcon name="menu" />
        </button>
        <LogoMain />
      </section>
      <SidebarContent />
    </aside>
  </transition>
</template>
