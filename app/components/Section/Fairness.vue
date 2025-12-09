<template>
  <section id="fairness" class="py-12">
    <div class="text-center mb-10">
      <h3 class="text-3xl font-bold text-purple">Fairness & Bias</h3>
      <p class="mt-4 text-gray-700 max-w-3xl mx-auto">
        AI bias happens when an AI system gives unfair results because of the
        data it was trained on. If data is incomplete, stereotypical or
        unbalanced, the AI will make unfair decisions.
      </p>
    </div>

    <div class="max-w-6xl mx-auto px-4">
      <div class="relative rounded-3xl overflow-hidden">
        <!-- gradient background -->
        <div
          class="absolute inset-0 bg-gradient-to-r from-purple-900 via-teal-700 to-indigo-700 pointer-events-none"
        ></div>

        <div
          class="relative z-10 grid grid-cols-1 lg:grid-cols-2 gap-8 items-center p-8 lg:p-12 text-white"
        >
          <!-- Left: Text content like Fairness & Bias style -->
          <div class="space-y-6">
            <div class="bg-white/6 p-5 rounded-xl">
              <div class="text-2xl font-bold mt-1">Why Bias Happens?</div>
              <ul class="list-disc ml-6 text-sm mt-2 space-y-1">
                <li>
                  Biased training data: If AI sees more of one group than others
                </li>
                <li>
                  Human bias: Developers or users unintentionally include
                  assumptions
                </li>
                <li>Algorithm design: AI sometimes misinterprets patterns</li>
              </ul>
            </div>

            <div class="bg-white/6 p-5 rounded-xl">
              <div class="text-2xl font-bold mt-1">How We Can Reduce Bias?</div>
              <ul class="list-disc ml-6 text-sm mt-2 space-y-1">
                <li>Share diverse, balanced content</li>
                <li>Review your privacy settings</li>
                <li>
                  Be mindful of what you "like", "save", and "interact" with
                </li>
                <li>Support ethical, transparent AI apps</li>
              </ul>
            </div>

            <div class="bg-white/6 p-5 rounded-xl">
              <div class="text-2xl font-bold mt-1">Real-Life Examples</div>
              <ul class="list-disc ml-6 text-sm space-y-1 text-gray-100">
                <li>Face filters: Detect some skin tones better than others</li>
                <li>Hiring AI: Prefer certain gender keywords</li>
                <li>Product recommendations: Only target certain groups</li>
              </ul>
            </div>
          </div>

          <!-- Right: Image like in original -->
          <div class="flex justify-center lg:justify-end">
            <div class="overflow-hidden rounded-2xl w-full max-w-md shadow-2xl">
              <img
                src="assets/img/fairness.jpg"
                alt="AI operator"
                class="w-full h-full object-cover"
              />
            </div>
          </div>
        </div>

        <!-- subtle border -->
        <div
          class="absolute inset-0 rounded-3xl pointer-events-none border border-white/6"
        ></div>
      </div>
    </div>
  </section>
</template>

<script lang="ts" setup></script>

<style>
.bias-tile {
  background: linear-gradient(
    180deg,
    rgba(255, 255, 255, 0.03),
    rgba(255, 255, 255, 0.02)
  );
  border: 1px solid rgba(255, 255, 255, 0.06);
  box-shadow: 0 10px 30px rgba(8, 12, 30, 0.35);
  color: #fff;
}
</style>
