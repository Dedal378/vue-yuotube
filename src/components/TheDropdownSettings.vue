<script setup>
import { nextTick, onMounted, reactive, ref, watch } from 'vue'
import BaseIcon from './BaseIcon.vue'
import BaseTooltip from './BaseTooltip.vue'
import TheDropdownSettingsMain from './TheDropdownSettingsMain.vue'
import TheDropdownSettingsAppearance from './TheDropdownSettingsAppearance.vue'

const dropDownSettingsButton = ref(null)
const dropDownSettings = ref(null)
const isOpen = ref(false)
const selectedMenu = ref('main')
const dropdownClasses = reactive([
  'absolute',
  'top-9',
  '-right-full',
  'sm:right-0',
  'bg-white',
  'w-72',
  'border',
  'border-t-0',
  'focus:outline-none',
])

const showSelectedMenu = (selMenu) => {
  selectedMenu.value = selMenu
}

watch(isOpen, () => {
  nextTick(() => isOpen.value && dropDownSettings.value.focus())
})
onMounted(() => {
  window.addEventListener('click', (ev) => {
    if (!dropDownSettingsButton.value.contains(ev.target)) {
      isOpen.value = false
    }
  })
})
</script>

<template>
  <div class="relative">
    <BaseTooltip text="Settings">
      <button
        @click="isOpen = !isOpen"
        @keydown.esc="isOpen = false"
        ref="dropDownSettingsButton"
        class="relative p-2 focus:outline-none"
      >
        <BaseIcon name="dotsVertical" class="h-5 w-5" />
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
      <div v-show="isOpen" @keydown.esc="isOpen = false" :class="dropdownClasses" ref="dropDownSettings" tabindex="-1">
        <TheDropdownSettingsMain v-if="selectedMenu === 'main'" @select-menu="showSelectedMenu" />
        <TheDropdownSettingsAppearance v-else-if="selectedMenu === 'appearance'" @select-menu="showSelectedMenu" />
      </div>
    </transition>
  </div>
</template>
