<template>
  <nav class="bg-violet-400 px-[clamp(1.5rem,8vw,20rem)] py-5 sticky top-0 z-50">
    <div class="flex items-center justify-between">
      <!-- Brand Logo -->
      <a href="#" class="text-2xl font-bold text-white">Danai Akrivou</a>

      <!-- Desktop Navigation -->
      <div class="hidden md:flex space-x-12 text-xl">
        <a
          v-for="link in links"
          :key="link.name"
          :href="link.href"
          class="text-white hover:text-blue-600 transition-colors"
        >
          {{ link.name }}
        </a>
      </div>

      <!-- Hamburger Button (Visible on Mobile / Tablet) -->
      <button
        type="button"
        class="md:hidden text-white focus:outline-none p-2 rounded hover:bg-violet-500 transition-colors"
        aria-label="Toggle Navigation Menu"
        :aria-expanded="isOpen"
        @click="toggleMenu"
      >
        <!-- Icon: Burger (shown when closed) -->
        <svg
          v-if="!isOpen"
          class="w-7 h-7"
          fill="none"
          stroke="currentColor"
          viewBox="0 0 24 24"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M4 6h16M4 12h16M4 18h16"
          />
        </svg>

        <!-- Icon: X (shown when open) -->
        <svg
          v-else
          class="w-7 h-7"
          fill="none"
          stroke="currentColor"
          viewBox="0 0 24 24"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M6 18L18 6M6 6l12 12"
          />
        </svg>
      </button>
    </div>

    <!-- Mobile Dropdown Menu -->
    <div
      v-show="isOpen"
      class="md:hidden pt-4 pb-2 flex flex-col space-y-3 text-lg"
    >
      <a
        v-for="link in links"
        :key="link.name"
        :href="link.href"
        class="text-white hover:text-blue-600 py-1 transition-colors"
        @click="isOpen = false"
      >
        {{ link.name }}
      </a>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue'

const links = [
  { name: 'ABOUT', href: '#about' },
  { name: 'FRONTEND', href: '#frontend' },
  { name: 'UX/UI', href: '#ux-ui' },
  { name: 'OTHER', href: '#other' }
]

const isOpen = ref(false)
const toggleMenu = () => {
  isOpen.value = !isOpen.value
}
</script>