<template>
  <section id="ai-data" class="py-10 bg-white rounded-3xl p-8 shadow-lg">
    <h3 class="text-3xl font-bold text-purple-700">AI & Your Data</h3>
    <p class="mt-4 text-gray-700 leading-relaxed">
      Everyday actions "likes, searches, clicks, and uploaded content" generate
      data that can be used to train AI models. While this helps AI provide
      smarter recommendations and personalized experiences, it can also reveal
      sensitive patterns about you. Often, this data is collected without our
      full awareness or consent.
    </p>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mt-8">
      <div
        class="p-6 border rounded-xl hover:shadow-md transition-shadow duration-300"
      >
        <h4 class="font-semibold text-purple-700 mb-2">
          What Data is Collected?
        </h4>
        <ul class="text-gray-600 list-disc list-inside space-y-1">
          <li>
            <strong>Device & Location Data:</strong> IP addresses, GPS, device
            type
          </li>
          <li>
            <strong>Search & Browsing History:</strong> Queries, visited
            websites, clicks
          </li>
          <li>
            <strong>Photos & Uploaded Files:</strong> Images, documents, videos
            shared online
          </li>
          <li>
            <strong>Behavioral Data:</strong> Likes, shares, app usage patterns
          </li>
        </ul>
      </div>

      <div
        class="p-6 border rounded-xl hover:shadow-md transition-shadow duration-300"
      >
        <h4 class="font-semibold text-purple-700 mb-2">Why It Matters</h4>
        <p class="text-gray-600 leading-relaxed">
          Data collected from users helps AI models predict preferences,
          personalize content, and even influence decisions in areas like
          advertising, hiring, and healthcare. Mismanagement or misuse of this
          data can lead to privacy risks or biased outcomes.
        </p>
      </div>
    </div>

    <div class="mt-8 p-4 bg-purple-50 border-l-4 border-purple-400 rounded-lg">
      <h4 class="font-semibold text-purple-700 mb-2">Protect Yourself</h4>
      <ul class="text-gray-700 list-disc list-inside space-y-1">
        <li>Review app and website privacy settings regularly</li>
        <li>Limit the amount of personal data you share online</li>
        <li>Use privacy-focused browsers or search engines</li>
        <li>Understand how your data might be used by AI services</li>
      </ul>
    </div>
  </section>
</template>

<script lang="ts" setup></script>

<style></style>
