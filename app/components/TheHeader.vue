<template>
  <header
    class="sticky top-0 z-50 bg-cream/95 backdrop-blur border-b border-purple-200"
  >
    <div
      class="max-w-6xl mx-auto px-4 sm:px-6 py-3 flex items-center justify-between"
    >
      <div class="flex items-center gap-3">
        <div class="w-10 h-10 rounded-full overflow-hidden">
          <img
            src="assets/img/logo.png"
            alt="Logo"
            class="w-full h-full object-cover"
          />
        </div>

        <div class="text-lg font-bold text-purple">
          Artificial Intelligence: Price of Free
        </div>
      </div>

      <!-- Desktop links -->
      <nav class="hidden md:flex gap-6 text-sm font-medium items-center">
        <a href="#home" class="hover:text-purple-600 transition">Home</a>
        <a href="#what-is-ai" class="hover:text-purple-600 transition"
          >What is AI</a
        >
        <a href="#ai-data" class="hover:text-purple-600 transition"
          >AI & Data</a
        >
        <a href="#fairness" @click="closeMobile" class="py-2"
          >Fairness & Bias</a
        >
        <a href="#privacy" class="hover:text-purple-600 transition">Privacy</a>
        <a href="#game" class="hover:text-purple-600 transition">Game</a>
      </nav>
      <button
        @click="mobileOpen = !mobileOpen"
        :aria-expanded="mobileOpen"
        aria-controls="mobile-menu"
        class="md:hidden p-2 rounded hover:bg-cream/60"
      >
        <svg
          v-if="!mobileOpen"
          class="w-6 h-6 text-purple-700"
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
          class="w-6 h-6 text-purple-700"
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

    <!-- Mobile dropdown -->
    <div
      v-if="mobileOpen"
      id="mobile-menu"
      class="md:hidden bg-cream border-t border-purple-100"
    >
      <div class="px-4 py-4 flex flex-col gap-3">
        <a href="#home" @click="closeMobile" class="py-2">Home</a>
        <a href="#what-is-ai" @click="closeMobile" class="py-2">What is AI</a>
        <a href="#ai-data" @click="closeMobile" class="py-2">AI & Data</a>
        <a href="#fairness" @click="closeMobile" class="py-2"
          >Fairness & Bias</a
        >
        <a href="#privacy" @click="closeMobile" class="py-2">Privacy</a>
        <a href="#game" @click="closeMobile" class="py-2">Game</a>
      </div>
    </div>
  </header>
</template>

<script lang="ts" setup>
const mobileOpen = ref(false);
function closeMobile() {
  mobileOpen.value = false;
}
</script>

<style></style>
