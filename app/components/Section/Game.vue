<template>
  <section id="game" class="py-10">
    <h3 class="text-2xl font-bold text-purple-700">
      Interactive Game — Would You Trade It?
    </h3>
    <p class="mt-2 text-gray-700 max-w-2xl">
      Jump in and play the game to experience it yourself! See what choices you
      would make and discover the fun interactive journey your teammates
      created.
    </p>

    <!-- Responsive iframe wrapper -->
    <div class="mt-6 max-w-4xl mx-auto">
      <div class="relative" style="padding-top: 56.25%">
        <!-- 16:9 -->
        <iframe
          title="Would You Trade It? - Genially"
          src="https://view.genially.com/6914be1c26254ceb89c1d30d/interactive-content-would-you-trade-it"
          class="absolute top-0 left-0 w-full h-full rounded-xl border"
          frameborder="0"
          allowfullscreen
          loading="lazy"
        ></iframe>
      </div>

      <p class="text-sm text-gray-500 mt-2">
        If the game doesn't load on mobile, open it in a new tab.
      </p>
    </div>
  </section>
</template>

<script lang="ts" setup></script>

<style>
iframe {
  border: 1px solid rgba(15, 23, 42, 0.06);
}
</style>
