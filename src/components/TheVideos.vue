<script>
export default {
  name: 'TheVideos',
}
</script>

<template>
  <main class="md:ml-24 xl:ml-64 pt-32 px-5 pb-5">
    <div
      class="grid sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 2xl:grid-cols-5 gap-4 max-w-screen-2xl m-auto"
    >
      <a class="mb-7 group" href="#">
        <div class="relative">
          <img alt="image" src="https://picsum.photos/seed/picsum/720/404" />

          <span
            class="absolute opacity-0 group-hover:opacity-100 bg-opacity-60 top-0 right-0 bg-black text-white rounded-sm m-1 p-1"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                clip-rule="evenodd"
                d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z"
                fill-rule="evenodd"
              />
            </svg>
          </span>

          <span
            class="absolute opacity-0 group-hover:opacity-100 bg-opacity-60 top-8 right-0 bg-black text-white rounded-sm m-1 p-1"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                clip-rule="evenodd"
                d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM9 15a1 1 0 011-1h6a1 1 0 110 2h-6a1 1 0 01-1-1z"
                fill-rule="evenodd"
              />
            </svg>
          </span>

          <span
            class="absolute opacity-100 group-hover:opacity-0 duration-500 bottom-0 right-0 bg-black text-white rounded-sm m-1 p-1 text-xs font-semibold"
            >6:35</span
          >
        </div>

        <div class="flex items-start mt-3">
          <img
            alt="image"
            class="mr-3 rounded-full w-9 h-9"
            src="https://picsum.photos/seed/avatar1/68"
          />

          <div class="text-xs whitespace-nowrap">
            <span class="font-semibold text-gray-800">Video title 1</span>

            <div class="flex items-center mt-1">
              <span class="mb-1">Channel name 1</span>
              <svg
                class="h-3.5 w-3.5 ml-1"
                fill="currentColor"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  clip-rule="evenodd"
                  d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                  fill-rule="evenodd"
                />
              </svg>
            </div>

            <div>
              <span>1k views</span>
              &middot;
              <span>1 day ago</span>
            </div>
          </div>

          <button
            class="ml-auto p-0.5 -mt-1 opacity-0 group-hover:opacity-100 text-gray-500 hover:text-gray-700 focus:outline-none"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"
              />
            </svg>
          </button>
        </div>
      </a>
      <a class="mb-7 group" href="#">
        <div class="relative">
          <img alt="image" src="https://picsum.photos/seed/picsum2/720/404" />

          <span
            class="absolute opacity-0 group-hover:opacity-100 bg-opacity-60 top-0 right-0 bg-black text-white rounded-sm m-1 p-1"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                clip-rule="evenodd"
                d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z"
                fill-rule="evenodd"
              />
            </svg>
          </span>

          <span
            class="absolute opacity-0 group-hover:opacity-100 bg-opacity-60 top-8 right-0 bg-black text-white rounded-sm m-1 p-1"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                clip-rule="evenodd"
                d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM9 15a1 1 0 011-1h6a1 1 0 110 2h-6a1 1 0 01-1-1z"
                fill-rule="evenodd"
              />
            </svg>
          </span>

          <span
            class="absolute opacity-100 group-hover:opacity-0 duration-500 bottom-0 right-0 bg-black text-white rounded-sm m-1 p-1 text-xs font-semibold"
            >6:35</span
          >
        </div>

        <div class="flex items-start mt-3">
          <img
            alt="image"
            class="mr-3 rounded-full w-9 h-9"
            src="https://picsum.photos/seed/avatar2/68"
          />

          <div class="text-xs whitespace-nowrap">
            <span class="font-semibold text-gray-800">Video title 1</span>

            <div class="flex items-center mt-1">
              <span class="mb-1">Channel name 1</span>
              <svg
                class="h-3.5 w-3.5 ml-1"
                fill="currentColor"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  clip-rule="evenodd"
                  d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                  fill-rule="evenodd"
                />
              </svg>
            </div>

            <div>
              <span>1k views</span>
              &middot;
              <span>1 day ago</span>
            </div>
          </div>

          <button
            class="ml-auto p-0.5 -mt-1 opacity-0 group-hover:opacity-100 text-gray-500 hover:text-gray-700 focus:outline-none"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"
              />
            </svg>
          </button>
        </div>
      </a>
      <a class="mb-7 group" href="#">
        <div class="relative">
          <img alt="image" src="https://picsum.photos/seed/picsum3/720/404" />

          <span
            class="absolute opacity-0 group-hover:opacity-100 bg-opacity-60 top-0 right-0 bg-black text-white rounded-sm m-1 p-1"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                clip-rule="evenodd"
                d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z"
                fill-rule="evenodd"
              />
            </svg>
          </span>

          <span
            class="absolute opacity-0 group-hover:opacity-100 bg-opacity-60 top-8 right-0 bg-black text-white rounded-sm m-1 p-1"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                clip-rule="evenodd"
                d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM9 15a1 1 0 011-1h6a1 1 0 110 2h-6a1 1 0 01-1-1z"
                fill-rule="evenodd"
              />
            </svg>
          </span>

          <span
            class="absolute opacity-100 group-hover:opacity-0 duration-500 bottom-0 right-0 bg-black text-white rounded-sm m-1 p-1 text-xs font-semibold"
            >6:35</span
          >
        </div>

        <div class="flex items-start mt-3">
          <img
            alt="image"
            class="mr-3 rounded-full w-9 h-9"
            src="https://picsum.photos/seed/avatar3/68"
          />

          <div class="text-xs whitespace-nowrap">
            <span class="font-semibold text-gray-800">Video title 1</span>

            <div class="flex items-center mt-1">
              <span class="mb-1">Channel name 1</span>
              <svg
                class="h-3.5 w-3.5 ml-1"
                fill="currentColor"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  clip-rule="evenodd"
                  d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                  fill-rule="evenodd"
                />
              </svg>
            </div>

            <div>
              <span>1k views</span>
              &middot;
              <span>1 day ago</span>
            </div>
          </div>

          <button
            class="ml-auto p-0.5 -mt-1 opacity-0 group-hover:opacity-100 text-gray-500 hover:text-gray-700 focus:outline-none"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"
              />
            </svg>
          </button>
        </div>
      </a>
      <a class="mb-7 group" href="#">
        <div class="relative">
          <img alt="image" src="https://picsum.photos/seed/picsum4/720/404" />

          <span
            class="absolute opacity-0 group-hover:opacity-100 bg-opacity-60 top-0 right-0 bg-black text-white rounded-sm m-1 p-1"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                clip-rule="evenodd"
                d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z"
                fill-rule="evenodd"
              />
            </svg>
          </span>

          <span
            class="absolute opacity-0 group-hover:opacity-100 bg-opacity-60 top-8 right-0 bg-black text-white rounded-sm m-1 p-1"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                clip-rule="evenodd"
                d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM9 15a1 1 0 011-1h6a1 1 0 110 2h-6a1 1 0 01-1-1z"
                fill-rule="evenodd"
              />
            </svg>
          </span>

          <span
            class="absolute opacity-100 group-hover:opacity-0 duration-500 bottom-0 right-0 bg-black text-white rounded-sm m-1 p-1 text-xs font-semibold"
            >6:35</span
          >
        </div>

        <div class="flex items-start mt-3">
          <img
            alt="image"
            class="mr-3 rounded-full w-9 h-9"
            src="https://picsum.photos/seed/avatar4/6"
          />

          <div class="text-xs whitespace-nowrap">
            <span class="font-semibold text-gray-800">Video title 1</span>

            <div class="flex items-center mt-1">
              <span class="mb-1">Channel name 1</span>
              <svg
                class="h-3.5 w-3.5 ml-1"
                fill="currentColor"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  clip-rule="evenodd"
                  d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                  fill-rule="evenodd"
                />
              </svg>
            </div>

            <div>
              <span>1k views</span>
              &middot;
              <span>1 day ago</span>
            </div>
          </div>

          <button
            class="ml-auto p-0.5 -mt-1 opacity-0 group-hover:opacity-100 text-gray-500 hover:text-gray-700 focus:outline-none"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"
              />
            </svg>
          </button>
        </div>
      </a>
      <a class="mb-7 group" href="#">
        <div class="relative">
          <img alt="image" src="https://picsum.photos/seed/picsum5/720/404" />

          <span
            class="absolute opacity-0 group-hover:opacity-100 bg-opacity-60 top-0 right-0 bg-black text-white rounded-sm m-1 p-1"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                clip-rule="evenodd"
                d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z"
                fill-rule="evenodd"
              />
            </svg>
          </span>

          <span
            class="absolute opacity-0 group-hover:opacity-100 bg-opacity-60 top-8 right-0 bg-black text-white rounded-sm m-1 p-1"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                clip-rule="evenodd"
                d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM9 15a1 1 0 011-1h6a1 1 0 110 2h-6a1 1 0 01-1-1z"
                fill-rule="evenodd"
              />
            </svg>
          </span>

          <span
            class="absolute opacity-100 group-hover:opacity-0 duration-500 bottom-0 right-0 bg-black text-white rounded-sm m-1 p-1 text-xs font-semibold"
            >6:35</span
          >
        </div>

        <div class="flex items-start mt-3">
          <img
            alt="image"
            class="mr-3 rounded-full w-9 h-9"
            src="https://picsum.photos/seed/avatar5/68"
          />

          <div class="text-xs whitespace-nowrap">
            <span class="font-semibold text-gray-800">Video title 1</span>

            <div class="flex items-center mt-1">
              <span class="mb-1">Channel name 1</span>
              <svg
                class="h-3.5 w-3.5 ml-1"
                fill="currentColor"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  clip-rule="evenodd"
                  d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                  fill-rule="evenodd"
                />
              </svg>
            </div>

            <div>
              <span>1k views</span>
              &middot;
              <span>1 day ago</span>
            </div>
          </div>

          <button
            class="ml-auto p-0.5 -mt-1 opacity-0 group-hover:opacity-100 text-gray-500 hover:text-gray-700 focus:outline-none"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"
              />
            </svg>
          </button>
        </div>
      </a>
      <a class="mb-7 group" href="#">
        <div class="relative">
          <img alt="image" src="https://picsum.photos/seed/picsum6/720/404" />

          <span
            class="absolute opacity-0 group-hover:opacity-100 bg-opacity-60 top-0 right-0 bg-black text-white rounded-sm m-1 p-1"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                clip-rule="evenodd"
                d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z"
                fill-rule="evenodd"
              />
            </svg>
          </span>

          <span
            class="absolute opacity-0 group-hover:opacity-100 bg-opacity-60 top-8 right-0 bg-black text-white rounded-sm m-1 p-1"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                clip-rule="evenodd"
                d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM9 15a1 1 0 011-1h6a1 1 0 110 2h-6a1 1 0 01-1-1z"
                fill-rule="evenodd"
              />
            </svg>
          </span>

          <span
            class="absolute opacity-100 group-hover:opacity-0 duration-500 bottom-0 right-0 bg-black text-white rounded-sm m-1 p-1 text-xs font-semibold"
            >6:35</span
          >
        </div>

        <div class="flex items-start mt-3">
          <img
            alt="image"
            class="mr-3 rounded-full w-9 h-9"
            src="https://picsum.photos/seed/avatar6/68"
          />

          <div class="text-xs whitespace-nowrap">
            <span class="font-semibold text-gray-800">Video title 1</span>

            <div class="flex items-center mt-1">
              <span class="mb-1">Channel name 1</span>
              <svg
                class="h-3.5 w-3.5 ml-1"
                fill="currentColor"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  clip-rule="evenodd"
                  d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                  fill-rule="evenodd"
                />
              </svg>
            </div>

            <div>
              <span>1k views</span>
              &middot;
              <span>1 day ago</span>
            </div>
          </div>

          <button
            class="ml-auto p-0.5 -mt-1 opacity-0 group-hover:opacity-100 text-gray-500 hover:text-gray-700 focus:outline-none"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"
              />
            </svg>
          </button>
        </div>
      </a>
      <a class="mb-7 group" href="#">
        <div class="relative">
          <img alt="image" src="https://picsum.photos/seed/picsum7/720/404" />

          <span
            class="absolute opacity-0 group-hover:opacity-100 bg-opacity-60 top-0 right-0 bg-black text-white rounded-sm m-1 p-1"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                clip-rule="evenodd"
                d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z"
                fill-rule="evenodd"
              />
            </svg>
          </span>

          <span
            class="absolute opacity-0 group-hover:opacity-100 bg-opacity-60 top-8 right-0 bg-black text-white rounded-sm m-1 p-1"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                clip-rule="evenodd"
                d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM9 15a1 1 0 011-1h6a1 1 0 110 2h-6a1 1 0 01-1-1z"
                fill-rule="evenodd"
              />
            </svg>
          </span>

          <span
            class="absolute opacity-100 group-hover:opacity-0 duration-500 bottom-0 right-0 bg-black text-white rounded-sm m-1 p-1 text-xs font-semibold"
            >6:35</span
          >
        </div>

        <div class="flex items-start mt-3">
          <img
            alt="image"
            class="mr-3 rounded-full w-9 h-9"
            src="https://picsum.photos/seed/avatar7/68"
          />

          <div class="text-xs whitespace-nowrap">
            <span class="font-semibold text-gray-800">Video title 1</span>

            <div class="flex items-center mt-1">
              <span class="mb-1">Channel name 1</span>
              <svg
                class="h-3.5 w-3.5 ml-1"
                fill="currentColor"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  clip-rule="evenodd"
                  d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                  fill-rule="evenodd"
                />
              </svg>
            </div>

            <div>
              <span>1k views</span>
              &middot;
              <span>1 day ago</span>
            </div>
          </div>

          <button
            class="ml-auto p-0.5 -mt-1 opacity-0 group-hover:opacity-100 text-gray-500 hover:text-gray-700 focus:outline-none"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"
              />
            </svg>
          </button>
        </div>
      </a>
      <a class="mb-7 group" href="#">
        <div class="relative">
          <img alt="image" src="https://picsum.photos/seed/picsum8/720/404" />

          <span
            class="absolute opacity-0 group-hover:opacity-100 bg-opacity-60 top-0 right-0 bg-black text-white rounded-sm m-1 p-1"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                clip-rule="evenodd"
                d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z"
                fill-rule="evenodd"
              />
            </svg>
          </span>

          <span
            class="absolute opacity-0 group-hover:opacity-100 bg-opacity-60 top-8 right-0 bg-black text-white rounded-sm m-1 p-1"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                clip-rule="evenodd"
                d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM9 15a1 1 0 011-1h6a1 1 0 110 2h-6a1 1 0 01-1-1z"
                fill-rule="evenodd"
              />
            </svg>
          </span>

          <span
            class="absolute opacity-100 group-hover:opacity-0 duration-500 bottom-0 right-0 bg-black text-white rounded-sm m-1 p-1 text-xs font-semibold"
            >6:35</span
          >
        </div>

        <div class="flex items-start mt-3">
          <img
            alt="image"
            class="mr-3 rounded-full w-9 h-9"
            src="https://picsum.photos/seed/avatar8/68"
          />

          <div class="text-xs whitespace-nowrap">
            <span class="font-semibold text-gray-800">Video title 1</span>

            <div class="flex items-center mt-1">
              <span class="mb-1">Channel name 1</span>
              <svg
                class="h-3.5 w-3.5 ml-1"
                fill="currentColor"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  clip-rule="evenodd"
                  d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                  fill-rule="evenodd"
                />
              </svg>
            </div>

            <div>
              <span>1k views</span>
              &middot;
              <span>1 day ago</span>
            </div>
          </div>

          <button
            class="ml-auto p-0.5 -mt-1 opacity-0 group-hover:opacity-100 text-gray-500 hover:text-gray-700 focus:outline-none"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"
              />
            </svg>
          </button>
        </div>
      </a>
      <a class="mb-7 group" href="#">
        <div class="relative">
          <img alt="image" src="https://picsum.photos/seed/picsum9/720/404" />

          <span
            class="absolute opacity-0 group-hover:opacity-100 bg-opacity-60 top-0 right-0 bg-black text-white rounded-sm m-1 p-1"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                clip-rule="evenodd"
                d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z"
                fill-rule="evenodd"
              />
            </svg>
          </span>

          <span
            class="absolute opacity-0 group-hover:opacity-100 bg-opacity-60 top-8 right-0 bg-black text-white rounded-sm m-1 p-1"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                clip-rule="evenodd"
                d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM9 15a1 1 0 011-1h6a1 1 0 110 2h-6a1 1 0 01-1-1z"
                fill-rule="evenodd"
              />
            </svg>
          </span>

          <span
            class="absolute opacity-100 group-hover:opacity-0 duration-500 bottom-0 right-0 bg-black text-white rounded-sm m-1 p-1 text-xs font-semibold"
            >6:35</span
          >
        </div>

        <div class="flex items-start mt-3">
          <img
            alt="image"
            class="mr-3 rounded-full w-9 h-9"
            src="https://picsum.photos/seed/avatar9/68"
          />

          <div class="text-xs whitespace-nowrap">
            <span class="font-semibold text-gray-800">Video title 1</span>

            <div class="flex items-center mt-1">
              <span class="mb-1">Channel name 1</span>
              <svg
                class="h-3.5 w-3.5 ml-1"
                fill="currentColor"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  clip-rule="evenodd"
                  d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                  fill-rule="evenodd"
                />
              </svg>
            </div>

            <div>
              <span>1k views</span>
              &middot;
              <span>1 day ago</span>
            </div>
          </div>

          <button
            class="ml-auto p-0.5 -mt-1 opacity-0 group-hover:opacity-100 text-gray-500 hover:text-gray-700 focus:outline-none"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"
              />
            </svg>
          </button>
        </div>
      </a>
      <a class="mb-7 group" href="#">
        <div class="relative">
          <img alt="image" src="https://picsum.photos/seed/picsum10/720/404" />

          <span
            class="absolute opacity-0 group-hover:opacity-100 bg-opacity-60 top-0 right-0 bg-black text-white rounded-sm m-1 p-1"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                clip-rule="evenodd"
                d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z"
                fill-rule="evenodd"
              />
            </svg>
          </span>

          <span
            class="absolute opacity-0 group-hover:opacity-100 bg-opacity-60 top-8 right-0 bg-black text-white rounded-sm m-1 p-1"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                clip-rule="evenodd"
                d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM9 15a1 1 0 011-1h6a1 1 0 110 2h-6a1 1 0 01-1-1z"
                fill-rule="evenodd"
              />
            </svg>
          </span>

          <span
            class="absolute opacity-100 group-hover:opacity-0 duration-500 bottom-0 right-0 bg-black text-white rounded-sm m-1 p-1 text-xs font-semibold"
            >6:35</span
          >
        </div>

        <div class="flex items-start mt-3">
          <img
            alt="image"
            class="mr-3 rounded-full w-9 h-9"
            src="https://picsum.photos/seed/avatar10/68"
          />

          <div class="text-xs whitespace-nowrap">
            <span class="font-semibold text-gray-800">Video title 1</span>

            <div class="flex items-center mt-1">
              <span class="mb-1">Channel name 1</span>
              <svg
                class="h-3.5 w-3.5 ml-1"
                fill="currentColor"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  clip-rule="evenodd"
                  d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                  fill-rule="evenodd"
                />
              </svg>
            </div>

            <div>
              <span>1k views</span>
              &middot;
              <span>1 day ago</span>
            </div>
          </div>

          <button
            class="ml-auto p-0.5 -mt-1 opacity-0 group-hover:opacity-100 text-gray-500 hover:text-gray-700 focus:outline-none"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"
              />
            </svg>
          </button>
        </div>
      </a>
      <a class="mb-7 group" href="#">
        <div class="relative">
          <img alt="image" src="https://picsum.photos/seed/picsum11/720/404" />

          <span
            class="absolute opacity-0 group-hover:opacity-100 bg-opacity-60 top-0 right-0 bg-black text-white rounded-sm m-1 p-1"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                clip-rule="evenodd"
                d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z"
                fill-rule="evenodd"
              />
            </svg>
          </span>

          <span
            class="absolute opacity-0 group-hover:opacity-100 bg-opacity-60 top-8 right-0 bg-black text-white rounded-sm m-1 p-1"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                clip-rule="evenodd"
                d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM9 15a1 1 0 011-1h6a1 1 0 110 2h-6a1 1 0 01-1-1z"
                fill-rule="evenodd"
              />
            </svg>
          </span>

          <span
            class="absolute opacity-100 group-hover:opacity-0 duration-500 bottom-0 right-0 bg-black text-white rounded-sm m-1 p-1 text-xs font-semibold"
            >6:35</span
          >
        </div>

        <div class="flex items-start mt-3">
          <img
            alt="image"
            class="mr-3 rounded-full w-9 h-9"
            src="https://picsum.photos/seed/avatar11/68"
          />

          <div class="text-xs whitespace-nowrap">
            <span class="font-semibold text-gray-800">Video title 1</span>

            <div class="flex items-center mt-1">
              <span class="mb-1">Channel name 1</span>
              <svg
                class="h-3.5 w-3.5 ml-1"
                fill="currentColor"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  clip-rule="evenodd"
                  d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                  fill-rule="evenodd"
                />
              </svg>
            </div>

            <div>
              <span>1k views</span>
              &middot;
              <span>1 day ago</span>
            </div>
          </div>

          <button
            class="ml-auto p-0.5 -mt-1 opacity-0 group-hover:opacity-100 text-gray-500 hover:text-gray-700 focus:outline-none"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"
              />
            </svg>
          </button>
        </div>
      </a>
      <a class="mb-7 group" href="#">
        <div class="relative">
          <img alt="image" src="https://picsum.photos/seed/picsum12/720/404" />

          <span
            class="absolute opacity-0 group-hover:opacity-100 bg-opacity-60 top-0 right-0 bg-black text-white rounded-sm m-1 p-1"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                clip-rule="evenodd"
                d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z"
                fill-rule="evenodd"
              />
            </svg>
          </span>

          <span
            class="absolute opacity-0 group-hover:opacity-100 bg-opacity-60 top-8 right-0 bg-black text-white rounded-sm m-1 p-1"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                clip-rule="evenodd"
                d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM9 15a1 1 0 011-1h6a1 1 0 110 2h-6a1 1 0 01-1-1z"
                fill-rule="evenodd"
              />
            </svg>
          </span>

          <span
            class="absolute opacity-100 group-hover:opacity-0 duration-500 bottom-0 right-0 bg-black text-white rounded-sm m-1 p-1 text-xs font-semibold"
            >6:35</span
          >
        </div>

        <div class="flex items-start mt-3">
          <img
            alt="image"
            class="mr-3 rounded-full w-9 h-9"
            src="https://picsum.photos/seed/avatar12/68"
          />

          <div class="text-xs whitespace-nowrap">
            <span class="font-semibold text-gray-800">Video title 1</span>

            <div class="flex items-center mt-1">
              <span class="mb-1">Channel name 1</span>
              <svg
                class="h-3.5 w-3.5 ml-1"
                fill="currentColor"
                viewBox="0 0 20 20"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  clip-rule="evenodd"
                  d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                  fill-rule="evenodd"
                />
              </svg>
            </div>

            <div>
              <span>1k views</span>
              &middot;
              <span>1 day ago</span>
            </div>
          </div>

          <button
            class="ml-auto p-0.5 -mt-1 opacity-0 group-hover:opacity-100 text-gray-500 hover:text-gray-700 focus:outline-none"
          >
            <svg
              class="h-5 w-5"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"
              />
            </svg>
          </button>
        </div>
      </a>
    </div>
  </main>
</template>
