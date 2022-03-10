<script setup>
import { ref } from 'vue'
import BaseIcon from './BaseIcon.vue'
import DropdownSettingsListItem from './DropdownSettingsListItem.vue'

const selectedThemeIdx = ref(0)
const themes = ref([
  'Appearance',
  'Use device theme',
  'Dark theme',
  'Light theme',
])
</script>

<template>
  <section class="flex items-center border-b border-gray-200 text-black">
    <button class="p-3 focus:outline-none">
      <BaseIcon
        @click="$emit('select-menu', 'main')"
        name="arrowLeft"
        class="h-5 w-5"
      />
    </button>
    <span>{{ themes[0] }}</span>
  </section>

  <section class="py-2">
    <div class="p-3 text-xs text-gray-500">
      Setting applies to this browser only
    </div>
    <ul>
      <DropdownSettingsListItem
        @click="selectedThemeIdx = themeIdx"
        v-for="(theme, themeIdx) in themes.slice(1, 4)"
        :key="themeIdx"
        :active="themeIdx === selectedThemeIdx"
        :label="theme"
      />
    </ul>
  </section>
</template>
