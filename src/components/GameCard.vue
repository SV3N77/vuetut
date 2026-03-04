<script setup lang="ts">
import type { Game } from '../types/game'

interface Props {
  game: Game
}

defineProps<Props>()
</script>

<template>
  <div
    class="bg-emerald-50 rounded-xl shadow-lg overflow-hidden hover:shadow-2xl hover:scale-105 transition-all duration-300"
  >
    <div class="p-8 flex flex-col h-full">
      <div class="flex items-start justify-between">
        <h2 class="text-2xl font-bold text-emerald-900">{{ game.title }}</h2>
        <span class="bg-emerald-600 text-white text-xs font-semibold px-3 py-1 rounded-full">
          {{ game.genre }}
        </span>
      </div>

      <div class="flex-grow py-2">
        <p class="text-emerald-700 text-sm leading-relaxed">{{ game.summary }}</p>

        <p class="text-emerald-600 text-sm">{{ game.description }}</p>
      </div>

      <div class="flex items-center justify-between pt-4 border-t border-emerald-200">
        <div class="flex items-center gap-2">
          <span class="text-amber-500 text-lg">★</span>
          <span class="font-semibold text-emerald-800">{{ game.rating }}</span>
        </div>
        <span class="text-emerald-600 text-sm">{{ game.releaseYear }}</span>
      </div>
    </div>
  </div>
</template>
