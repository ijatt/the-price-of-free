<template>
  <div class="bg-cream min-h-screen text-black font-sans">
    <!-- Header / Nav -->
    <header
      class="sticky top-0 z-50 bg-cream/95 backdrop-blur border-b border-purple-200"
    >
      <div
        class="max-w-6xl mx-auto px-4 sm:px-6 py-3 flex items-center justify-between"
      >
        <div class="flex items-center gap-3">
          <div
            class="w-10 h-10 rounded-full bg-purple flex items-center justify-center text-white font-bold"
          >
            S
          </div>
          <div class="text-lg font-bold text-purple">The Price of Free</div>
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
          <a href="#privacy" class="hover:text-purple-600 transition">Privacy</a>
          <a href="#game" class="hover:text-purple-600 transition">Game</a>
          <a href="#pledge" class="hover:text-purple-600 transition">Pledge</a>
          <a href="#contact" class="hover:text-purple-600 transition">Contact</a>
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
          <a href="#privacy" @click="closeMobile" class="py-2">Privacy</a>
          <a href="#game" @click="closeMobile" class="py-2">Game</a>
          <a href="#pledge" @click="closeMobile" class="py-2">Pledge</a>
          <a href="#contact" @click="closeMobile" class="py-2">Contact</a>
        </div>
      </div>
    </header>

    <main class="max-w-6xl mx-auto px-4 sm:px-6">
      <!-- HERO SECTION -->
      <section id="home" class="py-16">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-10 items-center">
          <div>
            <h1 class="text-5xl font-extrabold text-purple">
              The Price of Free:
            </h1>
            <h2 class="text-3xl md:text-4xl font-bold mt-2">
              How Much Is Your Data Worth?
            </h2>

            <p class="mt-5 text-gray-700 text-lg italic">
              In the age of Artificial Intelligence, your data is your identity.
            </p>

            <p class="mt-6 text-gray-700 max-w-xl">
              Every online action teaches AI something about you. This website
              uncovers how data powers AI systems and how your digital choices
              shape the algorithms around you.
            </p>

            <p class="mt-6 text-gray-700 max-w-xl">
              Learn what data AI uses, why it matters, and how small choices
              shape the systems around us. Play the interactive "Would You Trade
              It?" experience and reflect on your digital footprint.
            </p>
            <div class="mt-8 flex gap-4 flex-wrap">
              <a
                href="#game"
                class="bg-purple text-white px-6 py-3 rounded-full font-semibold hover:bg-purple-700"
              >
                Play Interactive Game
              </a>
              <a
                href="#pledge"
                class="border border-purple text-purple px-6 py-3 rounded-full hover:bg-purple-light hover:text-white font-semibold"
              >
                Make a Pledge
              </a>
            </div>
          </div>
          <!-- bg nak warna apa do -->
          <div class="flex justify-center">
            <div
              class="bg-white rounded-3xl shadow p-6 h-64 w-full flex flex-col items-center justify-center"
            >
              <p class="text-gray-500 text-center">
                (Insert your infographic or booth image here)
              </p>
            </div>
          </div>
        </div>
      </section>
      <section class="py-10" id="color-palette">
        <!-- 
        generate based this
        --color-cream: #fffaeb;
  
        -->
        <h3 class="text-2xl font-bold text-teal-700">Color Palette</h3>
        <div class="mt-4 flex gap-4">
          <div
            class="w-16 h-16 bg-cyan rounded-lg shadow flex items-center justify-center text-gray-700 font-semibold"
          >
            CYAN
          </div>
          <div
            class="w-16 h-16 bg-pink rounded-lg shadow flex items-center justify-center text-white font-semibold"
          >
            PINK
          </div>
          <div
            class="w-16 h-16 bg-cyan-light rounded-lg shadow flex items-center justify-center text-gray-700 font-semibold"
          >
            CYAN-LIGHT
          </div>
          <div
            class="w-16 h-16 bg-pink-light rounded-lg shadow flex items-center justify-center text-white font-semibold"
          >
            PINK-LIGHT
          </div>
          <div
            class="w-16 h-16 bg-purple-light rounded-lg shadow flex items-center justify-center text-white font-semibold"
          >
            PURPLE-LIGHT
          </div>
          <div
            class="w-16 h-16 bg-purple rounded-lg shadow flex items-center justify-center text-white font-semibold"
          >
            PURPLE
          </div>
          <div
            class="w-16 h-16 bg-bg-dark rounded-lg shadow flex items-center justify-center text-white font-semibold"
          >
            BG-DARK
          </div>
          <div
            class="w-16 h-16 bg-bg-purple rounded-lg shadow flex items-center justify-center text-white font-semibold"
          >
            BG-PURPLE
          </div>
        </div>
      </section>
      <!-- What is AI -->
      <section id="what-is-ai" class="py-10">
        <h3 class="text-3xl font-bold text-purple">
          What is Artificial Intelligence?
        </h3>
        <p class="mt-4 text-gray-700 max-w-3xl">
          Artificial Intelligence (AI) are systems that perform tasks that
          normally require human intelligence such as recognising images,
          translating language, or recommending content. Many AI systems are
          trained using data created by people: photos, clicks, text and
          location.
        </p>

        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 mt-8">
          <div class="bg-white p-5 rounded-2xl shadow">
            <h4 class="font-semibold text-purple">Machine Learning</h4>
            <p class="mt-2 text-gray-600">
              Models learn patterns from many examples (data).
            </p>
          </div>
          <div class="bg-white p-5 rounded-2xl shadow">
            <h4 class="font-semibold text-purple">Computer Vision</h4>
            <p class="mt-2 text-gray-600">
              AI that understands images and video.
            </p>
          </div>
          <div class="bg-white p-5 rounded-2xl shadow">
            <h4 class="font-semibold text-purple">
              Natural Language Processing
            </h4>
            <p class="mt-2 text-gray-600">
              AI systems that understand or generate text and speech.
            </p>
          </div>
        </div>
      </section>

      <!-- AI & Data -->
      <section id="ai-data" class="py-10 bg-white rounded-3xl p-6 shadow">
        <h3 class="text-2xl font-bold text-purple-700">AI & Your Data</h3>
        <p class="mt-4 text-gray-700">
          Everyday actions — likes, search queries, photos — are signals used to
          train models. Sometimes that data reveals sensitive patterns, and
          often it is collected without us fully realising the consequences.
        </p>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mt-6">
          <div class="p-4 border rounded-lg">
            <h4 class="font-semibold">What is collected?</h4>
            <ul class="mt-2 text-gray-600 list-disc list-inside">
              <li>Device & location data</li>
              <li>Search & browsing history</li>
              <li>Photos and uploaded files</li>
            </ul>
          </div>

          <div class="p-4 border rounded-lg">
            <h4 class="font-semibold">Why it matters</h4>
            <p class="mt-2 text-gray-600">
              Collected data shapes model predictions, recommendations, and even
              decisions that affect people.
            </p>
          </div>
        </div>
      </section>

      <!-- Privacy -->
      <section id="privacy" class="py-10">
        <h3 class="text-2xl font-bold text-purple-700">Privacy & Safety</h3>
        <p class="mt-4 text-gray-700 max-w-3xl">
          Simple actions can improve privacy: review app permissions, use
          stronger passwords, and think before sharing.
        </p>

        <div class="mt-6 flex gap-4 flex-col sm:flex-row">
          <div class="flex-1 bg-purple-600 text-white p-5 rounded-2xl">
            <h4 class="font-semibold">Quick tips</h4>
            <ul class="mt-3 text-sm">
              <li>Check permissions for photos & location</li>
              <li>Limit public profile information</li>
              <li>Use two-factor authentication</li>
            </ul>
          </div>

          <div class="flex-1 bg-white p-5 rounded-2xl shadow">
            <h4 class="font-semibold text-purple-600">For teachers & parents</h4>
            <p class="mt-2 text-gray-600">
              Discuss with young users what data apps ask for and why. Encourage
              critical questions about free services.
            </p>
          </div>
        </div>
      </section>

      <!-- Game (Genially embed) -->
      <section id="game" class="py-10">
        <h3 class="text-2xl font-bold text-purple-700">
          Interactive Game — "Would You Trade It?"
        </h3>
        <p class="mt-2 text-gray-700 max-w-2xl">
          Play the Genially interactive experience created by your teammates.
          The iframe below is responsive for mobile and desktop.
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

      <!-- Reflection / Pledge -->
      <section id="pledge" class="py-10 bg-white rounded-3xl p-6 shadow">
        <h3 class="text-2xl font-bold text-purple-700">Reflection & Pledge</h3>
        <p class="mt-2 text-gray-700">
          After playing, write one short action you will take to protect your
          data.
        </p>

        <form @submit.prevent="submitPledge" class="mt-4 max-w-2xl">
          <label class="block text-sm font-medium text-gray-700"
            >Your name (optional)</label
          >
          <input
            v-model="pledge.name"
            type="text"
            class="mt-1 w-full p-3 rounded-lg border"
            placeholder="e.g. Aisyah"
          />

          <label class="block text-sm font-medium text-gray-700 mt-4"
            >Your pledge</label
          >
          <textarea
            v-model="pledge.text"
            rows="4"
            required
            class="mt-1 w-full p-3 rounded-lg border"
            placeholder="I will review app permissions..."
          ></textarea>

          <div class="flex items-center gap-3 mt-4">
            <input
              v-model="pledge.share"
              id="share"
              type="checkbox"
              class="w-4 h-4"
            />
            <label for="share" class="text-sm text-gray-700"
              >Share my pledge anonymously on the site</label
            >
          </div>

          <div class="mt-4 flex gap-3">
            <button
              type="submit"
              class="bg-purple-600 text-white px-5 py-2 rounded-lg hover:bg-purple-700 transition"
            >
              Submit Pledge
            </button>
            <button
              type="button"
              @click="clearPledge"
              class="border px-4 py-2 rounded-lg"
            >
              Clear
            </button>
          </div>

          <p v-if="pledgeStatus" class="mt-3 text-sm text-green-600">
            {{ pledgeStatus }}
          </p>
        </form>

        <!-- Display last few pledges (local only) -->
        <div v-if="pledges.length" class="mt-8">
          <h4 class="font-semibold text-purple-700">Recent pledges</h4>
          <ul class="mt-3 space-y-3">
            <li
              v-for="(p, i) in latestPledges"
              :key="i"
              class="bg-gray-50 p-3 rounded-lg border"
            >
              <p class="text-sm text-gray-700">
                <strong v-if="p.name">{{ p.name }}</strong
                ><span v-else>Anonymous</span> —
                <span class="text-gray-500 text-xs">{{ p.when }}</span>
              </p>
              <p class="mt-1 text-gray-800">{{ p.text }}</p>
            </li>
          </ul>
        </div>
      </section>

      <section id="gallery" class="py-10">
        <h3 class="text-2xl font-bold text-purple-700">Awareness Poster</h3>
        <p class="mt-2 text-gray-700"></p>

        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 mt-6">
          <img src="assets/img/p1.png" alt="Awareness Poster 1" />
          <img src="assets/img/p2.png" alt="Awareness Poster 2" />
          <img src="assets/img/p3.png" alt="Awareness Poster 3" />
        </div>
      </section>

      <!-- Contact -->
      <section id="contact" class="py-10 bg-black text-white rounded-3xl p-6">
        <div class="md:flex md:items-center md:justify-between">
          <div>
            <h3 class="text-2xl font-bold">Contact & Credits</h3>
            <p class="mt-2 text-gray-300">
              SULAM project — Team members: Alya Natasha, [others]. For
              questions:
              <a class="underline" href="mailto:youremail@example.com"
                >youremail@example.com</a
              >
            </p>
          </div>

          <div class="mt-4 md:mt-0">
            <p class="text-sm text-gray-300">
              Copyright © {{ new Date().getFullYear() }} SULAM
            </p>
          </div>
        </div>
      </section>
    </main>
  </div>
</template>

<script lang="ts" setup>
definePageMeta({
  title: "The Price of Free: How Much Is Your Data Worth?",
  meta: [
    {
      name: "description",
      content:
        "Learn how everyday data trains AI — an interactive learning experience with a game and pledge.",
    },
    { name: "viewport", content: "width=device-width, initial-scale=1" },
  ],
});
import { ref, reactive, computed } from "vue";

/* Mobile menu */
const mobileOpen = ref(false);
function closeMobile() {
  mobileOpen.value = false;
}

/* Pledge form (local-only demo). If you want server saving, replace submitPledge with API/Firebase call. */
const pledge = reactive<{ name: string; text: string; share: boolean }>({
  name: "",
  text: "",
  share: true,
});
const pledgeStatus = ref("");
const pledges = ref<Array<{ name?: string; text: string; when: string }>>([]);

/* Save pledges to localStorage so they persist across reloads */
const loadPledges = () => {
  try {
    const raw = localStorage.getItem("sulam_pledges");
    if (raw) pledges.value = JSON.parse(raw);
  } catch (e) {
    /* ignore */
  }
};
const savePledges = () => {
  try {
    localStorage.setItem("sulam_pledges", JSON.stringify(pledges.value));
  } catch (e) {
    /* ignore */
  }
};
loadPledges();

function submitPledge() {
  if (!pledge.text.trim()) {
    pledgeStatus.value = "Please write a short pledge before submitting.";
    setTimeout(() => (pledgeStatus.value = ""), 3000);
    return;
  }
  const record = {
    name: pledge.name ? pledge.name.trim() : undefined,
    text: pledge.text.trim(),
    when: new Date().toLocaleString(),
  };
  if (pledge.share) pledges.value.unshift(record);
  pledgeStatus.value = "Thanks — your pledge is saved locally!";
  savePledges();
  // clear form
  pledge.name = "";
  pledge.text = "";
  setTimeout(() => (pledgeStatus.value = ""), 3500);
}

function clearPledge() {
  pledge.name = "";
  pledge.text = "";
  pledge.share = true;
}

/* computed for displaying recent (limit 5) */
const latestPledges = computed(() => pledges.value.slice(0, 5));
</script>

<style scoped>
.bg-cream {
  background-color: #faf7f2;
}

/* small polish for anchors smooth scrolling */
html {
  scroll-behavior: smooth;
}

/* ensure iframe border looks subtle on dark mode etc. */
iframe {
  border: 1px solid rgba(15, 23, 42, 0.06);
}
</style>
