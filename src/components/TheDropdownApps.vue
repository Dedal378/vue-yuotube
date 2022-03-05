<script setup>
import { ref, onMounted } from 'vue'
import DropdownAppsListItem from './DropdownAppsListItem.vue'
import BaseIcon from './BaseIcon.vue'

const isOpen = ref(false)
const el = ref(null)

// обработка click вне элемента
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
      <BaseIcon name="viewGrid" class="h-5 w-5" />
    </button>

    <transition
      enter-active-class="transition ease-out duration-100"
      enter-from-class="transition opacity-0 scale-55"
      enter-to-class="transform opacity-100 scale-100"
      leave-active-class="transition ease-in duration-75"
      leave-from-class="transform opacity-100 scale-100"
      leave-to-class="transform opacity-0 scale-55"
    >
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
    </transition>
  </div>
</template>
