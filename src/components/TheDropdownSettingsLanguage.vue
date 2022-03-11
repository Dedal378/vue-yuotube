<script setup>
import { ref } from 'vue'
import DropdownSettingsListItem from './DropdownSettingsListItem.vue'
import DropdownSettingsHeader from './DropdownSettingsHeader.vue'

defineEmits({ 'select-menu': null })
const selectedLanguageIdx = ref(0)
const languages = ref([
  'English',
  'Russian',
  'Russian',
  'Russian',
  'Russian',
  'Russian',
])
</script>

<template>
  <DropdownSettingsHeader
    title="Choose your language"
    @back="$emit('select-menu', 'main')"
  />

  <section class="py-2">
    <ul class="max-h-96 overflow-auto">
      <DropdownSettingsListItem
        @click.stop="selectedLanguageIdx = languageIdx"
        v-for="(language, languageIdx) in languages"
        :key="languageIdx"
        :active="languageIdx === selectedLanguageIdx"
        :label="language"
      />
    </ul>
  </section>
</template>
