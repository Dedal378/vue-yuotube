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
const themes = ref(['Use device theme', 'Dark theme', 'Light theme'])
const selectOption = (theme) => {
  emits('select-option', { name: 'theme', value: theme })
}
</script>

<template>
  <DropdownSettingsHeader
    @back="$emit('select-menu', 'main')"
    title="Appearance"
  />

  <section class="py-2">
    <div class="p-3 text-xs text-gray-500">
      Setting applies to this browser only
    </div>
    <ul>
      <DropdownSettingsListItem
        @click.stop="selectOption({ id: themeIdx, text: theme })"
        v-for="(theme, themeIdx) in themes"
        :key="themeIdx"
        :active="themeIdx === selectedOptions.theme.id"
        :label="theme"
      />
    </ul>
  </section>
</template>
