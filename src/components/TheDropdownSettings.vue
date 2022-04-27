<script setup>
import { computed, nextTick, onMounted, reactive, ref, watch } from 'vue'
import BaseIcon from './BaseIcon.vue'
import BaseTooltip from './BaseTooltip.vue'
import TheDropdownSettingsMain from './TheDropdownSettingsMain.vue'
import TheDropdownSettingsAppearance from './TheDropdownSettingsAppearance.vue'
import TheDropdownSettingsLanguage from './TheDropdownSettingsLanguage.vue'
import TheDropdownSettingsLocation from './TheDropdownSettingsLocation.vue'
import TheDropdownSettingsRestrictedMode from './TheDropdownSettingsRestrictedMode.vue'

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
const selectedOptions = reactive({
  theme: {
    id: 0,
    text: 'Use device theme',
  },
  languageId: 0,
  locationId: 0,
  modeId: false,
})

const menu = computed(() => {
  const menuComponentNames = {
    main: TheDropdownSettingsMain,
    appearance: TheDropdownSettingsAppearance,
    language: TheDropdownSettingsLanguage,
    location: TheDropdownSettingsLocation,
    mode: TheDropdownSettingsRestrictedMode,
  }

  return menuComponentNames[selectedMenu.value]
})

const showSelectedMenu = selMenu => {
  selectedMenu.value = selMenu
  dropDownSettings.value.focus()
}
const close = () => {
  isOpen.value = false
  setTimeout(() => (selectedMenu.value = 'main'), 100)
}
const open = () => {
  isOpen.value = true
}
const toggle = () => {
  isOpen.value ? close() : open()
}
const selectOption = (option) => {
  selectedOptions[option.name] = option.value
}

watch(isOpen, () => {
  nextTick(() => isOpen.value && dropDownSettings.value.focus())
})
onMounted(() => {
  window.addEventListener('click', ev => {
    if (!dropDownSettingsButton.value.contains(ev.target)) {
      close()
    }
  })
})
</script>

<template>
  <div class="relative">
    <BaseTooltip text="Settings">
      <button
        @click="toggle"
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
      <div
        v-show="isOpen"
        @keydown.esc="close"
        :class="dropdownClasses"
        ref="dropDownSettings"
        tabindex="-1"
      >
        <component
          @select-menu="showSelectedMenu"
          @select-option="selectOption"
          :is="menu"
          :selected-options="selectedOptions"
        />
      </div>
    </transition>
  </div>
</template>
