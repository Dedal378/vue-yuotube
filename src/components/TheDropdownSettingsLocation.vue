<script setup>
import { ref } from 'vue'
import DropdownSettingsListItem from './DropdownSettingsListItem.vue'
import DropdownSettingsHeader from './DropdownSettingsHeader.vue'

defineEmits({ 'select-menu': null })
const selectedLocationIdx = ref(0)
const locations = ref(['United states', 'Russia'])
</script>

<template>
  <DropdownSettingsHeader
    title="Choose your location"
    @back="$emit('select-menu', 'main')"
  />

  <section class="py-2">
    <ul class="max-h-96 overflow-auto">
      <DropdownSettingsListItem
        @click.stop="selectedLocationIdx = locationIdx"
        v-for="(location, locationIdx) in locations"
        :key="locationIdx"
        :active="locationIdx === selectedLocationIdx"
        :label="location"
      />
    </ul>
  </section>
</template>
