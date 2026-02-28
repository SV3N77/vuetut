<script setup lang="ts">
import { RouterLink } from 'vue-router'
</script>

<template>
  <nav class="bg-gray-800">
    <div class="max-w-4xl mx-auto flex justify-between items-center">
      <span class="text-xl font-bold text-gray-800">My App</span>
      <div class="space-x-4">
        <RouterLink to="/" class="text-gray-600 hover:text-blue-500 transition-colors"
          >Home</RouterLink
        >
        <RouterLink to="/about" class="text-gray-600 hover:text-blue-500 transition-colors"
          >About</RouterLink
        >
      </div>
    </div>
  </nav>
</template>
