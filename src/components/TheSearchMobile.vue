<script setup>
import { onBeforeMount, onMounted, ref } from 'vue'
import TheSearch from './TheSearch.vue'
import BaseIcon from './BaseIcon.vue'
import BaseTooltip from './BaseTooltip.vue'

const emit = defineEmits('close')
const rootEl = ref(null)

const onClick = (event) => {
  if (!rootEl.value.contains(event.target)) {
    emit('close')
  }
}

onMounted(() => {
  window.addEventListener('click', onClick)
})
onBeforeMount(() => {
  window.removeEventListener('click', onClick)
})
</script>

<template>
  <div ref="rootEl" class="absolute w-full p-2 z-10 flex">
    <BaseTooltip text="Back" right>
      <button @click="$emit('close')" class="mr-2 p-2 focus:outline-none">
        <BaseIcon name="arrowLeft" class="h-5 w-5" />
      </button>
    </BaseTooltip>

    <TheSearch />

    <BaseTooltip text="Search with your voice" left>
      <button class="p-2 focus:outline-none">
        <BaseIcon name="microphone" class="h-5 w-5" />
      </button>
    </BaseTooltip>
  </div>
</template>
