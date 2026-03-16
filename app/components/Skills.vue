<template>
  <section id="skills" class="relative py-28 md:py-36 px-6 overflow-hidden">
    <div class="max-w-7xl mx-auto">

      <!-- Header -->
      <div
        ref="headerRef"
        class="text-center max-w-3xl mx-auto transition-all duration-1000 ease-out"
        :class="inViewHeader ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-10'"
      >
        <div class="inline-flex items-center gap-2 rounded-full border border-white/10 bg-white/5 px-4 py-2 backdrop-blur-xl">
          <span class="h-2 w-2 rounded-full bg-purple-500 animate-pulse shadow-[0_0_18px_rgba(168,85,247,0.8)]"></span>
          <p class="text-xs uppercase tracking-[0.25em] text-gray-300">Skills</p>
        </div>

        <h2 class="text-4xl md:text-6xl font-bold text-white leading-tight mt-6">
          Modern Frontend
          <span class="bg-gradient-to-r from-purple-400 to-indigo-400 bg-clip-text text-transparent animate-gradient">
            Technologies
          </span>
        </h2>

        <p class="mt-6 text-gray-400 text-lg leading-relaxed">
          Focused on crafting responsive, interactive, and modern user interfaces
          with clean architecture and smooth animation.
        </p>
      </div>

      <!-- Skills Grid -->
      <div class="mt-20 grid gap-8 md:grid-cols-2 lg:grid-cols-3">

        <div
          v-for="(skill, index) in skills"
          :key="skill.name"
          class="skillCard animate-fadeUp"
          :style="{ animationDelay: index * 0.15 + 's' }"
          @mousemove="tilt($event, $event.currentTarget)"
          @mouseleave="resetTilt($event.currentTarget)"
        >
          <div class="p-8">
            <h3 class="text-xl font-semibold text-white">
              {{ skill.name }}
            </h3>

            <p class="text-sm text-gray-400 mt-2">
              {{ skill.description }}
            </p>

            <!-- Progress -->
            <div class="mt-6">
              <div class="h-2 w-full bg-white/10 rounded-full overflow-hidden">
                <div
                  class="h-full bg-gradient-to-r from-purple-500 to-indigo-500 transition-all duration-1000 ease-out"
                  :style="{ width: inViewHeader ? skill.level + '%' : '0%' }"
                ></div>
              </div>

              <p class="text-xs text-gray-400 mt-2">
                {{ skill.level }}%
              </p>
            </div>
          </div>
        </div>

      </div>

      <!-- Tools -->
      <div class="mt-24 text-center">
        <h3 class="text-2xl font-semibold text-white mb-6">
          Tools & Environment
        </h3>

        <div class="flex flex-wrap justify-center gap-3">
          <span v-for="(tool, i) in tools"
                :key="tool"
                class="chip animate-chip"
                :style="{ animationDelay: i * 0.1 + 's' }">
            {{ tool }}
          </span>
        </div>
      </div>

    </div>

    <!-- Floating Background Glow -->
    <div class="absolute -top-32 -left-32 w-96 h-96 bg-purple-600/20 blur-3xl rounded-full animate-float"></div>
    <div class="absolute bottom-0 right-0 w-96 h-96 bg-indigo-600/20 blur-3xl rounded-full animate-float delay-2000"></div>
  </section>
</template>
<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue'

const headerRef = ref(null)
const inViewHeader = ref(false)
let observer

const skills = [
  { name: 'Vue.js & Nuxt', description: 'Component-based frontend & SSR architecture.', level: 70 },
  { name: 'JavaScript (ES6+)', description: 'Core logic for both Frontend and Backend.', level: 65 },
  { name: 'Node.js & Express', description: 'Building scalable REST APIs and server-side logic.', level: 50 }, // New Focus
  { name: 'Tailwind & UI/UX', description: 'Modern styling and responsive interface design.', level: 85 },
  { name: 'Database Management', description: 'Designing schemas with MySQL & MongoDB.', level: 60 },
  { name: 'Laravel (Legacy)', description: 'Familiarity with PHP-based backend systems.', level: 55 }
]

const tools = [
  'GitHub',
  'Vercel',
  'Git',
  'Postman',
  'Figma',
  'REST API',
  'Responsive Design',
  'XAMPP',
  'MySQL'
]

function tilt(event, element) {
  const rect = element.getBoundingClientRect()
  const x = event.clientX - rect.left
  const y = event.clientY - rect.top
  const midX = rect.width / 2
  const midY = rect.height / 2

  const rotateY = ((x - midX) / midX) * 8
  const rotateX = -((y - midY) / midY) * 8

  element.style.transform = `
    perspective(1000px)
    rotateX(${rotateX}deg)
    rotateY(${rotateY}deg)
    scale(1.05)
  `
}

function resetTilt(element) {
  element.style.transform = 'perspective(1000px) rotateX(0deg) rotateY(0deg) scale(1)'
}

onMounted(() => {
  observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
      if (entry.target === headerRef.value) {
        inViewHeader.value = entry.isIntersecting
      }
    })
  }, { threshold: 0.3 })

  observer.observe(headerRef.value)
})

onBeforeUnmount(() => {
  if (observer) observer.disconnect()
})
</script>

<style scoped>
.skillCard {
  @apply relative rounded-[32px] border border-white/10
         bg-white/5 backdrop-blur-xl
         shadow-[0_20px_120px_rgba(0,0,0,0.5)]
         transition duration-300 ease-out;
}

.skillCard:hover {
  @apply border-purple-400;
  box-shadow: 0 0 40px rgba(168,85,247,0.4);
}

.chip {
  @apply rounded-full border border-white/10 bg-white/5
         px-4 py-2 text-sm text-gray-300 backdrop-blur-xl
         transition duration-300 hover:scale-105 hover:border-purple-400 hover:text-white;
}

/* Animations */
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(40px); }
  to { opacity: 1; transform: translateY(0); }
}

.animate-fadeUp {
  animation: fadeUp 0.8s ease forwards;
  opacity: 0;
}

@keyframes float {
  0%,100% { transform: translateY(0px); }
  50% { transform: translateY(-20px); }
}

.animate-float {
  animation: float 6s ease-in-out infinite;
}

.animate-chip {
  animation: fadeUp 0.6s ease forwards;
  opacity: 0;
}
</style>
