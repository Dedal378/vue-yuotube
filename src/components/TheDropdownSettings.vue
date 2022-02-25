<script setup>
import { reactive } from 'vue'
import DropdownSettingsListItem from './DropdownSettingsListItem.vue'

const listItems = reactive([
  { label: 'Appearance: Device theme', icon: 'theme', withSubMenu: true },
  { label: 'Language: English', icon: 'language', withSubMenu: true },
  { label: 'Location: United States', icon: 'location', withSubMenu: true },
  { label: 'Settings', icon: 'settings', withSubMenu: false },
  { label: 'Your data in YouTube', icon: 'data', withSubMenu: false },
  { label: 'Help', icon: 'help', withSubMenu: false },
  { label: 'Send feedback', icon: 'feedback', withSubMenu: false },
  { label: 'Keyboard shortcuts', icon: 'shortcut', withSubMenu: false },
  { label: 'Restricted mode: Off', icon: null, withSubMenu: true },
])
</script>

<template>
  <div class="opacity-100 absolute top-9 -right-full sm:right-0 bg-white w-72 border border-t-0">
    <section class="py-2 border-b">
      <ul>
        <DropdownSettingsListItem
          v-for="listItem in listItems.slice(0, 8)"
          :key="listItem.label"
          :label="listItem.label"
          :icon="listItem.icon"
          :with-sub-menu="listItem.withSubMenu"
        />
      </ul>
    </section>

    <section class="py-2">
      <ul>
        <DropdownSettingsListItem :label="listItems[8].label" :with-sub-menu="listItems[8].withSubMenu" />
      </ul>
    </section>
  </div>
</template>
