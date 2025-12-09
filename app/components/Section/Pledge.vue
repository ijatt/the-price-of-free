<template>
  <section id="pledge" class="py-10 bg-white rounded-3xl p-6 shadow">
    <h3 class="text-2xl font-bold text-purple-700">Reflection & Pledge</h3>
    <p class="mt-2 text-gray-700">
      After playing, write one short action you will take to protect your data.
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
          :disabled="isSubmitting"
          class="bg-purple-600 text-white px-5 py-2 rounded-lg hover:bg-purple-700 transition disabled:opacity-50 disabled:cursor-not-allowed"
        >
          {{ isSubmitting ? "Submitting..." : "Submit Pledge" }}
        </button>
        <button
          type="button"
          @click="clearPledge"
          :disabled="isSubmitting"
          class="border px-4 py-2 rounded-lg disabled:opacity-50 disabled:cursor-not-allowed"
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
</template>

<script lang="ts" setup>
const pledge = reactive<{ name: string; text: string; share: boolean }>({
  name: "",
  text: "",
  share: true,
});
const pledgeStatus = ref("");
const pledges = ref<
  Array<{ id: string; name?: string | null; text: string; createdAt: string }>
>([]);
const isSubmitting = ref(false);

/* Load pledges from server */
const loadPledges = async () => {
  try {
    const response = await $fetch("/api/pledges");
    if (response.success && response.data) {
      pledges.value = response.data;
    }
  } catch (e) {
    console.error("Error loading pledges:", e);
  }
};

async function submitPledge() {
  if (!pledge.text.trim()) {
    pledgeStatus.value = "Please write a short pledge before submitting.";
    setTimeout(() => (pledgeStatus.value = ""), 3000);
    return;
  }

  if (isSubmitting.value) return;
  
  isSubmitting.value = true;
  pledgeStatus.value = "";

  try {
    const response = await $fetch("/api/pledges/", {
      method: "POST",
      body: {
        name: pledge.name ? pledge.name.trim() : null,
        text: pledge.text.trim(),
      },
    });

    if (response.success) {
      pledgeStatus.value = "Thanks — your pledge has been saved!";
      // Reload pledges to show the new one
      if (pledge.share) {
        await loadPledges();
      }
      // Clear form
      pledge.name = "";
      pledge.text = "";
      setTimeout(() => (pledgeStatus.value = ""), 3500);
    }
  } catch (error: any) {
    console.error("Error submitting pledge:", error);
    pledgeStatus.value = error.data?.statusMessage || "Failed to save pledge. Please try again.";
    setTimeout(() => (pledgeStatus.value = ""), 3500);
  } finally {
    isSubmitting.value = false;
  }
}

function clearPledge() {
  pledge.name = "";
  pledge.text = "";
  pledge.share = true;
}

/* computed for displaying recent (limit 5) */
const latestPledges = computed(() => pledges.value.slice(0, 5).map(p => ({
  name: p.name || undefined,
  text: p.text,
  when: new Date(p.createdAt).toLocaleString(),
})));

onMounted(() => {
  loadPledges();
});
</script>

<style></style>
