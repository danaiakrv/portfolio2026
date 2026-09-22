<template>
  <nav
      class="px-[clamp(1.5rem,8vw,20rem)] fixed top-0 left-0 w-full z-50 transition-all duration-300"
      :class="(isScrolled || isOpen) ? 'bg-violet-400 py-5 shadow-md' : 'py-5'"
    >
    <div class="flex items-center justify-between">
      <a href="#" class="text-2xl font-bold text-white !no-underline">Danai Akrivou</a>

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

      <button
        type="button"
        class="md:hidden text-white focus:outline-none p-2 rounded hover:bg-violet-500 transition-colors"
        aria-label="Toggle Navigation Menu"
        :aria-expanded="isOpen"
        @click="toggleMenu"
      >
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
import { ref, onMounted, onUnmounted } from 'vue'

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

const isScrolled = ref(false)

const handleScroll = () => {
  const isDesktop = window.innerWidth >= 1024
  const threshold = isDesktop ? 350 : 20
  isScrolled.value = window.scrollY > threshold
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>