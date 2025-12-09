<template>
  <section id="about-uss" class="py-16 bg-cream text-black font-merri">
    <h3 class="text-3xl font-extrabold text-center text-purple-700 mb-10">
      About Us
    </h3>

    <UCarousel
      v-slot="{ item }"
      loop
      arrows
      dots
      :autoplay="{ delay: 3000 }"
      :items="team"
      :ui="{ item: 'basis-2/4 md:basis-1/4 lg:basis-1/4' }"
      class="max-w-7xl mx-auto px-6"
    >
      <!-- <div
        :class="['team-card rounded-lg p-4 flex flex-col items-center', item.gradient]"
      > -->
      <div
        :class="[
          'px-4 py-4 rounded-3xl flex flex-col items-center gap-y-4',
          item.gradient,
        ]"
      >
        <img
          :src="item.img"
          class="team-img w-40 h-40 rounded-3xl object-cover mb-4 hover:scale-105 transition-transform duration-300"
          :alt="item.name"
        />

        <h4 class="font-bold text-white text-lg">{{ item.name }}</h4>
        <p class="text-sm text-gray mt-1">{{ item.role }}</p>
      </div>
    </UCarousel>
  </section>
</template>

<script lang="ts" setup>
import aiImg from "@/assets/img/ai.png";

interface TeamMember {
  name: string;
  role: string;
  img: string;
  gradient: string;
}

const team: TeamMember[] = [
  {
    name: "Siti Najihah",
    role: "Group Leader",
    img: aiImg,
    gradient: "card-gradient-1",
  },
  {
    name: "Shahrizat",
    role: "Leader - Web Developer",
    img: "/assets/img/ai.jpg",
    gradient: "card-gradient-2",
  },
  {
    name: "Alya Natasha",
    role: "Web Developer",
    img: "/assets/img/ai.jpg",
    gradient: "card-gradient-3",
  },
  {
    name: "Sharifah",
    role: "Web Developer",
    img: "/assets/img/ai.jpg",
    gradient: "card-gradient-4",
  },
  {
    name: "Athul",
    role: "UI/UX Designer",
    img: "https://media.pitchfork.com/photos/67932557f4bbbe1b47e33b2e/2:1/w_1920,c_limit/Travis-Scott.jpg",
    gradient: "card-gradient-5",
  },
  {
    name: "Asha Alia",
    role: "Web Developers",
    img: "https://media.pitchfork.com/photos/67932557f4bbbe1b47e33b2e/2:1/w_1920,c_limit/Travis-Scott.jpg",
    gradient: "card-gradient-1",
  },
  {
    name: "Ilman",
    role: "Leader - Game Developer",
    img: "https://media.pitchfork.com/photos/67932557f4bbbe1b47e33b2e/2:1/w_1920,c_limit/Travis-Scott.jpg",
    gradient: "card-gradient-2",
  },
  {
    name: "Syazwani",
    role: "Game Developer",
    img: "https://media.pitchfork.com/photos/67932557f4bbbe1b47e33b2e/2:1/w_1920,c_limit/Travis-Scott.jpg",
    gradient: "card-gradient-3",
  },
  {
    name: "Yazid",
    role: "Game Developer",
    img: "https://media.pitchfork.com/photos/67932557f4bbbe1b47e33b2e/2:1/w_1920,c_limit/Travis-Scott.jpg",
    gradient: "card-gradient-4",
  },
  {
    name: "Dharsini",
    role: "Game Developer",
    img: "https://media.pitchfork.com/photos/67932557f4bbbe1b47e33b2e/2:1/w_1920,c_limit/Travis-Scott.jpg",
    gradient: "card-gradient-5",
  },
  {
    name: "Fahmi",
    role: "Game Developer",
    img: "https://media.pitchfork.com/photos/67932557f4bbbe1b47e33b2e/2:1/w_1920,c_limit/Travis-Scott.jpg",
    gradient: "card-gradient-1",
  },
];
</script>

<style>
  .card-gradient-1 {
  background: linear-gradient(135deg, #a855f7 0%, #ec4899 100%);
}

.card-gradient-2 {
  background: linear-gradient(135deg, #3b82f6 0%, #8b5cf6 100%);
}

.card-gradient-3 {
  background: linear-gradient(135deg, #06b6d4 0%, #14b8a6 100%);
}

.card-gradient-4 {
  background: linear-gradient(135deg, #f43f5e 0%, #f97316 100%);
}

.card-gradient-5 {
  background: linear-gradient(135deg, #6366f1 0%, #a855f7 100%);
}
</style>
