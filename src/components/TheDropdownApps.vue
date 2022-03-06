<script setup>
import { nextTick, onMounted, ref, watch } from 'vue'
import BaseIcon from './BaseIcon.vue'
import DropdownAppsListItem from './DropdownAppsListItem.vue'
import BaseTooltip from './BaseTooltip.vue'

const isOpen = ref(false)
const dropDownAppsButton = ref(null)
const dropDownApps = ref(null)

onMounted(() => {
  // обработка click вне элемента
  window.addEventListener('click', (ev) => {
    if (!dropDownAppsButton.value.contains(ev.target)) {
      isOpen.value = false
    }
  })
})

watch(isOpen, () => {
  nextTick(() => isOpen.value && dropDownApps.value.focus()) //выражение выполнится, если isOpen не null и не undefined
})
</script>

<template>
  <div class="relative">
    <BaseTooltip text="YouTube apps">
      <button @click="isOpen = !isOpen" ref="dropDownAppsButton" class="relative p-2 focus:outline-none">
        <BaseIcon name="viewGrid" class="h-5 w-5" />
      </button>
    </BaseTooltip>

    <transition
      enter-active-class="transition ease-out duration-100"
      enter-from-class="transition opacity-0 scale-55"
      enter-to-class="transform opacity-100 scale-100"
      leave-active-class="transition ease-in duration-75"
      leave-from-class="transform opacity-100 scale-100"
      leave-to-class="transform opacity-0 scale-55"
    >
      <div
        v-show="isOpen"
        @keydown.esc="isOpen = false"
        ref="dropDownApps"
        tabindex="-1"
        class="absolute right-0 sm:left-0 top-9 bg-white w-60 border border-t-0 focus:outline-none"
      >
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
