<script setup>
import TheDropdownApps from './TheDropdownApps.vue'
import TheDropdownSettings from './TheDropdownSettings.vue'
import LogoMain from './LogoMain.vue'
import TheSearch from './TheSearch.vue'
import ButtonLogin from './ButtonLogin.vue'
import BaseIcon from './BaseIcon.vue'
import BaseTooltip from './BaseTooltip.vue'

defineEmits({
  toggleSidebar: null,
})
</script>

<template>
  <header class="flex justify-between fixed z-30 w-full">
    <!--left-->
    <div class="lg:w-1/4 flex">
      <div class="flex items-center xl:w-64 xl:bg-white pl-4">
        <button @click="$emit('toggleSidebar')" class="mr-3 sm:ml-2 sm:mr-6 focus:outline-none">
          <BaseIcon name="menu" />
        </button>

        <LogoMain />
      </div>
    </div>

    <!--center-->
    <div
      class="hidden sm:flex flex-1 items-center justify-end p-2.5 pl-8 md:pl-12 md:px-8 lg:px-0 lg:w-1/2 max-w-screen-md"
    >
      <TheSearch />

      <BaseTooltip text="Search with your voice">
        <button class="py-2 focus:outline-none">
          <BaseIcon name="microphone" class="h-5 w-5" />
        </button>
      </BaseTooltip>
    </div>

    <!--right-->
    <div class="flex items-center justify-end lg:w-1/4 sm:space-x-3 p-2 sm:px-4">
      <!--hidden on xl  icon search-->
      <BaseTooltip text="Search">
        <button class="sm:hidden p-2 focus:outline-none">
          <BaseIcon name="search" class="h-5 w-5" />
        </button>
      </BaseTooltip>

      <!--hidden on xl icon microphone-->
      <BaseTooltip text="Search with your voice">
        <button class="sm:hidden p-2 focus:outline-none">
          <BaseIcon name="microphone" class="h-5 w-5" />
        </button>
      </BaseTooltip>

      <!--pop-up btn list 1-->
      <TheDropdownApps />

      <!--pop-up btn list 2-->
      <TheDropdownSettings />

      <ButtonLogin />
    </div>
  </header>
</template>
