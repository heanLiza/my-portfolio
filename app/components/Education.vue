<template>
  <section id="education" class="relative py-32 px-6 overflow-hidden">
    <div class="max-w-7xl mx-auto">

      <!-- Header -->
      <div class="text-center max-w-3xl mx-auto mb-20">
        <p class="text-xs uppercase tracking-[0.3em] text-purple-400 mb-4">
          Education & Achievement
        </p>

        <h2 class="text-4xl md:text-6xl font-bold text-white leading-tight">
          Learning Journey &
          <span class="bg-gradient-to-r from-purple-400 to-indigo-400 bg-clip-text text-transparent">
            Recognition
          </span>
        </h2>

        <p class="mt-6 text-gray-400 text-lg">
          My academic and professional development through university,
          scholarships, and competitive web design achievements.
        </p>
      </div>

      <!-- CURRENT STATUS -->
      <div class="grid md:grid-cols-2 gap-10">

        <!-- University -->
        <div class="highlightCard">
          <h3 class="title">Bachelor of Computer Science</h3>
          <p class="subtitle">Western University</p>
          <p class="desc">
            Currently studying Computer Science since 2024,
            focusing on programming fundamentals and software development.
          </p>
          <p class="date">2024 – Present</p>
        </div>

        <!-- ANT Scholarship -->
        <div class="highlightCard purpleBorder">
          <h3 class="title">100% Scholarship – Web Development Program</h3>
          <p class="subtitle">ANT Technology Training Center</p>
          <p class="desc">
            Awarded a full 1-year scholarship (June 16, 2025 – Present)
            after achieving 1st place in Web Design competition.
            Currently participating in structured web development training,
            including team-based project development.
          </p>
          <p class="date">2025 – Present</p>
        </div>

      </div>

      <!-- Completed Programs -->
      <div class="mt-24">
        <h3 class="sectionTitle">Completed Programs</h3>

        <div class="grid md:grid-cols-2 gap-8 mt-10">

          <!-- ISTAD -->
          <div class="card">
            <h4 class="titleSmall">Pre-University Web Junior (3 Months)</h4>
            <p class="subtitle">ISTAD</p>
            <p class="descSmall">
              Successfully completed 3-month scholarship-based Web Junior program,
              focusing on foundational web development skills.
            </p>
            <p class="date">2025</p>
          </div>

          <!-- ANT Course -->
          <div class="card">
            <h4 class="titleSmall">HTML, CSS & Bootstrap Training</h4>
            <p class="subtitle">ANT Technology Training Center</p>
            <p class="descSmall">
              Completed structured frontend training covering responsive layouts
              and UI fundamentals.
            </p>
            <p class="date"> 2025</p>
          </div>

        </div>
      </div>

      <!-- Awards -->
      <div class="mt-24">
        <h3 class="sectionTitle">Competition Awards</h3>

        <div class="grid md:grid-cols-2 gap-8 mt-10">

          <div class="card">
            <h4 class="titleSmall">🥇 1st Place – Web Design Project</h4>
            <p class="subtitle">ANT Technology Training Center</p>
            <p class="descSmall">
              Achieved first place in Web Design competition,
              leading to 100% scholarship award.
            </p>
            <p class="date">2025</p>
          </div>

          <div class="card">
            <h4 class="titleSmall">🥈 2nd Place – Web Design Junior Project</h4>
            <p class="subtitle">ISTAD</p>
            <p class="descSmall">
              Awarded second place in Web Design Junior project competition.
            </p>
            <p class="date">April 2025</p>
          </div>

        </div>
      </div>

    </div>

    <!-- Glow Background -->
    <div class="absolute -top-40 -left-40 w-96 h-96 bg-purple-600/20 blur-3xl rounded-full animate-float"></div>
  </section>
</template>


<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue'

const headerRef = ref(null)
const inView = ref(false)
let observer

const timeline = [
  {
    title: '1st Place – Web Design Competition',
    place: 'ANT Technology Training Center',
    description: 'Achieved first place in web design competition, demonstrating frontend layout and UI creativity.',
    date: '2024'
  },
  {
    title: '2nd Place – Web Design Junior',
    place: 'ISATD',
    description: 'Awarded second place in junior web design competition.',
    date: 'April 2025'
  },
  {
    title: 'Short Course – HTML & CSS',
    place: 'ANT Technology Training Center',
    description: 'Completed foundational frontend development training.',
    date: '2024 – 2025'
  },
  {
    title: 'Short Course – Web Junior',
    place: 'ISATD',
    description: 'Focused on practical web development fundamentals.',
    date: '2025'
  },
  {
    title: 'Bachelor of Computer Science',
    place: 'Western University',
    description: 'Currently pursuing degree in Computer Science.',
    date: '2024 – Present'
  }
]




onMounted(() => {
  if (process.client) {
    observer = new IntersectionObserver(entries => {
      entries.forEach(entry => {
        if (entry.target === headerRef.value) {
          inView.value = entry.isIntersecting
        }
      })
    }, { threshold: 0.2 })

    if (headerRef.value) {
      observer.observe(headerRef.value)
    }
  }
})


onBeforeUnmount(() => {
  if (observer) observer.disconnect()
})
</script>
<style scoped>
.sectionTitle {
  @apply text-3xl font-bold text-white text-center;
}

.highlightCard {
  @apply relative rounded-[40px] border border-white/10
         bg-white/5 backdrop-blur-xl p-10
         shadow-[0_20px_120px_rgba(0,0,0,0.5)]
         transition duration-300 hover:border-purple-400;
}

.purpleBorder {
  @apply border-purple-400/40;
}

.card {
  @apply relative rounded-[32px] border border-white/10
         bg-white/5 backdrop-blur-xl p-8
         shadow-[0_20px_100px_rgba(0,0,0,0.5)]
         transition duration-300 hover:border-purple-400;
}

.title {
  @apply text-2xl font-semibold text-white;
}

.titleSmall {
  @apply text-xl font-semibold text-white;
}

.subtitle {
  @apply text-purple-400 text-sm mt-2;
}

.desc {
  @apply text-gray-400 mt-4 leading-relaxed;
}

.descSmall {
  @apply text-gray-400 text-sm mt-3;
}

.date {
  @apply text-xs text-gray-500 mt-5;
}

@keyframes float {
  0%,100% { transform: translateY(0px); }
  50% { transform: translateY(-20px); }
}

.animate-float {
  animation: float 6s ease-in-out infinite;
}
</style>
