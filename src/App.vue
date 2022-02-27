<script setup>
import { ref, onMounted } from 'vue'
import TheHeader from './components/TheHeader.vue'
import TheSidebar from './components/TheSidebar.vue'
import TheCategories from './components/TheCategories.vue'
import TheSidebarSmall from './components/TheSidebarSmall.vue'
import TheSidebarMobile from './components/TheSidebarMobile.vue'
import TheVideos from './components/TheVideos.vue'

const sidebarState = ref(null)
const isMobileSidebarOpen = ref(false)

onMounted(() => {
  if (window.innerWidth >= 768 && window.innerWidth < 1280) {
    sidebarState.value = 'compact'
  }

  if (window.innerWidth >= 1280) {
    sidebarState.value = 'normal'
  }
})

const toggleSidebar = () => {
  if (window.innerWidth >= 1280) {
    sidebarState.value = sidebarState.value === 'normal' ? 'compact' : 'normal'
  } else {
    openMobileSidebar()
  }
}
const openMobileSidebar = () => (isMobileSidebarOpen.value = true)
const closeMobileSidebar = () => (isMobileSidebarOpen.value = false)
</script>

<template>
  <TheHeader @toggle-sidebar="toggleSidebar" />
  <TheSidebarSmall :is-open="sidebarState === 'compact'" />
  <TheSidebar :is-open="sidebarState === 'normal'" />
  <TheSidebarMobile :is-open="isMobileSidebarOpen" @close="closeMobileSidebar" />
  <TheCategories :is-sidebar-open="sidebarState === 'normal'" />
  <TheVideos :is-sidebar-open="sidebarState === 'normal'" />
</template>
