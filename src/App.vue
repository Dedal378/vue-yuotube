<script setup>
import { ref, onMounted } from 'vue'
import TheHeader from './components/TheHeader.vue'
import TheSidebar from './components/TheSidebar.vue'
import TheCategories from './components/TheCategories.vue'
import TheSidebarCompact from './components/TheSidebarSmall.vue'
import TheSidebarMobile from './components/TheSidebarMobile.vue'
import TheVideos from './components/TheVideos.vue'

const isCompactSidebarActive = ref(false)
const isCompactSidebarOpen = ref(false)
const isMobileSidebarOpen = ref(false)
const isSidebarOpen = ref(false)

const toggleSidebar = () => {
  if (window.innerWidth >= 1280) {
    isCompactSidebarActive.value = !isCompactSidebarActive.value

    onResize()
  } else {
    openMobileSidebar()
  }
}
const openMobileSidebar = () => (isMobileSidebarOpen.value = true)
const closeMobileSidebar = () => (isMobileSidebarOpen.value = false)
const onResize = () => {
  if (window.innerWidth < 768) {
    isCompactSidebarOpen.value = false
    isSidebarOpen.value = false
  } else if (window.innerWidth < 1280) {
    isCompactSidebarOpen.value = true
    isSidebarOpen.value = false
  } else {
    isCompactSidebarOpen.value = isCompactSidebarActive.value
    isSidebarOpen.value = !isCompactSidebarActive.value
  }
}

onMounted(() => {
  if (window.innerWidth >= 768 && window.innerWidth < 1280) {
    isCompactSidebarActive.value = true
  }

  if (window.innerWidth >= 1280) {
    isCompactSidebarActive.value = false
  }

  onResize()

  window.addEventListener('resize', onResize)
})
</script>

<template>
  <TheHeader @toggle-sidebar="toggleSidebar" />
  <TheSidebarCompact v-if="isCompactSidebarOpen" />
  <TheSidebar v-if="isSidebarOpen" />
  <TheSidebarMobile :is-open="isMobileSidebarOpen" @close="closeMobileSidebar" />
  <TheCategories :is-sidebar-open="isSidebarOpen" />
  <TheVideos :is-sidebar-open="isSidebarOpen" />
</template>
