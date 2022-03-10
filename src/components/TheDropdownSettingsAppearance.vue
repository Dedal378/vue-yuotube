<script setup>
import { ref } from 'vue'
import DropdownSettingsListItem from './DropdownSettingsListItem.vue'
import DropdownSettingsHeader from './DropdownSettingsHeader.vue'

defineEmits({ 'select-menu': null })
const selectedThemeIdx = ref(0)
const themes = ref(['Use device theme', 'Dark theme', 'Light theme'])
</script>

<template>
  <DropdownSettingsHeader
    title="Appearance"
    @back="$emit('select-menu', 'main')"
  />

  <section class="py-2">
    <div class="p-3 text-xs text-gray-500">
      Setting applies to this browser only
    </div>
    <ul>
      <DropdownSettingsListItem
        @click.stop="selectedThemeIdx = themeIdx"
        v-for="(theme, themeIdx) in themes"
        :key="themeIdx"
        :active="themeIdx === selectedThemeIdx"
        :label="theme"
      />
    </ul>
  </section>
</template>
