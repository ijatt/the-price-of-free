<template>
  <div class="bg-cream min-h-screen text-black font-sans">
    <!-- Navigation -->
    <nav
      class="sticky top-0 z-50 bg-cream/95 backdrop-blur border-b border-teal-200"
    >
      <div
        class="max-w-6xl mx-auto px-4 sm:px-6 py-4 flex items-center justify-between"
      >
        <div class="text-2xl font-bold text-teal-700">AI</div>
        <div class="hidden md:flex gap-8 text-sm font-medium">
          <a href="#home" class="hover:text-teal-600 transition">Home</a>
          <a href="#what-is-ai" class="hover:text-teal-600 transition"
            >What is AI</a
          >
          <a href="#applications" class="hover:text-teal-600 transition"
            >Applications</a
          >
          <a href="#future" class="hover:text-teal-600 transition">Future</a>
          <a href="#contact" class="hover:text-teal-600 transition">Contact</a>
        </div>
        <button class="md:hidden text-teal-700">
          <svg
            class="w-6 h-6"
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
        </button>
      </div>
    </nav>

    <!-- Hero Section -->
    <section
      id="home"
      class="min-h-screen flex items-center justify-center px-8 py-20"
    >
      <div class="max-w-4xl mx-auto text-center space-y-8">
        <div class="space-y-4">
          <h1 class="text-xl text-teal-600 font-bold">
            RISUS PRAESENT VULPUTATE
          </h1>
          <h1 class="text-5xl sm:text-6xl md:text-7xl font-bold leading-tight">
            Artificial Intelligence
          </h1>
        </div>
        <div class="flex items-center flex-col gap-4">
          <div class="bg-white rounded-full flex gap-2 items-center py-2 px-4">
            <Icon name="mdi-check-circle" class="text-teal-600" />
            <p>Cursus Integer</p>
          </div>
          <div class="bg-white rounded-full flex gap-2 items-center py-2 px-4">
            <Icon name="mdi-check-circle" class="text-teal-600" />
            <p>Integer Consequat</p>
          </div>
          <div class="bg-white rounded-full flex gap-2 items-center py-2 px-4">
            <Icon name="mdi-check-circle" class="text-teal-600" />
            <p>Tellus Euismod Pellentesque</p>
          </div>
          <div class="bg-white rounded-full flex gap-2 items-center py-2 px-4">
            <Icon name="mdi-check-circle" class="text-teal-600" />
            <p>Aliquot Tristique</p>
          </div>
          <div class="bg-white rounded-full flex gap-2 items-center py-2 px-4">
            <Icon name="mdi-check-circle" class="text-teal-600" />
            <p>Pellentesque Tempus</p>
          </div>
          <div class="bg-white rounded-full flex gap-2 items-center py-2 px-4">
            <Icon name="mdi-check-circle" class="text-teal-600" />
            <p>Mauris Fermentum Praesent</p>
          </div>
        </div>
        <div class="pt-12">
          <div
            class="w-full sm:h-80 bg-teal-500 rounded-full py-4 px-8 flex items-center justify-between"
          >
            <p class="font-bold">Lorem Ipsum</p>
            <Icon name="mdi-arrow-right" />
          </div>
        </div>
        <div class="pt-2">
          <div class="w-full bg-teal-600 rounded-3xl p-8">
            <SvgoIcon name="icon-1" />
            <h1 class="text-4xl font-bold">
              Phasellus a vitae iaculis magna eleifend pulvinar velit odio.
            </h1>
            <p class="underline pt-8">
              Vulputate et vulputate <br />
              suspendisse natouqe!
            </p>
            <p class="pt-8">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed
              euismod, nunc ut.
            </p>
            <div
              class="w-full sm:h-80 text-white bg-black rounded-full py-4 px-8 flex items-center justify-between mt-8"
            >
              <p class="font-bold text-white tracking-wider">Lorem Ipsum</p>
              <Icon name="mdi-arrow-right" />
            </div>
          </div>
        </div>
        <div class="mt-2 bg-black rounded-3xl py-8 px-10">
          <p class="text-teal-500 text-center tracking-wider text-sm">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed
            euismod, nunc ut.
          </p>
          <h1 class="mt-8 text-white text-3xl font-bold tracking-wider">
            Cursus Integer Conseq Aliquam Tristique
          </h1>
          <div
            class="w-full sm:h-80 bg-white mt-8 rounded-full py-4 px-8 flex items-center justify-between"
          >
            <p class="font-bold">Lorem Ipsum</p>
            <Icon name="mdi-arrow-right" />
          </div>
          <div class="bg-white mt-8 p-8 rounded-4xl">
            <SvgoIcon name="icon-2" />
            <p class="text-5xl font-bold text-start mt-4">
              1 <span class="text-teal-500">.</span>
            </p>
            <p class="text-lg font-bold text-start mt-4">Phasellus Vitae</p>
            <p class="font-semibold text-start mt-4">Quisque</p>
            <p class="text-start font-light">Porttitor Vitae Vel Amet</p>
          </div>
          <div class="bg-teal-600 mt-8 p-8 rounded-4xl">
            <SvgoIcon name="icon-3" />
            <p class="text-5xl font-bold text-start mt-4">
              2 <span class="text-white">.</span>
            </p>
            <p class="text-lg font-bold text-start mt-4">Iaculis Magna</p>
            <p class="font-semibold text-start mt-4">Porttitor</p>
            <p class="text-start font-light">Neque Scelerisque Mattis</p>
          </div>
          <div class="bg-white mt-8 p-8 rounded-4xl">
            <SvgoIcon name="icon-4" />
            <p class="text-5xl font-bold text-start mt-4">
              3 <span class="text-teal-500">.</span>
            </p>
            <p class="text-lg font-bold text-start mt-4">Eleifend Pulvinar</p>
            <p class="font-semibold text-start mt-4">Vitae</p>
            <p class="text-start font-light">Consectetur Nibh Velit</p>
          </div>
          <div class="bg-teal-600 mt-8 p-8 rounded-4xl">
            <SvgoIcon name="icon-5" />
            <p class="text-5xl font-bold text-start mt-4">
              4 <span class="text-white">.</span>
            </p>
            <p class="text-lg font-bold text-start mt-4">Velit Odio Phir</p>
            <p class="font-semibold text-start mt-4">Ametneq</p>
            <p class="text-start font-light">Magna Consectetur Leo.</p>
          </div>
        </div>
        <div class="mt-2 bg-white rounded-4xl p-8">
          <img class="w-40 h-40 rounded-full mx-auto" src="" alt="" />
          <p class="text-3xl mt-8 font-bold tracking-wider">
            What our <br />
            customers thought?
          </p>
          <p class="font-light mt-8">
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Adipisci
            corrupti, itaque nihil voluptatem eius modi necessitatibus voluptate
            vero quibusdam qui quo ut quas quis a impedit, praesentium dicta
            repellat laboriosam.
          </p>
          <p class="text-2xl mt-8 font-bold tracking-wider">Holly Davidson</p>
          <div
            class="flex w-full items-center gap-10 mx-auto mt-8 justify-center"
          >
            <button class>
              <Icon
                name="mdi-arrow-left"
                class="w-8 h-8 text-gray-400 hover:text-teal-600"
              />
            </button>
            <button class>
              <Icon
                name="mdi-arrow-right"
                class="w-8 h-8 text-gray-400 hover:text-teal-600"
              />
            </button>
          </div>
        </div>
        <div class="mt-2 bg-white rounded-4xl p-8">
          <SvgoIcon name="hero-2" />
          <h1 class="text-4xl font-bold">
            Cursus Integer <br />
            consequat <br />
            Tristique.
          </h1>
          <div class="flex items-center flex-col gap-4 mt-8">
            <div
              class="bg-cream rounded-full flex gap-2 items-center py-2 px-4"
            >
              <Icon name="mdi-check-circle" class="text-teal-600" />
              <p>Cursus Integer</p>
            </div>
            <div
              class="bg-cream rounded-full flex gap-2 items-center py-2 px-4"
            >
              <Icon name="mdi-check-circle" class="text-teal-600" />
              <p>Integer Consequat</p>
            </div>
            <div
              class="bg-cream rounded-full flex gap-2 items-center py-2 px-4"
            >
              <Icon name="mdi-check-circle" class="text-teal-600" />
              <p>Tellus Euismod Pellentesque</p>
            </div>
            <div
              class="bg-cream rounded-full flex gap-2 items-center py-2 px-4"
            >
              <Icon name="mdi-check-circle" class="text-teal-600" />
              <p>Aliquot Tristique</p>
            </div>
            <div
              class="bg-cream rounded-full flex gap-2 items-center py-2 px-4"
            >
              <Icon name="mdi-check-circle" class="text-teal-600" />
              <p>Pellentesque Tempus</p>
            </div>
            <div
              class="bg-cream rounded-full flex gap-2 items-center py-2 px-4"
            >
              <Icon name="mdi-check-circle" class="text-teal-600" />
              <p>Mauris Fermentum Praesent</p>
            </div>
            <div
              class="w-full sm:h-80 text-white bg-black rounded-full py-4 px-8 flex items-center justify-between mt-8"
            >
              <p class="font-bold text-white tracking-wider">Lorem Ipsum</p>
              <Icon name="mdi-arrow-right" />
            </div>
          </div>
        </div>
        <div class="mt-8">
          <h1 class="text-4xl font-bold">
            Phasellus a vitae <br />
            iaculis magna.
          </h1>
          <p class="font-light mt-8">
            Phasellus a vitae iaculis magna eleifend pulvinar velit odio.
          </p>
        </div>
        <div class="mt-8 bg-white rounded-4xl p-6">
          <div class="flex w-full items-center justify-between">
            <div class="">
              <p class="font-bold text-lg text-start">
                Quam vehicula faucbius amet lorem.
              </p>
            </div>
            <div class="">
              <button @click="show = !show">
                <span v-if="!show" class="text-teal-600 font-bold text-3xl">
                  +
                </span>
                <span v-else class="text-teal-600 font-bold text-3xl"> − </span>
              </button>
            </div>
          </div>
          <div class="mt-8 w-4/5" v-if="show">
            <p class="font-light text-start">
              Euismod Magna Id Purus Eget Nunc Ligula Suspendisse Dui Netus.
              Condimentum Blandit Retrum At Mauris Enim Pulvinar Duis Etiam
              Duis. Mauris Fermentum Praesent Tellus Euismod.
            </p>
          </div>
        </div>
        <div class="mt-8 rounded-4xl bg-black p-8">
          <h1 class="text-2xl tracking-wider text-white font-bold">
            Vulputate et <br />
            pulvinar ethre <br />
            Suspendisse tellus <br />
            consecteur
          </h1>
          <div class="pt-12">
            <div
              class="w-full sm:h-80 bg-teal-500 rounded-full py-4 px-8 flex items-center justify-between"
            >
              <p class="font-bold">Lorem Ipsum</p>
              <Icon name="mdi-arrow-right" />
            </div>
          </div>
          <hr class="text-white mt-8" />
          <div class="mt-8">
            <p class="text-white">
              Copyright © 2024 Your Company. All rights reserved.
            </p>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script lang="ts" setup>
const show = ref(false);
</script>

<style scoped></style>
