<script setup lang="ts">
import { RouterLink } from 'vue-router'
</script>

<template>
  <nav class="bg-emerald-950 py-4 px-8">
    <div class="mx-auto flex justify-between items-center">
      <span class="text-xl font-bold text-emerald-100">Game Collections</span>
      <div class="flex items-center gap-4">
        <RouterLink to="/" class="text-emerald-200 hover:text-emerald-400 transition-colors"
          >Home</RouterLink
        >
        <RouterLink to="/about" class="text-emerald-200 hover:text-emerald-400 transition-colors"
          >About</RouterLink
        >
      </div>
    </div>
  </nav>
</template>
