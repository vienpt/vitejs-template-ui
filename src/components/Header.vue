<template>
  <div class="bg-white">
    <!-- desktop-->
    <nav class="justify-between hidden h-16 p-6 mx-auto md:flex max-w-7xl">
      <ul class="flex flex-row items-center space-x-10 font-medium">
        <li>
          <figure>
            <a>
              <img
                alt="logo"
                src="../assets/logo.svg"
              />
            </a>
          </figure>
        </li>
        <li>About</li>
        <li>Products</li>
        <li>Pricing</li>
        <li>Blog</li>
        <li>Jobs</li>
        <li class="inline-flex items-center justify-center">
          More
          <span>
            <svg
              x-state:on="Item active"
              x-state:off="Item inactive"
              class="w-5 h-5 ml-1 group-hover:text-gray-500"
              :class="{ 'text-gray-900': open, 'text-gray-700': !(open) }"
              x-description="Heroicon name: solid/chevron-down"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 20 20"
              fill="currentColor"
              aria-hidden="true"
            >
              <path
                fill-rule="evenodd"
                d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
                clip-rule="evenodd"
              ></path>
            </svg>
          </span>
        </li>
      </ul>
      <ul class="flex flex-row items-center space-x-4">
        <li>
          <figure>
            <a>
              <img
                alt="googleStoreBadge"
                src="../assets/Google_Play_Badge.svg"
              />
            </a>
          </figure>
        </li>
        <li>
          <figure>
            <a>
              <img
                alt="googleStoreBadge"
                src="../assets/App_Store_Badge.svg"
              />
            </a>
          </figure>
        </li>
      </ul>
    </nav>
    <!-- mobile menu -->
    <nav class="md:hidden">
      <ul class="flex flex-row items-center justify-between h-16 p-6 mx-auto overflow-hidden">
        <li>
          <figure>
            <a>
              <img
                alt="logo"
                src="../assets/logo.svg"
              />
            </a>
          </figure>
        </li>
        <li
          class="px-2 py-2 cursor-pointer"
          @click="isCollapseMenu = !isCollapseMenu"
          
        >
          <button
            type="button"
            class="text-gray-500 hover:text-gray-700 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500"
            aria-expanded="false"
          >
            <!-- icon buger open -->
            <span class="sr-only">Open menu</span>
            <img
              v-if="!isCollapseMenu"
              alt="openMenu"
              src="../assets/bugger.svg"
            />
            <!-- <svg
              v-if="!isCollapseMenu"
              class="flex w-6 h-6 md:hidden"
              x-description="Heroicon name: outline/menu"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
              aria-hidden="true"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M4 6h16M4 12h16M4 18h16"
              ></path>
            </svg> -->
            <!-- icon x close -->
            <svg
              v-if="isCollapseMenu"
              class="flex w-6 h-6 md:hidden"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
              aria-hidden="true"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M6 18L18 6M6 6l12 12"
              />
            </svg>
          </button>
        </li>
      </ul>
    </nav>
    <!-- end mobile menu -->
    <!-- collapse item menu -->
    <div id="menu-items" :class="!isCollapseMenu ? 'hidden' : 'block'">
      <ul class="fixed flex flex-col justify-start min-w-full min-h-full px-6 py-4 mx-auto space-y-4 overflow-hidden bg-white shadow-xl md:hidden">
        <li>Logo</li>
        <li>About</li>
        <li>Products</li>
        <li>Pricing</li>
        <li>Blog</li>
        <li>Jobs</li>
      </ul>
    </div>
    <!-- end collapse items menu -->
  </div>
</template>

<script lang="ts">
import { ref, defineComponent, reactive, computed } from "vue";

export default defineComponent({
  name: "Header",
  setup: () => {
    const isCollapseMenu = ref(false);
    // const isMenu = document.getElementById("#menu-items")
    // const doubleCount = computed(() => isCollapseMenu ? console.log(isMenu) : null)

    return { isCollapseMenu };
  },
});
</script>
