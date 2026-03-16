<template>
  <section id="contact" class="relative py-32 px-6 overflow-hidden">

    <!-- Animated Gradient Background -->
    <div class="absolute inset-0 bg-gradient-to-br from-purple-900/40 via-black to-indigo-900/40 animate-gradientMove"></div>

    <div class="relative max-w-6xl mx-auto">

      <!-- Header -->
      <div class="text-center max-w-3xl mx-auto mb-20 animate-fadeUp">
        <p class="text-xs uppercase tracking-[0.3em] text-purple-400 mb-4">
          Contact
        </p>

        <h2 class="text-4xl md:text-6xl font-bold text-white leading-tight">
          Let’s Build Something
          <span class="bg-gradient-to-r from-purple-400 to-indigo-400 bg-clip-text text-transparent">
            Great Together
          </span>
        </h2>

        <p class="mt-6 text-gray-400 text-lg">
          I'm open to frontend projects, collaborations, internships,
          and creative web opportunities.
        </p>
      </div>

      <!-- Main Grid -->
      <div class="grid md:grid-cols-2 gap-16 items-center">

        <!-- Left Side Info -->
        <div class="space-y-10">

          <div class="infoBlock">
            <h3>Email</h3>
            <p>heanliza33@gmail.com</p>
          </div>

          <div class="infoBlock">
            <h3>Location</h3>
            <p>Phnom Penh, Cambodia</p>
          </div>

          <div class="infoBlock">
            <h3>Availability</h3>
            <p>Available for freelance & internship</p>
          </div>

          <!-- Social -->
          <div class="flex gap-4 mt-8">
            <a href="https://github.com/heanLiza" class="socialBtn">GitHub</a>
            <a href="www.linkedin.com/in/hean-liza-734030350" class="socialBtn">LinkedIn</a>
            <a href="https://t.me/areal_lizaa" class="socialBtn">Telegram</a>
          </div>

        </div>

        <!-- Right Side Form -->
        <div class="formCard">

          <form @submit.prevent="submitForm" class="space-y-6">

            <input v-model="form.name" type="text" placeholder="Your Name" class="input" required />
            <input v-model="form.email" type="email" placeholder="Your Email" class="input" required />
            <textarea v-model="form.message" rows="5" placeholder="Your Message" class="input" required></textarea>

            <button type="submit" class="submitBtn">
              Send Message
            </button>

          </form>

        </div>

      </div>

      <!-- Animated Walking Dot -->
      <div class="walker"></div>

    </div>
  </section>
</template>
<script setup>
import { ref } from 'vue'

const form = ref({
  name: '',
  email: '',
  message: ''
})

function submitForm() {
  alert('Message sent! (Frontend demo)')
  form.value = { name: '', email: '', message: '' }
}
</script>
<style scoped>

/* Info Blocks */
.infoBlock h3 {
  @apply text-purple-400 uppercase tracking-widest text-sm;
}

.infoBlock p {
  @apply text-white mt-2 text-lg;
}

/* Form */
.formCard {
  @apply rounded-[40px] border border-white/10
         bg-white/5 backdrop-blur-xl p-10
         shadow-[0_20px_120px_rgba(0,0,0,0.5)]
         transition duration-300 hover:border-purple-400;
}

.input {
  @apply w-full rounded-xl border border-white/10
         bg-white/5 px-4 py-3 text-white
         placeholder-gray-400 outline-none
         focus:border-purple-400 transition;
}

.submitBtn {
  @apply w-full rounded-xl bg-gradient-to-r
         from-purple-600 to-indigo-600
         py-3 font-semibold text-white
         hover:shadow-[0_0_30px_rgba(168,85,247,0.5)]
         transition duration-300;
}

/* Social Buttons */
.socialBtn {
  @apply px-5 py-2 rounded-full border border-white/10
         bg-white/5 text-white text-sm
         transition duration-300 hover:border-purple-400 hover:scale-105;
}

/* Gradient Background Animation */
@keyframes gradientMove {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

.animate-gradientMove {
  background-size: 200% 200%;
  animation: gradientMove 15s ease infinite;
}

/* Fade Animation */
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(40px); }
  to { opacity: 1; transform: translateY(0); }
}

.animate-fadeUp {
  animation: fadeUp 1s ease forwards;
}

/* Floating Walker Dot (Run Animation Feel) */
.walker {
  position: absolute;
  bottom: 20px;
  left: 0;
  width: 12px;
  height: 12px;
  background: linear-gradient(to right, #a855f7, #6366f1);
  border-radius: 50%;
  animation: walk 8s linear infinite;
  box-shadow: 0 0 20px rgba(168,85,247,0.8);
}

@keyframes walk {
  0% { left: 0%; }
  50% { left: 90%; }
  100% { left: 0%; }
}

</style>
