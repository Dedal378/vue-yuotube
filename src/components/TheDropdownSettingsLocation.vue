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
const locations = ref(['United States', 'Russia'])
const selectOption = (locationId) => {
  emits('select-option', { name: 'locationId', value: locationId })
}
</script>

<template>
  <DropdownSettingsHeader
    title="Choose your location"
    @back="$emit('select-menu', 'main')"
  />

  <section class="py-2">
    <ul class="max-h-96 overflow-auto">
      <DropdownSettingsListItem
        @click.stop="selectOption(locationIdx)"
        v-for="(location, locationIdx) in locations"
        :key="locationIdx"
        :active="locationIdx === selectedOptions.locationId"
        :label="location"
      />
    </ul>
  </section>
</template>
