<script setup>
// import TheDropdownApps from './TheDropdownApps.vue'
// import TheDropdownSettings from './TheDropdownSettings.vue'
import LogoMain from './LogoMain.vue'
import TheSearch from './TheSearch.vue'
import ButtonLogin from './ButtonLogin.vue'
</script>

<template>
  <header class="flex justify-between fixed z-30 w-full">
    <!--left-->
    <div class="lg:w-1/4 flex">
      <div class="flex items-center xl:w-64 xl:bg-white pl-4">
        <button class="mr-3 sm:ml-2 sm:mr-6 focus:outline-none">
          <svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path d="M4 6h16M4 12h16M4 18h16" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" />
          </svg>
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
        <svg class="h-5 w-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
          <path
            clip-rule="evenodd"
            d="M7 4a3 3 0 016 0v4a3 3 0 11-6 0V4zm4 10.93A7.001 7.001 0 0017 8a1 1 0 10-2 0A5 5 0 015 8a1 1 0 00-2 0 7.001 7.001 0 006 6.93V17H6a1 1 0 100 2h8a1 1 0 100-2h-3v-2.07z"
            fill-rule="evenodd"
          />
        </svg>
      </button>
    </div>

    <!--right-->
    <div class="flex items-center justify-end lg:w-1/4 sm:space-x-3 p-2 sm:px-4">
      <button class="sm:hidden p-2 focus:outline-none">
        <svg class="h-5 w-5" fill="none" stroke="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
          <path
            d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
          />
        </svg>
      </button>

      <button class="sm:hidden p-2 focus:outline-none">
        <svg class="h-5 w-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
          <path
            clip-rule="evenodd"
            d="M7 4a3 3 0 016 0v4a3 3 0 11-6 0V4zm4 10.93A7.001 7.001 0 0017 8a1 1 0 10-2 0A5 5 0 015 8a1 1 0 00-2 0 7.001 7.001 0 006 6.93V17H6a1 1 0 100 2h8a1 1 0 100-2h-3v-2.07z"
            fill-rule="evenodd"
          />
        </svg>
      </button>

      <!--pop-up btn list 1-->
      <button class="relative group p-2 focus:outline-none">
        <svg class="h-5 w-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
          <path
            d="M5 3a2 2 0 00-2 2v2a2 2 0 002 2h2a2 2 0 002-2V5a2 2 0 00-2-2H5zM5 11a2 2 0 00-2 2v2a2 2 0 002 2h2a2 2 0 002-2v-2a2 2 0 00-2-2H5zM11 5a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2V5zM11 13a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2v-2z"
          />
        </svg>
        <!--TODO: переделать-->
        <!--<TheDropdownApps />-->
      </button>

      <!--pop-up btn list 2-->
      <button class="relative group p-2 focus:outline-none">
        <svg class="h-5 w-5" fill="none" stroke="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
          <path
            d="M12 5v.01M12 12v.01M12 19v.01M12 6a1 1 0 110-2 1 1 0 010 2zm0 7a1 1 0 110-2 1 1 0 010 2zm0 7a1 1 0 110-2 1 1 0 010 2z"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
          />
        </svg>
        <!--TODO: переделать, второй список-->
        <!--<TheDropdownSettings />-->
      </button>

      <ButtonLogin />
    </div>
  </header>
</template>
