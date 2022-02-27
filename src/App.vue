<script setup>
import { ref } from 'vue'
import TheHeader from './components/TheHeader.vue'
import TheSidebar from './components/TheSidebar.vue'
import TheCategories from './components/TheCategories.vue'
import TheSidebarSmall from './components/TheSidebarSmall.vue'
import TheSidebarMobile from './components/TheSidebarMobile.vue'
import TheVideos from './components/TheVideos.vue'

const isMobileSidebarOpen = ref(false)
const openMobileSidebar = () => (isMobileSidebarOpen.value = true)
const closeMobileSidebar = () => (isMobileSidebarOpen.value = false)
</script>

<template>
  <TheHeader @open-mobile-sidebar="openMobileSidebar" />
  <TheCategories />
  <TheSidebar />
  <TheSidebarSmall />
  <TheSidebarMobile :is-open="isMobileSidebarOpen" @close="closeMobileSidebar" />
  <TheVideos />
</template>
