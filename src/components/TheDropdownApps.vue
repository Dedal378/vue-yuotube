<script setup>
import { ref, onMounted } from 'vue'
import DropdownAppsListItem from './DropdownAppsListItem.vue'
import BaseIcon from './BaseIcon.vue'

const isOpen = ref(false)
const el = ref(null)

const closeDropDown = () => (isOpen.value = !isOpen.value)

// обработка click вне элемента
onMounted(() => {
  window.addEventListener('click', (ev) => {
    if (!el.value.contains(ev.target)) {
      closeDropDown()
    }
  })
})
</script>

<template>
  <div class="relative">
    <button @click="closeDropDown" ref="el" class="relative group p-2 focus:outline-none">
      <BaseIcon name="viewGrid" class="h-5 w-5" />
    </button>

    <div v-show="isOpen" class="absolute right-0 sm:left-0 top-9 bg-white w-60 border border-t-0">
      <section class="py-2 border-b">
        <ul>
          <DropdownAppsListItem label="YouTube TV" />
        </ul>
      </section>

      <section class="py-2 border-b">
        <ul>
          <DropdownAppsListItem label="YouTube Music" />
          <DropdownAppsListItem label="YouTube Kids" />
        </ul>
      </section>

      <section class="py-2">
        <ul>
          <DropdownAppsListItem label="Creator Academy" />
          <DropdownAppsListItem label="YouTube for Artist" />
        </ul>
      </section>
    </div>
  </div>
</template>
