<script setup>
import { ref } from 'vue'
import DropdownSettingsListItem from './DropdownSettingsListItem.vue'
import DropdownSettingsHeader from './DropdownSettingsHeader.vue'

defineProps({
  selectedOptions: {
    type: [Object, Number, String],
    required: false,
    default: 0,
  },
})
const emits = defineEmits(['select-menu', 'select-option'])
const languages = ref([
  'English',
  'Russian',
  'Russian',
  'Russian',
  'Russian',
  'Russian',
])
const selectOption = (languageId) => {
  emits('select-option', { name: 'languageId', value: languageId })
}
</script>

<template>
  <DropdownSettingsHeader
    @back="$emit('select-menu', 'main')"
    title="Choose your language"
  />

  <section class="py-2">
    <ul class="max-h-96 overflow-auto">
      <DropdownSettingsListItem
        @click.stop="selectOption(languageIdx)"
        v-for="(language, languageIdx) in languages"
        :key="languageIdx"
        :active="languageIdx === selectedOptions.languageId"
        :label="language"
      />
    </ul>
  </section>
</template>
