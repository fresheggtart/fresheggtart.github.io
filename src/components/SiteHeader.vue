<template>
  <header
    class="bg-gray-900 sm:flex sm:items-center sm:justify-between xl:bg-white xl:flex-shrink-0"
  >
    <div
      class="flex items-center justify-between px-4 py-3 xl:w-72 xl:bg-gray-900 xl:justify-center xl:py-5"
    >
      <div>
        <svg
          class="w-auto h-8"
          viewBox="0 0 185 32"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M121.09 28.336c2.352 0 4.392-1.248 5.424-3.12l-2.688-1.536c-.48.984-1.512 1.584-2.76 1.584-1.848 0-3.216-1.368-3.216-3.264 0-1.92 1.368-3.288 3.216-3.288 1.224 0 2.256.624 2.736 1.608l2.664-1.56c-.984-1.848-3.024-3.096-5.376-3.096-3.648 0-6.336 2.76-6.336 6.336 0 3.576 2.688 6.336 6.336 6.336zM137.084 16v1.416c-.864-1.08-2.16-1.752-3.912-1.752-3.192 0-5.832 2.76-5.832 6.336 0 3.576 2.64 6.336 5.832 6.336 1.752 0 3.048-.672 3.912-1.752V28h3.096V16h-3.096zm-3.336 9.384c-1.896 0-3.312-1.368-3.312-3.384s1.416-3.384 3.312-3.384c1.92 0 3.336 1.368 3.336 3.384s-1.416 3.384-3.336 3.384zm16.103-6.408V16h-2.712v-3.36l-3.096.936V16h-2.088v2.976h2.088v4.992c0 3.24 1.464 4.512 5.808 4.032v-2.808c-1.776.096-2.712.072-2.712-1.224v-4.992h2.712zm3.719-4.416c1.056 0 1.92-.864 1.92-1.896s-.864-1.92-1.92-1.92c-1.032 0-1.896.888-1.896 1.92s.864 1.896 1.896 1.896zM152.034 28h3.096V16h-3.096v12zm11.642.336c3.528 0 6.36-2.76 6.36-6.336 0-3.576-2.832-6.336-6.36-6.336-3.528 0-6.336 2.76-6.336 6.336 0 3.576 2.808 6.336 6.336 6.336zm0-3.024c-1.824 0-3.24-1.368-3.24-3.312 0-1.944 1.416-3.312 3.24-3.312 1.848 0 3.264 1.368 3.264 3.312 0 1.944-1.416 3.312-3.264 3.312zm15.21-9.648c-1.608 0-2.856.6-3.576 1.68V16h-3.096v12h3.096v-6.48c0-2.088 1.128-2.976 2.64-2.976 1.392 0 2.376.84 2.376 2.472V28h3.096v-7.368c0-3.192-1.992-4.968-4.536-4.968z"
            fill="#667EEA"
          />
          <path
            d="M61.063 28h3.768l3.144-11.088L71.143 28h3.768l4.704-16.8h-3.48L72.92 23.656 69.391 11.2H66.56l-3.504 12.456L59.84 11.2h-3.48L61.063 28zm24.611.336c3.528 0 6.36-2.76 6.36-6.336 0-3.576-2.832-6.336-6.36-6.336-3.528 0-6.336 2.76-6.336 6.336 0 3.576 2.808 6.336 6.336 6.336zm0-3.024c-1.824 0-3.24-1.368-3.24-3.312 0-1.944 1.416-3.312 3.24-3.312 1.848 0 3.264 1.368 3.264 3.312 0 1.944-1.416 3.312-3.264 3.312zm11.634-7.248V16h-3.096v12h3.096v-5.736c0-2.52 2.04-3.24 3.648-3.048V15.76c-1.512 0-3.024.672-3.648 2.304zM113.831 28l-4.968-6.072L113.687 16h-3.696l-4.128 5.28V11.2h-3.096V28h3.096v-5.448L110.231 28h3.6z"
            fill="#2D3748"
          />
          <path
            fill-rule="evenodd"
            clip-rule="evenodd"
            d="M43.911 12.604L36.213 8.16v20.645h9v2h-44v-2h4v-12.72l-3.728.933L1 15.078l21.09-5.273h3.122a9.552 9.552 0 00-.68 2.559l-.483 3.975 5.164-2.982v15.448h5V8.161l-7.696 4.444a7.502 7.502 0 012.565-4.8h-4.12a7.489 7.489 0 016.646-2.973l-5.591-3.228a7.488 7.488 0 016.696.402c1.039.6 1.88 1.41 2.5 2.347a7.461 7.461 0 012.5-2.347 7.49 7.49 0 016.698-.402l-5.593 3.228a7.488 7.488 0 016.646 2.973h-4.12a7.498 7.498 0 012.567 4.8zM25.213 28.805v-10h-6v10h6zm-11-8a2 2 0 11-4 0 2 2 0 014 0z"
            fill="#667EEA"
          />
        </svg>
      </div>
      <div class="flex sm:hidden">
        <button
          @click="toggle"
          type="button"
          class="px-2 text-gray-500 hover:text-white focus:outline-none focus:text-white"
        >
          <svg v-if="isOpen" class="w-6 h-6 fill-current " viewBox="0 0 100 80">
            <rect width="100" height="20"></rect>
            <rect y="30" width="100" height="20"></rect>
            <rect y="60" width="100" height="20"></rect>
          </svg>

          <svg
            v-else
            class="w-6 h-6 fill-current "
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 20 20"
          >
            <path
              fill-rule="evenodd"
              d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z"
              clip-rule="evenodd"
            />
          </svg>
        </button>
      </div>
    </div>

    <nav
      class="sm:flex sm:items-center sm:px-4 xl:w-full2 xl:h-full2 xl:flex-1 xl:justify-between"
      :class="{ hidden: !isOpen, block: isOpen }"
    >
      <div class="hidden xl:block xl:relative xl:max-w-xl xl:w-full">
        <div
          class="absolute inset-y-0 left-0 flex items-center pl-3 pointer-events-none"
        >
          <svg
            class="w-6 h-6 text-gray-600 fill-current"
            version="1.0"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 1244 1280"
          >
            <path
              d="M402.5 1.1C299.6 9 205.6 51.2 132.1 122.5 33.6 218-13.5 351.7 3.6 487.5c15.6 124.4 84.9 236 189.9 305.9 19.3 12.9 27.2 17.5 47 27.4 45.2 22.7 90.6 36.2 144.5 42.9 20.7 2.5 76.3 2.5 97 0 40.4-5 75.2-13.8 111.5-28.1 25.1-9.8 60-28.3 81.9-43.3l8-5.4 107.5 107.3c383.5 382.7 377 376.2 382.8 379.5 18.9 10.5 41.1 7.5 56.3-7.7 14.8-14.8 18-35.9 8.4-55.3-2.1-4.3-46.2-48.8-243.2-245.9C774 743.5 754.8 724 756 722.3c.8-1 4-4.7 7-8.3 71.4-83.6 108.8-192.7 103.1-301.1-3.2-61-16.5-113.6-42-166.4-16.9-34.9-34-61.5-59.2-92-10.6-12.8-39.5-41.7-52.4-52.4-68.7-56.9-146.3-90-233.6-99.6-17.4-1.9-59.8-2.7-76.4-1.4zm78 94.9c77.7 11.8 145.3 46.3 198.2 101.4 51.6 53.6 82.9 119.4 93 195.1 2.4 18.6 2.4 61.8 0 81-5.4 41.6-15.8 75.8-34.2 112.5-29.7 59.3-77.9 110.1-136 143.2-96.4 54.9-215.3 59-315.2 10.8C188.8 693 119.6 603.6 99 498c-3.7-19.2-5.1-32.3-5.7-55.5-.6-25.8.4-42.3 4.2-65.1 16.1-97.1 74.2-183.1 158.8-234.8 45.3-27.8 93.5-43.4 151.2-49 2.2-.2 16.4-.3 31.5-.1 21.7.3 30.4.8 41.5 2.5z"
            />
          </svg>
        </div>
        <input
          class="w-full inline-block py-2 pl-10 pr-4 border-transparent border:bg-gray-800 text-gray-800 bg-gray-400 rounded-lg focus:outline-none focus:bg-gray-200 focus:text-gray-700"
          placeholder="Search by keywords"
        />
      </div>

      <div class="sm:flex sm:items-center">
        <div
          class="px-2 pt-2 pb-5 border-gray-800 border-b sm:flex sm:border-b-0 sm:pt-0 sm:pb-0 sm:px-0 "
        >
          <a
            class="block px-1 py-1 font-semibold leading-tight text-white rounded hover:bg-gray-800 xl:hover:bg-gray-200 sm:text-sm xl:text-gray-900"
            href="#"
            >List your property</a
          >
          <a
            class="block px-1 py-1 mt-1 sm:mt-0 font-semibold leading-tight text-white rounded hover:bg-gray-800 xl:hover:bg-gray-200 sm:text-sm sm:ml-2 xl:text-gray-900"
            href="#"
            >Trips</a
          >
          <a
            class="block px-1 py-1 mt-1 sm:mt-0 font-semibold leading-tight text-white rounded hover:bg-gray-800 xl:hover:bg-gray-200 sm:text-sm sm:ml-2 xl:text-gray-900"
            href="#"
            >Messages</a
          >
        </div>
        <div class="relative px-5 py-5 sm:py-0 sm:px-0 sm:ml-4">
          <div class="flex items-center sm:hidden">
            <img
              class="object-cover w-10 h-10 border-2 border-gray-600 rounded-full"
              src="https://images.unsplash.com/photo-1484399172022-72a90b12e3c1?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=256&q=60"
              alt=""
            />
            <span
              class="ml-4 font-semibold text-gray-200 sm:hidden xl:border-gray-300"
              >Christine Jan</span
            >
          </div>
          <div class="mt-5 sm:hidden">
            <a class="block text-gray-400 hover:text-white " href="#account"
              >Account settings</a
            >
            <a
              class="block mt-3 text-gray-400 hover:text-white "
              href="#support"
              >Support</a
            >
            <a
              class="block mt-3 text-gray-400 hover:text-white "
              href="#sign-out"
              >Sign out</a
            >
          </div>

          <!-- <span
            class="hidden sm:overflow-hidden sm:h-8 sm:w-8   sm:block sm:border-2 border-gray-600 sm:rounded-full sm:focus:outline-none sm:focus:border-white"
          >
            <img
              class="object-cover w-full h-full  xl:w-12 xl:h-12"
              src="https://images.unsplash.com/photo-1484399172022-72a90b12e3c1?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=256&q=60"
              alt=""
            />
          </span> -->

          <!-- <button
            @click="toggleDropDown"
            type="button"
            class="hidden sm:overflow-hidden sm:h-8 sm:w-8   sm:block sm:border-2 border-gray-600 sm:rounded-full sm:focus:outline-none sm:focus:border-white"
          >
            <img
              class="object-cover w-full h-full  xl:w-12 xl:h-12"
              src="https://images.unsplash.com/photo-1484399172022-72a90b12e3c1?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=256&q=60"
              alt=""
            />
          </button> -->

          <!-- <div :class="[dropdownOpen ? 'sm:block' : 'sm:hidden']">
            <button
              @click="dropdownOpen = false"
              type="button"
              class="hidden sm:block  sm:fixed sm:opacity-0 sm:inset-0 sm:cursor-default sm:w-full sm:h-full"
            ></button> -->

          <DropDown class="hidden sm:block">
            <template #trigger="{ hasFocus, isOpen }">
              <span
                class="overflow-hidden h-8 w-8   block border-2 rounded-full "
                :class="[ (hasFocus || isOpen) ? 'border-white': 'border-gray-600 xl:border-gray-800' ]"
              >
                <img
                  class="object-cover w-full h-full  xl:w-12 xl:h-12"
                  src="https://images.unsplash.com/photo-1484399172022-72a90b12e3c1?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=256&q=60"
                  alt=""
                />
              </span>
            </template>

            <template #dropdown>
              <div
                class=" bg-white xl:border rounded-lg absolute mt-3 right-0 w-48 shadow-xl py-2"
              >
                <a
                  class="block  hover:text-white text-gray-800 px-4 py-2 hover:bg-indigo-500"
                  href="#account"
                  >Account settings</a
                >
                <a
                  class="block  hover:text-white text-gray-800 px-4 py-2 mt-0 hover:bg-indigo-500"
                  href="#support"
                  >Support</a
                >
                <a
                  class="block  hover:text-white text-gray-800 px-4 py-2 mt-0 hover:bg-indigo-500"
                  href="#sign-out"
                  >Sign out</a
                >
              </div>
            </template>
          </DropDown>
          <!-- </div> -->
        </div>
      </div>
    </nav>
  </header>
</template>

<script>
import DropDown from "@/components/DropDown";

export default {
  components: { DropDown },
  props: {},
  data() {
    return {
      isOpen: false,
    };
  },
  methods: {
    toggle() {
      this.isOpen = !this.isOpen;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
