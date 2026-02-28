<script setup lang="ts">
import { RouterLink } from 'vue-router'
</script>

<template>
  <main class="min-h-screen flex flex-col items-center justify-center bg-gray-50 p-8">
    <div class="text-center">
      <h1 class="text-4xl font-bold text-gray-800 mb-4">About This App</h1>
      <p class="text-gray-600 mb-8">
        This is a temporary about page with some placeholder content.
      </p>
      <RouterLink
        to="/"
        class="px-6 py-3 bg-blue-500 text-white rounded-lg hover:bg-blue-600 transition-colors"
      >
        Back to Home
      </RouterLink>
    </div>
  </main>
</template>
