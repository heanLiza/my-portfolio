<template>
  <section id="projects" class="py-20 px-6 bg-[#050505] text-white">
    <div class="max-w-6xl mx-auto">
      <div class="text-center mb-16">
        <h2 class="text-4xl md:text-5xl font-bold mb-4">
          Featured <span class="text-[#6823ff]">Projects</span>
        </h2>
        <p class="text-gray-400 max-w-2xl mx-auto">
          A collection of web applications built with modern frameworks, 
          focusing on clean code and user-centric design.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div 
          v-for="(project, index) in projects" 
          :key="index"
          class="bg-[#111111] border border-gray-800 rounded-2xl overflow-hidden hover:border-[#6823ff] transition-all duration-300 group"
        >
          <div class="p-6">
            <h3 class="text-xl font-semibold mb-2 group-hover:text-[#6823ff] transition-colors">
              {{ project.title }}
            </h3>
            <p class="text-gray-400 text-sm mb-4 leading-relaxed">
              {{ project.description }}
            </p>
            
            <div class="flex flex-wrap gap-2 mb-6">
              <span 
                v-for="tech in project.tech" 
                :key="tech"
                class="text-[10px] uppercase tracking-wider bg-[#1a1a1a] text-[#6823ff] px-2 py-1 rounded"
              >
                {{ tech }}
              </span>
            </div>

            <div class="flex items-center gap-4">
              <a 
                :href="project.link" 
                target="_blank" 
                class="text-sm font-medium flex items-center gap-1 hover:underline"
              >
                Live Demo <span class="text-xs">↗</span>
              </a>
              <span class="text-gray-600">|</span>
              <a 
                href="#" 
                class="text-sm text-gray-400 hover:text-white transition-colors"
              >
                GitHub
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const projects = [
  {
    title: 'ReabList',
    description: 'A productivity-focused to-do list application with dynamic task management and real-time state handling.',
    tech: ['Vue.js', 'Node.js', 'Boostrap'],
    link: 'https://reablist.vercel.app/'
  },

  {
    title: 'Wiboard',
    description: 'An interactive dashboard system for visualizing collaborative data and managing user workflows.',
    tech: ['React.js', 'API', 'Tailwind'],
    link: 'https://wiboard.vercel.app/'
  },
    {
    title: 'Vichea-Learn',
    description: 'An online learning platform designed for structured course delivery and intuitive student navigation.',
    tech: [ 'HTML', 'Bootstrap', 'JavaScript'],
    link: 'https://vichea-learn.vercel.app/'
  },

];
</script>

<style scoped>
/* Optional: Adds a subtle glow to the card on hover */
.group:hover {
  box-shadow: 0 10px 30px -15px rgba(104, 35, 255, 0.3);
}
</style>