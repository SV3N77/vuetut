<script setup lang="ts">
import { ref } from 'vue'

interface Game {
  id: number
  title: string
  genre: string
  rating: number
  releaseYear: number
  summary: string
  description: string
}

const games = ref<Game[]>([
  {
    id: 1,
    title: 'Cosmic Odyssey',
    genre: 'Space RPG',
    rating: 4.8,
    releaseYear: 2023,
    summary: 'Explore vast galaxies and uncover ancient mysteries',
    description:
      'Embark on an epic journey through the cosmos, discovering new planets, encountering alien civilizations, and solving the greatest mystery of the universe.',
  },
  {
    id: 2,
    title: 'Shadow Realm',
    genre: 'Action Adventure',
    rating: 4.5,
    releaseYear: 2022,
    summary: 'Master stealth in a dark fantasy world',
    description:
      'Navigate through treacherous dungeons, master the art of stealth, and defeat the darkness that threatens to consume the realm.',
  },
  {
    id: 3,
    title: 'Pixel Racing',
    genre: 'Racing',
    rating: 4.2,
    releaseYear: 2024,
    summary: 'High-speed retro racing championships',
    description:
      'Compete in adrenaline-pumping races across diverse tracks, upgrade your vehicle, and become the ultimate pixel racing champion.',
  },
  {
    id: 4,
    title: 'Crystal Kingdom',
    genre: 'Strategy',
    rating: 4.6,
    releaseYear: 2023,
    summary: 'Build and defend your magical empire',
    description:
      'Construct your kingdom, gather resources, train armies, and defend against rival factions in this enchanting strategy game.',
  },
  {
    id: 5,
    title: 'Cyber Legends',
    genre: 'Sci-Fi RPG',
    rating: 4.4,
    releaseYear: 2024,
    summary: 'Hack, slash, and survive in a cyberpunk world',
    description:
      'In a world where technology and magic collide, customize your character, upgrade your cybernetics, and battle through a futuristic city.',
  },
  {
    id: 6,
    title: 'Forest Guardian',
    genre: 'Simulation',
    rating: 4.3,
    releaseYear: 2022,
    summary: 'Protect and nurture a mystical forest',
    description:
      'Manage resources, care for magical creatures, and defend your forest from threats in this peaceful simulation game.',
  },
])
</script>

<template>
  <main class="min-h-screen bg-gradient-to-br from-emerald-950 via-green-900 to-teal-900 p-8">
    <div class="mx-auto">
      <header class="text-center mb-12">
        <h1 class="text-5xl font-bold text-emerald-100 mb-4">Game Collection</h1>
        <p class="text-emerald-300 text-lg">Explore our curated selection of games</p>
      </header>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <div
          v-for="game in games"
          :key="game.id"
          class="bg-emerald-50 rounded-xl shadow-lg overflow-hidden hover:shadow-2xl hover:scale-105 transition-all duration-300"
        >
          <div class="p-6">
            <div class="flex items-start justify-between mb-4">
              <h2 class="text-2xl font-bold text-emerald-900">{{ game.title }}</h2>
              <span class="bg-emerald-600 text-white text-xs font-semibold px-3 py-1 rounded-full">
                {{ game.genre }}
              </span>
            </div>

            <p class="text-emerald-700 text-sm mb-4 leading-relaxed">{{ game.summary }}</p>

            <p class="text-emerald-600 text-sm mb-4">{{ game.description }}</p>

            <div class="flex items-center justify-between pt-4 border-t border-emerald-200">
              <div class="flex items-center gap-2">
                <span class="text-amber-500 text-lg">★</span>
                <span class="font-semibold text-emerald-800">{{ game.rating }}</span>
              </div>
              <span class="text-emerald-600 text-sm">{{ game.releaseYear }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>
