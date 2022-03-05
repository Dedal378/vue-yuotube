<script setup>
import { reactive, ref, onMounted } from 'vue'
import DropdownSettingsListItem from './DropdownSettingsListItem.vue'
import BaseIcon from './BaseIcon.vue'

const isOpen = ref(false)
const el = ref(null)
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

onMounted(() => {
  window.addEventListener('click', (ev) => {
    if (!el.value.contains(ev.target)) {
      isOpen.value = false
    }
  })
})
</script>

<template>
  <div class="relative">
    <button @click="isOpen = !isOpen" ref="el" class="relative p-2 focus:outline-none">
      <BaseIcon name="dotsVertical" class="h-5 w-5" />
    </button>

    <transition
      enter-active-class="transition ease-out duration-100"
      enter-from-class="transition opacity-0 scale-55"
      enter-to-class="transform opacity-100 scale-100"
      leave-active-class="transition ease-in duration-75"
      leave-from-class="transform opacity-100 scale-100"
      leave-to-class="transform opacity-0 scale-55"
    >
      <div
        v-show='isOpen'
        class="absolute top-9 -right-full sm:right-0 bg-white w-72 border border-t-0"
      >
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
    </transition>
  </div>
</template>
