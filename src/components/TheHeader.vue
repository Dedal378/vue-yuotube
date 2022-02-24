<script setup>
// import TheDropdownApps from './TheDropdownApps.vue'
// import TheDropdownSettings from './TheDropdownSettings.vue'
import LogoMain from './LogoMain.vue'
import TheSearch from './TheSearch.vue'
import ButtonLogin from './ButtonLogin.vue'
import BaseIcon from './BaseIcon.vue'
</script>

<template>
  <header class="flex justify-between fixed z-30 w-full">
    <!--left-->
    <div class="lg:w-1/4 flex">
      <div class="flex items-center xl:w-64 xl:bg-white pl-4">
        <button class="mr-3 sm:ml-2 sm:mr-6 focus:outline-none">
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

      <button class="ml-4 focus:outline-none">
        <BaseIcon name="microphone" class="h-5 w-5" />
      </button>
    </div>

    <!--right-->
    <div class="flex items-center justify-end lg:w-1/4 sm:space-x-3 p-2 sm:px-4">
      <button class="sm:hidden p-2 focus:outline-none">
        <BaseIcon name="search" class="h-5 w-5" />
      </button>

      <button class="sm:hidden p-2 focus:outline-none">
        <BaseIcon name="microphone" class="h-5 w-5" />
      </button>

      <!--pop-up btn list 1-->
      <button class="relative group p-2 focus:outline-none">
        <BaseIcon name="viewGrid" class="h-5 w-5" />

        <!--<svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 11a7 7 0 01-7 7m0 0a7 7 0 01-7-7m7 7v4m0 0H8m4 0h4m-4-8a3 3 0 01-3-3V5a3 3 0 116 0v6a3 3 0 01-3 3z"></path></svg>-->
        <!--TODO: переделать-->
        <!--<TheDropdownApps />-->
      </button>

      <!--pop-up btn list 2-->
      <button class="relative group p-2 focus:outline-none">
        <BaseIcon name="dotsVertical" class="h-5 w-5" />
        <!--TODO: переделать, второй список-->
        <!--<TheDropdownSettings />-->
      </button>

      <ButtonLogin />
    </div>
  </header>
</template>
