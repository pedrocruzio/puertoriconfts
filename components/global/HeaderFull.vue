<template>
  <nav class="bg-gray-800">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-16">
        <div class="flex items-center">
          <div class="flex-shrink-0">
            <NuxtLink to="/">
              <img
                class="h-8 w-8"
                src="https://tailwindui.com/img/logos/workflow-mark-indigo-400.svg"
                alt="Workflow logo"
              />
            </NuxtLink>
          </div>
          <div class="hidden md:block">
            <div class="ml-10 flex items-baseline">
              <NuxtLink
                to="/artists"
                class="
                  ml-4
                  px-3
                  py-2
                  rounded-md
                  text-sm
                  font-medium
                  text-gray-300
                  hover:text-white hover:bg-gray-700
                  focus:outline-none focus:text-white focus:bg-gray-700
                "
                >Artist Directory</NuxtLink
              >

              <NuxtLink
                to="/gallery"
                class="
                  ml-4
                  px-3
                  py-2
                  rounded-md
                  text-sm
                  font-medium
                  text-gray-300
                  hover:text-white hover:bg-gray-700
                  focus:outline-none focus:text-white focus:bg-gray-700
                "
                >Virtual Gallery</NuxtLink
              >

              <NuxtLink
                to="upcoming#"
                class="
                  ml-4
                  px-3
                  py-2
                  rounded-md
                  text-sm
                  font-medium
                  text-gray-300
                  hover:text-white hover:bg-gray-700
                  focus:outline-none focus:text-white focus:bg-gray-700
                "
                v-tooltip="'Coming Soon'"
                >Upcoming Drops</NuxtLink
              >
              <NuxtLink
                to="events#"
                class="
                  ml-4
                  px-3
                  py-2
                  rounded-md
                  text-sm
                  font-medium
                  text-gray-300
                  hover:text-white hover:bg-gray-700
                  focus:outline-none focus:text-white focus:bg-gray-700
                "
                v-tooltip="'Coming Soon'"
                >Events</NuxtLink
              >
              <NuxtLink
                to="stats#"
                class="
                  ml-4
                  px-3
                  py-2
                  rounded-md
                  text-sm
                  font-medium
                  text-gray-300
                  hover:text-white hover:bg-gray-700
                  focus:outline-none focus:text-white focus:bg-gray-700
                "
                v-tooltip="'Coming Soon'"
                >Stats</NuxtLink
              >
            </div>
          </div>
        </div>
        <div class="-mr-2 flex md:hidden">
          <!-- Mobile menu button -->
          <button
            @click="toggle"
            class="
              inline-flex
              items-center
              justify-center
              p-2
              rounded-md
              text-gray-400
              hover:text-white hover:bg-gray-700
              focus:outline-none focus:bg-gray-700 focus:text-white
            "
          >
            <svg
              :class="[isOpen ? 'hidden' : 'block', 'h-6 w-6']"
              stroke="currentColor"
              fill="none"
              viewBox="0 0 24 24"
            >
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
            </svg>
            <svg
              :class="[isOpen ? 'block' : 'hidden', 'h-6 w-6']"
              stroke="currentColor"
              fill="none"
              viewBox="0 0 24 24"
            >
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
            </svg>
          </button>
        </div>
      </div>
    </div>
    <div :class="[isOpen ? '' : 'hidden', 'md:hidden']">
      <div class="px-2 pt-2 pb-3 sm:px-3">
        <a
          href="#"
          class="
            block
            px-3
            py-2
            rounded-md
            text-base
            font-medium
            text-white
            bg-gray-900
            focus:outline-none focus:text-white focus:bg-gray-700
          "
          >Artist Directory</a
        >
        <a
          href="#"
          class="
            mt-1
            block
            px-3
            py-2
            rounded-md
            text-base
            font-medium
            text-gray-300
            hover:text-white hover:bg-gray-700
            focus:outline-none focus:text-white focus:bg-gray-700
          "
          >Virtual Gallery</a
        >
        <a
          href="#"
          class="
            mt-1
            block
            px-3
            py-2
            rounded-md
            text-base
            font-medium
            text-gray-300
            hover:text-white hover:bg-gray-700
            focus:outline-none focus:text-white focus:bg-gray-700
          "
          >Upcoming Drops</a
        >
        <a
          href="#"
          class="
            mt-1
            block
            px-3
            py-2
            rounded-md
            text-base
            font-medium
            text-gray-300
            hover:text-white hover:bg-gray-700
            focus:outline-none focus:text-white focus:bg-gray-700
          "
          >Events</a
        >
        <a
          href="#"
          class="
            mt-1
            block
            px-3
            py-2
            rounded-md
            text-base
            font-medium
            text-gray-300
            hover:text-white hover:bg-gray-700
            focus:outline-none focus:text-white focus:bg-gray-700
          "
          >Stats</a
        >
      </div>
    </div>
  </nav>
</template>

<script>
import 'v-tooltip/dist/v-tooltip.css'

export default {
  name: 'HeaderFull',
  data() {
    return {
      isOpen: false,
    }
  },
  methods: {
    toggle() {
      this.isOpen = !this.isOpen
    },
  },
}
</script>

<style lang="postcss" scoped>
.scrim-bg {
  &::before {
    content: '';
    z-index: -1;
    background-color: var(--bg);
    @apply absolute bottom-0 inset-x-0 h-12 mb-4 transition-colors duration-200 ease-in-out;
  }
  &::after {
    content: '';
    z-index: -1;
    opacity: 1;
    animation: fadeIn1 500ms ease-in-out;
    @apply pointer-events-none absolute bottom-0 inset-x-0 h-16 -mb-12;
    background: linear-gradient(to bottom, #111827, cubic-bezier(0.15, 0, 0.45, 1), transparent);
  }
}
.nuxt-link-exact-active {
  @apply text-gray-200 border-gray-400 bg-gray-800 bg-opacity-25 cursor-default;
}

.light {
  & .scrim-bg {
    &::after {
      animation-name: fadeIn2;
      background: linear-gradient(to bottom, #e5e7eb, cubic-bezier(0.15, 0, 0.45, 1), transparent);
    }
  }
  & .nuxt-link-exact-active {
    @apply text-primary-700 border-gray-600 bg-gray-100;
  }
}

/* Need two because of smoother switching between color modes */
@keyframes fadeIn1 {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@keyframes fadeIn2 {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>
