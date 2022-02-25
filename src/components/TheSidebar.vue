<script setup>
import { reactive } from 'vue'
import BaseIcon from './BaseIcon.vue'
import SidebarNavItem from './SidebarNavItem.vue'

const listItems = reactive([
  { label: 'Home', icon: 'home', isActive: true },
  { label: 'Trending', icon: 'trending', isActive: false },
  { label: 'Subscriptions', icon: 'subscriptions', isActive: false },
  { label: 'Library', icon: 'library', isActive: false },
  { label: 'History', icon: 'history', isActive: false },
])
</script>

<template>
  <aside class="hidden xl:block w-64 max-h-screen fixed z-20 top-0 overflow-auto pt-12 bg-white">
    <section class="py-2 border-b">
      <ul>
        <SidebarNavItem
          v-for="listItem in listItems.slice(0, 3)"
          :key="listItem.label"
          :label="listItem.label"
          :icon="listItem.icon"
          :is-active="listItem.isActive"
        />
      </ul>
    </section>
    <section class="py-2 border-b">
      <ul>
        <SidebarNavItem
          v-for="listItem in listItems.slice(3)"
          :key="listItem.label"
          :label="listItem.label"
          :icon="listItem.icon"
          :is-active="listItem.isActive"
        />
      </ul>
    </section>
    <section class="px-8 py-4 border-b font-medium leading-5">
      <span class="text-sm"> Sign in to like videos, comment, and subscribe. </span>
      <button
        class="flex items-center px-2 py-0.5 mt-3 text-sm text-blue-700 uppercase border border-blue-700 rounded-sm focus:outline-none"
      >
        <BaseIcon name="user" class="h-7 w-7 mr-2" />
        Sign in
      </button>
    </section>
    <section class="py-2 border-b">
      <div class="uppercase text-sm font-semibold px-6 py-2">Best of youtube</div>

      <ul>
        <li>
          <a class="flex items-center px-6 py-2 text-sm hover:bg-gray-100" href="#">
            <div class="rounded-full mr-6 p-1 bg-gray-700">
              <svg
                class="h-4 w-4 text-white"
                fill="currentColor"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M18 3a1 1 0 00-1.196-.98l-10 2A1 1 0 006 5v9.114A4.369 4.369 0 005 14c-1.657 0-3 .895-3 2s1.343 2 3 2 3-.895 3-2V7.82l8-1.6v5.894A4.37 4.37 0 0015 12c-1.657 0-3 .895-3 2s1.343 2 3 2 3-.895 3-2V3z"
                />
              </svg>
            </div>
            <span>Music</span>
          </a>
        </li>
        <li>
          <a class="flex items-center px-6 py-2 text-sm hover:bg-gray-100" href="#">
            <div class="rounded-full mr-6 p-1 bg-gray-700">
              <svg
                class="h-4 w-4 text-white"
                fill="currentColor"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  clip-rule="evenodd"
                  d="M18 3a1 1 0 00-1.447-.894L8.763 6H5a3 3 0 000 6h.28l1.771 5.316A1 1 0 008 18h1a1 1 0 001-1v-4.382l6.553 3.276A1 1 0 0018 15V3z"
                  fill-rule="evenodd"
                />
              </svg>
            </div>
            <span>Sports</span>
          </a>
        </li>
        <li>
          <a class="flex items-center px-6 py-2 text-sm hover:bg-gray-100" href="#">
            <div class="rounded-full mr-6 p-1 bg-gray-700">
              <svg
                class="h-4 w-4 text-white"
                fill="currentColor"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M10 3.5a1.5 1.5 0 013 0V4a1 1 0 001 1h3a1 1 0 011 1v3a1 1 0 01-1 1h-.5a1.5 1.5 0 000 3h.5a1 1 0 011 1v3a1 1 0 01-1 1h-3a1 1 0 01-1-1v-.5a1.5 1.5 0 00-3 0v.5a1 1 0 01-1 1H6a1 1 0 01-1-1v-3a1 1 0 00-1-1h-.5a1.5 1.5 0 010-3H4a1 1 0 001-1V6a1 1 0 011-1h3a1 1 0 001-1v-.5z"
                />
              </svg>
            </div>
            <span>Gaming</span>
          </a>
        </li>
        <li>
          <a class="flex items-center px-6 py-2 text-sm hover:bg-gray-100" href="#">
            <div class="rounded-full mr-6 p-1 bg-gray-700">
              <svg
                class="h-4 w-4 text-white"
                fill="currentColor"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  clip-rule="evenodd"
                  d="M4 3a2 2 0 00-2 2v10a2 2 0 002 2h12a2 2 0 002-2V5a2 2 0 00-2-2H4zm3 2h6v4H7V5zm8 8v2h1v-2h-1zm-2-2H7v4h6v-4zm2 0h1V9h-1v2zm1-4V5h-1v2h1zM5 5v2H4V5h1zm0 4H4v2h1V9zm-1 4h1v2H4v-2z"
                  fill-rule="evenodd"
                />
              </svg>
            </div>
            <span>Movies</span>
          </a>
        </li>
        <li>
          <a class="flex items-center px-6 py-2 text-sm hover:bg-gray-100" href="#">
            <div class="rounded-full mr-6 p-1 bg-gray-700">
              <svg
                class="h-4 w-4 text-white"
                fill="currentColor"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  clip-rule="evenodd"
                  d="M2 5a2 2 0 012-2h8a2 2 0 012 2v10a2 2 0 002 2H4a2 2 0 01-2-2V5zm3 1h6v4H5V6zm6 6H5v2h6v-2z"
                  fill-rule="evenodd"
                />
                <path d="M15 7h1a2 2 0 012 2v5.5a1.5 1.5 0 01-3 0V7z" />
              </svg>
            </div>
            <span>News</span>
          </a>
        </li>
        <li>
          <a class="flex items-center px-6 py-2 text-sm hover:bg-gray-100" href="#">
            <div class="rounded-full mr-6 p-1 bg-gray-700">
              <svg
                class="h-4 w-4 text-white"
                fill="currentColor"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  clip-rule="evenodd"
                  d="M5.05 3.636a1 1 0 010 1.414 7 7 0 000 9.9 1 1 0 11-1.414 1.414 9 9 0 010-12.728 1 1 0 011.414 0zm9.9 0a1 1 0 011.414 0 9 9 0 010 12.728 1 1 0 11-1.414-1.414 7 7 0 000-9.9 1 1 0 010-1.414zM7.879 6.464a1 1 0 010 1.414 3 3 0 000 4.243 1 1 0 11-1.415 1.414 5 5 0 010-7.07 1 1 0 011.415 0zm4.242 0a1 1 0 011.415 0 5 5 0 010 7.072 1 1 0 01-1.415-1.415 3 3 0 000-4.242 1 1 0 010-1.415zM10 9a1 1 0 011 1v.01a1 1 0 11-2 0V10a1 1 0 011-1z"
                  fill-rule="evenodd"
                />
              </svg>
            </div>
            <span>Live</span>
          </a>
        </li>
        <li>
          <a class="flex items-center px-6 py-2 text-sm hover:bg-gray-100" href="#">
            <div class="rounded-full mr-6 p-1 bg-gray-700">
              <svg
                class="h-4 w-4 text-white"
                fill="currentColor"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path d="M10 12a2 2 0 100-4 2 2 0 000 4z" />
                <path
                  clip-rule="evenodd"
                  d="M.458 10C1.732 5.943 5.522 3 10 3s8.268 2.943 9.542 7c-1.274 4.057-5.064 7-9.542 7S1.732 14.057.458 10zM14 10a4 4 0 11-8 0 4 4 0 018 0z"
                  fill-rule="evenodd"
                />
              </svg>
            </div>
            <span>360&deg; Video</span>
          </a>
        </li>
      </ul>
    </section>
    <section class="py-2 border-b">
      <ul>
        <li>
          <a class="flex items-center px-6 py-2 text-sm hover:bg-gray-100" href="#">
            <svg class="h-6 w-6 mr-6" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
              <path
                clip-rule="evenodd"
                d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-11a1 1 0 10-2 0v2H7a1 1 0 100 2h2v2a1 1 0 102 0v-2h2a1 1 0 100-2h-2V7z"
                fill-rule="evenodd"
              />
            </svg>
            <span>Browse channels</span>
          </a>
        </li>
      </ul>
    </section>
    <section class="py-2 border-b">
      <div class="uppercase text-sm font-semibold px-6 py-2">More from youtube</div>

      <ul>
        <li>
          <a class="flex items-center px-6 py-2 text-sm hover:bg-gray-100" href="#">
            <svg class="h-6 w-6 mr-6" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
              <path
                clip-rule="evenodd"
                d="M10 18a8 8 0 100-16 8 8 0 000 16zM9.555 7.168A1 1 0 008 8v4a1 1 0 001.555.832l3-2a1 1 0 000-1.664l-3-2z"
                fill-rule="evenodd"
              />
            </svg>
            <span>YouTube Premium</span>
          </a>
        </li>
        <li>
          <a class="flex items-center px-6 py-2 text-sm hover:bg-gray-100" href="#">
            <svg class="h-6 w-6 mr-6" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
              <path
                clip-rule="evenodd"
                d="M5.05 3.636a1 1 0 010 1.414 7 7 0 000 9.9 1 1 0 11-1.414 1.414 9 9 0 010-12.728 1 1 0 011.414 0zm9.9 0a1 1 0 011.414 0 9 9 0 010 12.728 1 1 0 11-1.414-1.414 7 7 0 000-9.9 1 1 0 010-1.414zM7.879 6.464a1 1 0 010 1.414 3 3 0 000 4.243 1 1 0 11-1.415 1.414 5 5 0 010-7.07 1 1 0 011.415 0zm4.242 0a1 1 0 011.415 0 5 5 0 010 7.072 1 1 0 01-1.415-1.415 3 3 0 000-4.242 1 1 0 010-1.415zM10 9a1 1 0 011 1v.01a1 1 0 11-2 0V10a1 1 0 011-1z"
                fill-rule="evenodd"
              />
            </svg>
            <span>Live</span>
          </a>
        </li>
      </ul>
    </section>
    <section class="py-2 border-b">
      <ul>
        <li>
          <a class="flex items-center px-6 py-2 text-sm hover:bg-gray-100" href="#">
            <svg class="h-6 w-6 mr-6" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
              <path
                clip-rule="evenodd"
                d="M11.49 3.17c-.38-1.56-2.6-1.56-2.98 0a1.532 1.532 0 01-2.286.948c-1.372-.836-2.942.734-2.106 2.106.54.886.061 2.042-.947 2.287-1.561.379-1.561 2.6 0 2.978a1.532 1.532 0 01.947 2.287c-.836 1.372.734 2.942 2.106 2.106a1.532 1.532 0 012.287.947c.379 1.561 2.6 1.561 2.978 0a1.533 1.533 0 012.287-.947c1.372.836 2.942-.734 2.106-2.106a1.533 1.533 0 01.947-2.287c1.561-.379 1.561-2.6 0-2.978a1.532 1.532 0 01-.947-2.287c.836-1.372-.734-2.942-2.106-2.106a1.532 1.532 0 01-2.287-.947zM10 13a3 3 0 100-6 3 3 0 000 6z"
                fill-rule="evenodd"
              />
            </svg>
            <span>Settings</span>
          </a>
        </li>
        <li>
          <a class="flex items-center px-6 py-2 text-sm hover:bg-gray-100" href="#">
            <svg class="h-6 w-6 mr-6" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
              <path
                clip-rule="evenodd"
                d="M3 6a3 3 0 013-3h10a1 1 0 01.8 1.6L14.25 8l2.55 3.4A1 1 0 0116 13H6a1 1 0 00-1 1v3a1 1 0 11-2 0V6z"
                fill-rule="evenodd"
              />
            </svg>
            <span>Report history</span>
          </a>
        </li>
        <li>
          <a class="flex items-center px-6 py-2 text-sm hover:bg-gray-100" href="#">
            <svg class="h-6 w-6 mr-6" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
              <path
                clip-rule="evenodd"
                d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-8-3a1 1 0 00-.867.5 1 1 0 11-1.731-1A3 3 0 0113 8a3.001 3.001 0 01-2 2.83V11a1 1 0 11-2 0v-1a1 1 0 011-1 1 1 0 100-2zm0 8a1 1 0 100-2 1 1 0 000 2z"
                fill-rule="evenodd"
              />
            </svg>
            <span>Help</span>
          </a>
        </li>
        <li>
          <a class="flex items-center px-6 py-2 text-sm hover:bg-gray-100" href="#">
            <svg class="h-6 w-6 mr-6" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
              <path
                clip-rule="evenodd"
                d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-7 4a1 1 0 11-2 0 1 1 0 012 0zm-1-9a1 1 0 00-1 1v4a1 1 0 102 0V6a1 1 0 00-1-1z"
                fill-rule="evenodd"
              />
            </svg>
            <span>Send feedback</span>
          </a>
        </li>
      </ul>
    </section>
    <section class="px-6 py-4 text-xs font-semibold space-y-4">
      <div>
        <a class="mr-2" href="#">About</a>
        <a class="mr-2" href="#">Press</a>
        <a class="mr-2" href="#">Copyright</a>
        <a class="mr-2" href="#">Contact us</a>
        <a class="mr-2" href="#">Creators</a>
        <a class="mr-2" href="#">Advertise</a>
        <a class="mr-2" href="#">Developers</a>
      </div>

      <div>
        <a class="mr-2" href="#">Terms</a>
        <a class="mr-2" href="#">Privacy</a>
        <a class="mr-2" href="#">Policy & Safety</a>
        <a class="mr-2" href="#">How YouTube works</a>
        <a class="mr-2" href="#">Test new features</a>
      </div>

      <div class="font-normal text-gray-500">&copy; 2021 Google LLC</div>
    </section>
  </aside>
</template>
