<script setup>
import DropdownSettingsHeader from './DropdownSettingsHeader.vue'

defineProps({
  selectedOptions: {
    type: [Object, Number, String],
    required: false,
    default: 0,
  },
})
const emits = defineEmits(['select-menu', 'select-option'])
const selectOption = ($event) => {
  emits('select-option', { name: 'modeId', value: $event.target.checked })
}
</script>

<template>
  <DropdownSettingsHeader
    @back="$emit('select-menu', 'main')"
    title="Restricted Mode"
  />

  <section class="px-3 py-4 text-black text-sm">
    <p>
      This helps hide potentially mature videos. No filter is 100% accurate.
    </p>
    <p>This setting only applies to this browser.</p>
    <div class="text-gray-600 font-semibold flex items-center">
      <span class="uppercase mr-2">Activate restricted mode</span>
      <input
        type="checkbox"
        @input="selectOption($event)"
        :checked="selectedOptions.modeId"
      />
    </div>
  </section>
</template>
