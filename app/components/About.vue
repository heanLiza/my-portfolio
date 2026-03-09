<template>
  <section id="about" class="relative py-28 md:py-36 px-6">
    <div class="mx-auto max-w-7xl">
      
      <!-- Header -->
      <div
        ref="headerRef"
        class="mx-auto max-w-3xl text-center transition-all duration-700 ease-out"
        :class="inViewHeader ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-6'"
      >
        <div class="inline-flex items-center gap-2 rounded-full border border-white/10 bg-white/5 px-4 py-2 backdrop-blur-xl">
          <span class="h-2 w-2 rounded-full bg-purple-500 shadow-[0_0_18px_rgba(168,85,247,0.8)]"></span>
          <p class="text-xs uppercase tracking-[0.25em] text-gray-300">About</p>
        </div>

        <h2 class="mt-6 text-4xl md:text-6xl font-extrabold leading-tight text-white">
          Focused on
          <span class="bg-gradient-to-r from-purple-400 to-indigo-400 bg-clip-text text-transparent">
            Frontend Development
          </span>
        </h2>

        <p class="mt-5 text-base md:text-lg leading-relaxed text-gray-400">
          I’m a frontend developer passionate about building modern,
          responsive, and visually polished web interfaces.
          I focus on clean UI structure, smooth user experience,
          and writing maintainable frontend code.
        </p>
      </div>

      <!-- Content -->
      <div class="mt-16 grid gap-10 lg:grid-cols-2 lg:gap-14 items-center">

        <!-- 3D Tilt Card -->
        <div
          ref="tiltRef"
          class="relative will-change-transform"
          @mousemove="onMove"
          @mouseenter="onEnter"
          @mouseleave="onLeave"
        >
          <!-- Glow -->
          <div class="absolute -inset-6 rounded-[40px] bg-gradient-to-tr from-purple-600/25 to-indigo-600/15 blur-3xl opacity-60"></div>

          <div
            class="relative rounded-[40px] border border-white/10 bg-white/5 backdrop-blur-xl overflow-hidden
                   shadow-[0_20px_120px_rgba(0,0,0,0.5)]"
            :style="cardStyle"
          >
            <div class="pointer-events-none absolute inset-0 opacity-70">
              <div class="absolute -top-24 left-10 h-48 w-72 rotate-12 bg-white/10 blur-2xl"></div>
              <div class="absolute -bottom-28 right-0 h-60 w-80 -rotate-12 bg-purple-500/10 blur-2xl"></div>
            </div>

            <div class="p-8 md:p-10">
              <div class="flex items-center justify-between">
                <div class="space-y-2">
                  <p class="text-sm text-gray-300">Primary Focus</p>
                  <h3 class="text-2xl md:text-3xl font-bold text-white">
                    UI Development & User Experience
                  </h3>
                </div>

                <div class="hidden md:flex h-12 w-12 items-center justify-center rounded-2xl bg-purple-500/15 border border-purple-400/20">
                  <div class="h-2 w-2 rounded-full bg-purple-400 shadow-[0_0_18px_rgba(168,85,247,0.9)]"></div>
                </div>
              </div>

              <p class="mt-6 text-gray-400 leading-relaxed">
                I specialize in creating clean, responsive, and interactive
                web interfaces using modern frontend technologies.
                While I have basic backend understanding,
                my strength lies in building structured and polished user interfaces.
              </p>

              <!-- Languages (kept same but honest positioning) -->
              <div class="mt-7 flex flex-wrap gap-2">
                <span class="chip">Nuxt</span>
                <span class="chip">Vue</span>
                <span class="chip">Tailwind</span>
                <span class="chip">Laravel (Basic)</span>
                <span class="chip">REST API Integration</span>
                <span class="chip">MySQL (Basic)</span>
              </div>

              <!-- Mini grid -->
              <div class="mt-8 grid gap-4 sm:grid-cols-2">
                <div class="rounded-2xl border border-white/10 bg-white/5 p-5 hover:bg-white/10 transition">
                  <p class="text-sm text-gray-300">Frontend Strength</p>
                  <p class="mt-1 text-white font-semibold">Responsive & Interactive UI</p>
                  <p class="mt-2 text-sm text-gray-400">
                    Modern layouts, animations, clean design systems.
                  </p>
                </div>

                <div class="rounded-2xl border border-white/10 bg-white/5 p-5 hover:bg-white/10 transition">
                  <p class="text-sm text-gray-300">Learning Direction</p>
                  <p class="mt-1 text-white font-semibold">Backend Improvement</p>
                  <p class="mt-2 text-sm text-gray-400">
                    Continuously improving backend knowledge and system logic.
                  </p>
                </div>
              </div>
            </div>

            <div class="h-[2px] w-full bg-gradient-to-r from-transparent via-purple-500/40 to-transparent"></div>
          </div>
        </div>

        <!-- Right Side -->
        <div
          ref="rightRef"
          class="space-y-8 transition-all duration-700 ease-out delay-100"
          :class="inViewRight ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-6'"
        >
          <div class="rounded-[32px] border border-white/10 bg-white/5 backdrop-blur-xl p-8 md:p-10">
            <h3 class="text-2xl font-bold text-white">What I Do</h3>

            <p class="mt-4 text-gray-400 leading-relaxed">
              I build frontend applications that prioritize user experience,
              clarity, and responsive design.
              I enjoy transforming design concepts into functional,
              smooth, and accessible interfaces.
            </p>

            <div class="mt-7 space-y-4">
              <div class="flex items-start gap-4">
                <span class="mt-1 h-2.5 w-2.5 rounded-full bg-purple-400 shadow-[0_0_14px_rgba(168,85,247,0.9)]"></span>
                <div>
                  <p class="font-semibold text-white">Responsive Layouts</p>
                  <p class="text-sm text-gray-400">Mobile-first and clean UI structure.</p>
                </div>
              </div>

              <div class="flex items-start gap-4">
                <span class="mt-1 h-2.5 w-2.5 rounded-full bg-indigo-400 shadow-[0_0_14px_rgba(129,140,248,0.9)]"></span>
                <div>
                  <p class="font-semibold text-white">UI Animation</p>
                  <p class="text-sm text-gray-400">Smooth transitions and interactive effects.</p>
                </div>
              </div>

              <div class="flex items-start gap-4">
                <span class="mt-1 h-2.5 w-2.5 rounded-full bg-purple-300 shadow-[0_0_14px_rgba(196,181,253,0.9)]"></span>
                <div>
                  <p class="font-semibold text-white">API Integration</p>
                  <p class="text-sm text-gray-400">Connecting frontend with backend services.</p>
                </div>
              </div>
            </div>

            <!-- Stats -->
            <div class="mt-10 grid grid-cols-3 gap-5">
              <div class="stat">
                <p class="statNum">5+</p>
                <p class="statLabel">Projects</p>
              </div>
              <div class="stat">
                <p class="statNum">10+</p>
                <p class="statLabel">UI Sections</p>
              </div>
              <div class="stat">
                <p class="statNum">Growing</p>
                <p class="statLabel">Experience</p>
              </div>
            </div>
          </div>

          <div class="rounded-[28px] border border-white/10 bg-white/5 backdrop-blur-xl p-6 text-gray-400">
            <p class="text-sm leading-relaxed">
              I’m continuously learning and improving my skills to grow into a stronger frontend engineer.
            </p>
          </div>
        </div>
      </div>
    </div>

    <div class="pointer-events-none absolute inset-0 -z-10 opacity-40">
      <div class="absolute inset-0 bg-[radial-gradient(circle_at_1px_1px,rgba(255,255,255,0.06)_1px,transparent_0)] [background-size:34px_34px]"></div>
    </div>
  </section>
</template>

<script setup>
import { onMounted, onBeforeUnmount, ref, computed } from 'vue'

/** Scroll reveal */
const headerRef = ref(null)
const rightRef = ref(null)
const inViewHeader = ref(false)
const inViewRight = ref(false)
let io

/** 3D Tilt */
const tiltRef = ref(null)
const rotateX = ref(0)
const rotateY = ref(0)
const scale = ref(1)

const cardStyle = computed(() => ({
  transform: `perspective(1100px) rotateX(${rotateX.value}deg) rotateY(${rotateY.value}deg) scale(${scale.value})`,
  transition: `transform 180ms ease`
}))

function onEnter() {
  scale.value = 1.02
}
function onLeave() {
  rotateX.value = 0
  rotateY.value = 0
  scale.value = 1
}
function onMove(e) {
  const el = tiltRef.value
  if (!el) return
  const card = el.querySelector(':scope > div:nth-child(2)') // the main card
  if (!card) return

  const rect = card.getBoundingClientRect()
  const x = e.clientX - rect.left
  const y = e.clientY - rect.top

  const midX = rect.width / 2
  const midY = rect.height / 2

  // subtle, modern tilt
  rotateY.value = ((x - midX) / midX) * 8
  rotateX.value = -((y - midY) / midY) * 6
}

onMounted(() => {
  io = new IntersectionObserver(
    (entries) => {
      for (const entry of entries) {
        if (entry.target === headerRef.value) inViewHeader.value = entry.isIntersecting
        if (entry.target === rightRef.value) inViewRight.value = entry.isIntersecting
      }
    },
    { threshold: 0.18 }
  )

  if (headerRef.value) io.observe(headerRef.value)
  if (rightRef.value) io.observe(rightRef.value)
})

onBeforeUnmount(() => {
  if (io) io.disconnect()
})
</script>

<style scoped>
/* Tailwind-friendly utility classes as component styles */
.chip {
  @apply rounded-full border border-white/10 bg-white/5 px-3 py-1 text-xs text-gray-300 backdrop-blur-xl;
}

.stat {
  @apply rounded-2xl border border-white/10 bg-white/5 px-4 py-5 text-center hover:bg-white/10 transition;
}
.statNum {
  @apply text-2xl md:text-3xl font-extrabold text-purple-400;
}
.statLabel {
  @apply mt-1 text-xs md:text-sm text-gray-400;
}
</style>
