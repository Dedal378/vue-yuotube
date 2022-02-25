<script setup>
import BaseIcon from './BaseIcon.vue'
</script>

<template>
  <div class="opacity-100 absolute top-9 -right-full sm:right-0 bg-white w-72 border border-t-0">
    <section class="py-2 border-b">
      <ul>
        <li>
          <a class="flex items-center px-4 py-2 text-sm hover:bg-gray-100" href="#">
            <BaseIcon name="theme" class="h-6 w-6 mr-3 text-gray-400" />
            <span>Appearance: Device theme</span>
            <BaseIcon name="arrow" class="h-5 w-5 text-gray-400 ml-auto" />
          </a>
        </li>
        <li>
          <a class="flex items-center px-4 py-2 text-sm hover:bg-gray-100" href="#">
            <BaseIcon name="language" class="h-6 w-6 mr-3 text-gray-400" />
            <span>Language: English</span>
            <BaseIcon name="arrow" class="h-5 w-5 text-gray-400 ml-auto" />
          </a>
        </li>
        <li>
          <a class="flex items-center px-4 py-2 text-sm hover:bg-gray-100" href="#">
            <BaseIcon name="location" class="h-6 w-6 mr-3 text-gray-400" />
            <span>Location: United States</span>
            <BaseIcon name="arrow" class="h-5 w-5 text-gray-400 ml-auto" />
          </a>
        </li>

        <li>
          <a class="flex items-center px-4 py-2 text-sm hover:bg-gray-100" href="#">
            <BaseIcon name="settings" class="h-6 w-6 mr-3 text-gray-400" />
            <span>Settings</span>
          </a>
        </li>
        <li>
          <a class="flex items-center px-4 py-2 text-sm hover:bg-gray-100" href="#">
            <BaseIcon name="data" class="h-6 w-6 mr-3 text-gray-400" />
            <span>Your data in YouTube</span>
          </a>
        </li>
        <li>
          <a class="flex items-center px-4 py-2 text-sm hover:bg-gray-100" href="#">
            <BaseIcon name="help" class="h-6 w-6 mr-3 text-gray-400" />
            <span>Help</span>
          </a>
        </li>
        <li>
          <a class="flex items-center px-4 py-2 text-sm hover:bg-gray-100" href="#">
            <BaseIcon name="feedback" class="h-6 w-6 mr-3 text-gray-400" />
            <span>Send feedback</span>
          </a>
        </li>
        <li>
          <a class="flex items-center px-4 py-2 text-sm hover:bg-gray-100" href="#">
            <BaseIcon name="shortcut" class="h-6 w-6 mr-3 text-gray-400" />
            <span>Keyboard shortcuts</span>
          </a>
        </li>
      </ul>
    </section>

    <section class="py-2">
      <ul>
        <li>
          <a class="flex items-center px-4 py-2 text-sm hover:bg-gray-100" href="#">
            <span>Restricted Mode: Off</span>
            <BaseIcon name="arrow" class="h-5 w-5 text-gray-400 ml-auto" />
          </a>
        </li>
      </ul>
    </section>
  </div>
</template>
