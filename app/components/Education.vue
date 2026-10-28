<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

import certIstad from '../assets/images/cert-istad.png'
import certNode from '../assets/images/cert-ant-nodejs.png'
import award1st from '../assets/images/award-1st-ant.jpg'
import award2nd from '../assets/images/award-2nd-cstad.jpg'
import volunteerImg from '../assets/images/volunteer-wingbank.jpg'

/* ---------- DATA (edit here only) ----------
   Each section has a list of rows.
   `image` is optional: rows without one render as a text card.
--------------------------------------------- */
const sections = [
  {
    id: 'education',
    heading: 'Education',
    icon: '🎓',
    items: [
      {
        title: 'Bachelor of Computer Science',
        org: 'Western University · Phnom Penh',
        desc: 'Studying programming fundamentals and software development.',
        tagGroups: [
          {
            label: 'Relevant courses',
            tags: [
              'Web Development',
              'Database Management Systems',
              'Linux System Administration',
              'Mobile Programming',
              'Object-Oriented Programming',
              'Data Structures & Algorithms',
              'UX/UI Design',
            ],
          },
        ],
        date: '2024 – Present',
        ongoing: true,
      },
      {
        title: '100% Scholarship · Web Development Program',
        org: 'ANT Technology Training Center · Scholarship Trainee',
        desc: 'Full scholarship earned by placing 1st in the web design competition. Covers front-end, back-end and team development.',
        facts: [
          { label: 'Study schedule', value: 'Monday – Friday' },
          { label: 'Total study hours', value: '700 hours' },
          {
            label: 'Funding',
            value: 'Sponsored by the Ministry of Post and Telecommunications and CBRD Fund',
            wide: true,
          },
        ],
        tagGroups: [
          {
            label: 'Front-end',
            tags: ['HTML', 'CSS', 'Bootstrap', 'JavaScript', 'Vue.js', 'API Consumption'],
          },
          {
            label: 'Back-end',
            tags: ['Node.js', 'Express.js', 'API Design', 'JWT Authentication', 'MVC Architecture'],
          },
          {
            label: 'Extra courses',
            tags: ['C++', 'UX/UI Advanced Concepts', 'Cyber Security Fundamentals'],
          },
          {
            label: 'Practices',
            tags: ['Git & GitHub', 'Team Collaboration', 'SDLC'],
          },
        ],
        date: '16 Jun 2025 – 17 Jul 2026',
      },
      {
        title: 'High School',
        org: 'Mongkolborey High School · Banteay Meanchey',
        desc: 'Completed high school education.',
        date: '2021 – 2023',
      },
    ],
  },
  {
    id: 'programs',
    heading: 'Completed Programs',
    icon: '📜',
    items: [
      {
        title: 'Web Application Development with Node.js',
        org: 'ANT Technology Training Center',
        desc: 'Completed the Node.js course on building web applications.',
        tags: ['Node.js'],
        date: '16 Jun 2025 – 3 Jul 2026',
        image: certNode,
        alt: 'ANT Node.js certificate of completion',
      },
      {
        title: 'HTML, CSS & Bootstrap Training',
        org: 'ANT Technology Training Center',
        desc: 'Front-end training on responsive layouts and UI basics.',
        tags: ['HTML5', 'CSS3', 'Bootstrap'],
        date: 'Nov 2024 – Apr 2025',
      },
      {
        title: 'Pre-University Web Design Junior',
        org: 'Institute of Science and Technology Advanced Development (ISTAD)',
        desc: '90-hour scholarship program in front-end web design.',
        tags: ['HTML', 'CSS', 'Tailwind', 'UX/UI', 'JavaScript', 'ReactJS'],
        date: 'Feb 2025 – Apr 2025',
        image: certIstad,
        alt: 'ISTAD Web Design Junior certificate',
      },
    ],
  },
  {
    id: 'awards',
    heading: 'Competition Awards',
    icon: '🏆',
    items: [
      {
        title: '🥇 1st Place · Web Design Project',
        org: 'ANT Technology Training Center',
        desc: 'Won the HTML5, CSS3 & Bootstrap project competition, which led to the scholarship.',
        date: '2025',
        image: award1st,
        alt: '1st place award board at ANT',
      },
      {
        title: '🥈 2nd Place · Web Design Junior Project',
        org: 'CSTAD · ISTAD',
        desc: 'Silver Award for the Top 2 project team in the Web Design Junior competition.',
        date: 'April 2025',
        image: award2nd,
        alt: 'Silver award for top 2 project team',
      },
    ],
  },
  {
    id: 'volunteer',
    heading: 'Volunteering',
    icon: '🤝',
    items: [
      {
        title: 'National Career and Productivity Fair 2026',
        org: 'Wing Bank · Certificate of Appreciation',
        desc: 'Volunteered at the fair and was recognised for outstanding support and dedication.',
        date: '12–13 Sep 2026',
        image: volunteerImg,
        alt: 'Wing Bank certificate of appreciation',
      },
    ],
  },
]

/* ---------- LIGHTBOX ---------- */
const lightbox = ref(null)
const open = (src, alt) => (lightbox.value = { src, alt })
const close = () => (lightbox.value = null)
const onKey = (e) => e.key === 'Escape' && close()
onMounted(() => window.addEventListener('keydown', onKey))
onUnmounted(() => window.removeEventListener('keydown', onKey))
</script>

<template>
  <section id="education" class="relative scroll-mt-24 overflow-hidden px-6 py-28">
    <div class="relative z-10 mx-auto max-w-5xl">

      <!-- Header -->
      <header class="mx-auto mb-20 max-w-2xl text-center">
        <p class="mb-4 text-xs uppercase tracking-[0.3em] text-purple-400">
          Education & Achievement
        </p>
        <h2 class="text-4xl font-bold leading-tight text-white md:text-5xl">
          Learning Journey &
          <span class="bg-gradient-to-r from-purple-400 to-indigo-400 bg-clip-text text-transparent">
            Recognition
          </span>
        </h2>
        <p class="mt-5 text-gray-400">
          University, training, competitions and volunteering.
        </p>
      </header>

      <!-- Sections -->
      <div class="space-y-20">
        <section v-for="s in sections" :key="s.id" :aria-labelledby="'h-' + s.id">

          <!-- Section heading -->
          <div class="mb-8 flex items-center gap-4">
            <span
              class="flex h-12 w-12 shrink-0 items-center justify-center rounded-2xl border border-purple-400/40 bg-purple-500/10 text-xl"
            >
              {{ s.icon }}
            </span>
            <h3 :id="'h-' + s.id" class="text-2xl font-bold text-white md:text-3xl">
              {{ s.heading }}
            </h3>
            <span class="h-px flex-1 bg-gradient-to-r from-white/15 to-transparent"></span>
          </div>

          <!-- Rows -->
          <div class="space-y-5">
            <article
              v-for="item in s.items"
              :key="item.title"
              class="group grid gap-6 rounded-3xl border border-white/10 bg-white/5 p-6 backdrop-blur-xl transition duration-300 hover:border-purple-400/70"
              :class="item.image ? 'md:grid-cols-[1fr_250px]' : ''"
            >
              <!-- Text -->
              <div class="flex flex-col">
                <div class="flex flex-wrap items-center gap-3">
                  <h4 class="text-xl font-semibold leading-snug text-white">
                    {{ item.title }}
                  </h4>
                  <span
                    v-if="item.ongoing"
                    class="rounded-full bg-indigo-500/20 px-3 py-1 text-xs text-indigo-300"
                  >
                    In progress
                  </span>
                </div>

                <p class="mt-1 text-sm text-purple-400">{{ item.org }}</p>
                <p class="mt-3 text-sm leading-relaxed text-gray-400">{{ item.desc }}</p>

                <dl v-if="item.facts" class="mt-5 grid gap-x-6 gap-y-3 text-sm sm:grid-cols-2">
                  <div v-for="f in item.facts" :key="f.label" :class="f.wide ? 'sm:col-span-2' : ''">
                    <dt class="text-xs text-gray-500">{{ f.label }}</dt>
                    <dd class="text-gray-300">{{ f.value }}</dd>
                  </div>
                </dl>

                <div v-if="item.tagGroups" class="mt-5 space-y-4">
                  <div v-for="g in item.tagGroups" :key="g.label">
                    <p class="mb-2 text-xs text-gray-500">{{ g.label }}</p>
                    <ul class="flex flex-wrap gap-2">
                      <li
                        v-for="t in g.tags"
                        :key="t"
                        class="rounded-md border border-white/10 bg-white/5 px-2 py-0.5 text-xs text-gray-300"
                      >
                        {{ t }}
                      </li>
                    </ul>
                  </div>
                </div>

                <ul v-if="item.tags" class="mt-4 flex flex-wrap gap-2">
                  <li
                    v-for="t in item.tags"
                    :key="t"
                    class="rounded-md border border-white/10 bg-white/5 px-2 py-0.5 text-xs text-gray-300"
                  >
                    {{ t }}
                  </li>
                </ul>

                <p class="mt-auto pt-5 text-xs text-gray-500">{{ item.date }}</p>
              </div>

              <!-- Image: full picture always visible -->
              <button
                v-if="item.image"
                type="button"
                class="relative aspect-[4/3] w-full cursor-zoom-in self-start overflow-hidden rounded-2xl border border-white/10 bg-black/40 focus:outline-none focus-visible:ring-2 focus-visible:ring-purple-400"
                :aria-label="'View full image: ' + item.alt"
                @click="open(item.image, item.alt)"
              >
                <img
                  :src="item.image"
                  alt=""
                  aria-hidden="true"
                  class="absolute inset-0 h-full w-full scale-125 object-cover opacity-40 blur-2xl"
                />
                <img
                  :src="item.image"
                  :alt="item.alt"
                  class="absolute inset-0 h-full w-full object-contain p-1.5"
                />
                <span
                  class="absolute bottom-2 right-2 rounded-full bg-black/60 px-3 py-1 text-xs text-white opacity-0 transition-opacity duration-300 group-hover:opacity-100"
                >
                  Click to enlarge
                </span>
              </button>
            </article>
          </div>
        </section>
      </div>
    </div>

    <!-- Glow background -->
    <div class="pointer-events-none absolute -left-40 -top-40 h-96 w-96 animate-float rounded-full bg-purple-600/20 blur-3xl"></div>

    <!-- Lightbox -->
    <Teleport to="body">
      <div
        v-if="lightbox"
        class="fixed inset-0 z-[9999] flex cursor-zoom-out items-center justify-center bg-black/90 p-4"
        role="dialog"
        aria-modal="true"
        @click="close"
      >
        <button
          type="button"
          class="absolute right-5 top-5 h-10 w-10 rounded-full bg-white/10 text-lg text-white hover:bg-white/20"
          aria-label="Close"
          @click.stop="close"
        >
          ✕
        </button>
        <img
          :src="lightbox.src"
          :alt="lightbox.alt"
          class="max-h-[92vh] max-w-[95vw] rounded-xl object-contain shadow-2xl"
          @click.stop
        />
      </div>
    </Teleport>
  </section>
</template>

<style scoped>
@keyframes float {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-20px); }
}

.animate-float {
  animation: float 6s ease-in-out infinite;
}

@media (prefers-reduced-motion: reduce) {
  .animate-float { animation: none; }
}
</style>