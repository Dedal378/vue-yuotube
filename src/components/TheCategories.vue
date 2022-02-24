<script setup>
import { ref } from 'vue'
import CategoryItem from './CategoryItem.vue'

const categories = ref([
  'All',
  'Trucks',
  'Tool',
  'Machines',
  'Engines',
  'Snow',
  'Ships',
  'Roads',
  'Tanks',
  'Buildings',
  'Mars',
  'Woodworking',
  'Tractors',
  'Songs',
  'Show',
  'Football',
  'Planes',
  'Lives',
  'Streets',
  'Math',
  'Programming',
])
</script>

<template>
  <section class="pt-14 md:pl-24 xl:pl-64 w-full fixed z-10 bg-white bg-opacity-95">
    <div class="border-t border-b px-4 max-w-screen-2xl m-auto">
      <div class="py-3 flex space-x-3 overflow-auto text-sm whitespace-nowrap">
        <CategoryItem
          v-for="category in categories"
          :key="category"
          :category="category"
          :is-active="category === 'All'"
        />
      </div>
    </div>
  </section>
</template>
