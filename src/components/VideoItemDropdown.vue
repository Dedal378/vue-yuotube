<script setup>
import { computed, nextTick, onMounted, ref, watch } from 'vue'
import BaseIcon from './BaseIcon.vue'
import VideoItemDropdownListItem from './VideoItemDropdownListItem.vue'

const isOpen = ref(false)
const videoItemDropdown = ref(null)
const videoItemDropdownButton = ref(null)
const positionClasses = ref([])

const buttonClasses = computed(() => {
  return [
    '-mt-1',
    'ml-auto',
    'p-1',
    'opacity-0',
    'group-hover:opacity-100',
    'text-gray-500',
    'hover:text-gray-700',
    'focus:outline-none',
  ]
})
const dropdownClasses = computed(() => {
  return [
    'absolute',
    // 'top-9',
    '-right-full',
    'sm:right-0',
    'bg-white',
    'w-48',
    'rounded',
    'shadow',
    'focus:outline-none',
    ...positionClasses.value,
  ]
})

const toggle = (event) => {
  isOpen.value = !isOpen.value

  if (isOpen.value) {
    nextTick(() => {
      positionClasses.value = getPositionClasses(event)
    })
  }
}
const getPositionClasses = (event) => {
  return [getTopClass(event), getRightClass(), getLeftClass()]
}
const getTopClass = (event) => {
  const clickCoordY = event.clientY
  const buttonHeight = event.currentTarget.offsetHeight
  const dropdownHeight = videoItemDropdown.value.offsetHeight

  if (window.innerHeight - clickCoordY < dropdownHeight) {
    return '-top-14'
  }
  if (window.innerHeight - clickCoordY < dropdownHeight + buttonHeight) {
    return 'top-0'
  }

  return 'top-9'
}
const getRightClass = () => {}
const getLeftClass = () => {}

onMounted(() => {
  window.addEventListener('click', (ev) => {
    if (!videoItemDropdownButton.value.contains(ev.target)) {
      isOpen.value = false
    }
  })
})

watch(isOpen, () => {
  nextTick(() => isOpen.value && videoItemDropdown.value.focus())
})
</script>

<template>
  <div class="relative -mt-1 ml-auto">
    <button @click="toggle" @keydown.esc="isOpen = false" :class="buttonClasses" ref="videoItemDropdownButton">
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
      <div v-show="isOpen" @keydown.esc="isOpen = false" ref="videoItemDropdown" tabindex="-1" :class="dropdownClasses">
        <section class="py-2">
          <ul>
            <VideoItemDropdownListItem label="Add to queue" icon="menuVideo" />
          </ul>
        </section>
      </div>
    </transition>
  </div>
</template>
