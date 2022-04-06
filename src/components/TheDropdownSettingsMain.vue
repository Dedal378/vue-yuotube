<script setup>
import { reactive } from 'vue'
import DropdownSettingsListItem from './DropdownSettingsListItem.vue'

defineProps({
  selectedOptions: {
    type: [Object, Number, String],
    required: false,
    default: 0,
  },
})
defineEmits(['select-menu', 'select-option'])
const listItems = reactive([
  { id: 'appearance', label: 'Appearance: Device theme', icon: 'theme', withSubMenu: true },
  { id: 'language', label: 'Language: English', icon: 'language', withSubMenu: true },
  { id: 'location', label: 'Location: United States', icon: 'location', withSubMenu: true },
  { id: 'settings', label: 'Settings', icon: 'settings', withSubMenu: false },
  { id: 'data', label: 'Your data in YouTube', icon: 'data', withSubMenu: false },
  { id: 'help', label: 'Help', icon: 'help', withSubMenu: false },
  { id: 'feedback', label: 'Send feedback', icon: 'feedback', withSubMenu: false },
  { id: 'shortcuts', label: 'Keyboard shortcuts', icon: 'shortcut', withSubMenu: false },
  { id: 'mode', label: 'Restricted mode: Off', icon: null, withSubMenu: true },
])

const selectMenu = (listItem) => {
  // listItem.withSubMenu && emit('select-menu', listItem.id)
  if (listItem.withSubMenu) {
    emit('select-menu', listItem.id)
  }
}
</script>

<template>
  <section class="py-2 border-b">
    <ul>
      <DropdownSettingsListItem
        @click.stop="selectMenu(listItem)"
        v-for="listItem in listItems.slice(0, 8)"
        :key="listItem.label"
        :icon="listItem.icon"
        :label="listItem.label"
        :with-sub-menu="listItem.withSubMenu"
      />
    </ul>
  </section>
  <section class="py-2">
    <ul>
      <DropdownSettingsListItem
        @click.stop="$emit('select-menu', listItems[8].id)"
        :label="listItems[8].label"
        :icon="listItems[8].icon"
        :with-sub-menu="listItems[8].withSubMenu"
      />
    </ul>
  </section>
</template>
