<template>
  <section id="projects" class="relative py-24 px-6 bg-[#050505] text-white overflow-hidden">
    <div class="pointer-events-none absolute -top-40 left-1/2 -translate-x-1/2 w-[700px] h-[700px] rounded-full bg-[#6823ff]/10 blur-[140px]"></div>

    <div class="relative max-w-6xl mx-auto">
      <!-- Header -->
      <div class="mb-16 flex flex-col md:flex-row md:items-end md:justify-between gap-6">
        <div>
          <span class="inline-flex items-center gap-2 text-xs uppercase tracking-[0.25em] text-[#6823ff] mb-4">
            <span class="w-8 h-px bg-[#6823ff]"></span> Portfolio
          </span>
          <h2 class="text-4xl md:text-6xl font-bold leading-tight">
            Featured <span class="text-[#6823ff]">Projects</span>
          </h2>
        </div>
        <p class="text-gray-400 max-w-md leading-relaxed">
       
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">

        <!-- 01 Wedding -->
        <article class="group flex flex-col bg-[#0d0d0d] border border-white/10 rounded-3xl overflow-hidden hover:border-[#6823ff]/70 hover:-translate-y-1 transition-all duration-300 lg:col-span-2">
          <div class="relative h-56 overflow-hidden">
            <img src="../assets/images/wedding.png" alt="Wedding E-Invitation" class="w-full h-full object-cover object-top group-hover:scale-105 transition-transform duration-700" />
            <div class="absolute inset-0 bg-gradient-to-t from-[#0d0d0d] via-[#0d0d0d]/20 to-transparent"></div>
            <span class="absolute top-4 left-4 text-xs font-mono text-white/80 bg-black/50 backdrop-blur-md border border-white/10 px-3 py-1 rounded-full">01</span>
            <span class="absolute top-4 right-4 text-[10px] uppercase tracking-wider bg-[#6823ff] px-3 py-1 rounded-full">Latest</span>
          </div>
          <div class="flex flex-col flex-1 p-6">
            <h3 class="text-xl font-semibold mb-2 group-hover:text-[#6823ff] transition-colors">Wedding E-Invitation — Meng &amp; Leakhena</h3>
            <p class="text-gray-400 text-sm leading-relaxed mb-5">A bilingual (Khmer / English) digital wedding invitation with elegant animations, couple details, date and venue — matching the printed card.</p>
            <div class="flex flex-wrap gap-2 mb-6">
              <span class="text-[10px] uppercase tracking-wider text-[#6823ff] bg-[#6823ff]/10 border border-[#6823ff]/20 px-2.5 py-1 rounded-full">HTML</span>
              <span class="text-[10px] uppercase tracking-wider text-[#6823ff] bg-[#6823ff]/10 border border-[#6823ff]/20 px-2.5 py-1 rounded-full">CSS</span>
              <span class="text-[10px] uppercase tracking-wider text-[#6823ff] bg-[#6823ff]/10 border border-[#6823ff]/20 px-2.5 py-1 rounded-full">JavaScript</span>
            </div>
            <div class="mt-auto flex items-center gap-3">
              <a href="https://our-wedding-meng-leakhena.vercel.app/" target="_blank" rel="noopener" class="inline-flex items-center gap-1.5 text-sm font-medium bg-[#6823ff] hover:bg-[#7d44ff] px-4 py-2 rounded-full transition-colors">Live Demo <span class="text-xs">↗</span></a>
              <a href="#" target="_blank" rel="noopener" class="text-sm text-gray-400 hover:text-white border border-white/10 hover:border-white/30 px-4 py-2 rounded-full transition-colors">GitHub</a>
            </div>
          </div>
        </article>

        <!-- 02 Pralong -->
        <article class="group flex flex-col bg-[#0d0d0d] border border-white/10 rounded-3xl overflow-hidden hover:border-[#6823ff]/70 hover:-translate-y-1 transition-all duration-300">
          <div class="relative h-56 overflow-hidden">
            <img src="../assets/images/pralong.png" alt="Pralong" class="w-full h-full object-cover object-top group-hover:scale-105 transition-transform duration-700" />
            <div class="absolute inset-0 bg-gradient-to-t from-[#0d0d0d] via-[#0d0d0d]/20 to-transparent"></div>
            <span class="absolute top-4 left-4 text-xs font-mono text-white/80 bg-black/50 backdrop-blur-md border border-white/10 px-3 py-1 rounded-full">02</span>
          </div>
          <div class="flex flex-col flex-1 p-6">
            <h3 class="text-xl font-semibold mb-2 group-hover:text-[#6823ff] transition-colors">Pralong</h3>
            <p class="text-gray-400 text-sm leading-relaxed mb-5">A comprehensive Quiz Management System designed for instructors to create, manage, and analyze student examination results in real-time.</p>
            <div class="flex flex-wrap gap-2 mb-6">
              <span class="text-[10px] uppercase tracking-wider text-[#6823ff] bg-[#6823ff]/10 border border-[#6823ff]/20 px-2.5 py-1 rounded-full">Vue.js</span>
              <span class="text-[10px] uppercase tracking-wider text-[#6823ff] bg-[#6823ff]/10 border border-[#6823ff]/20 px-2.5 py-1 rounded-full">Node.js</span>
              <span class="text-[10px] uppercase tracking-wider text-[#6823ff] bg-[#6823ff]/10 border border-[#6823ff]/20 px-2.5 py-1 rounded-full">Bootstrap</span>
              <span class="text-[10px] uppercase tracking-wider text-[#6823ff] bg-[#6823ff]/10 border border-[#6823ff]/20 px-2.5 py-1 rounded-full">MySQL</span>
            </div>
            <div class="mt-auto flex items-center gap-3">
              <a href="https://qmlsystem.tdomain.work.gd/" target="_blank" rel="noopener" class="inline-flex items-center gap-1.5 text-sm font-medium bg-[#6823ff] hover:bg-[#7d44ff] px-4 py-2 rounded-full transition-colors">Live Demo <span class="text-xs">↗</span></a>
              <a href="#" target="_blank" rel="noopener" class="text-sm text-gray-400 hover:text-white border border-white/10 hover:border-white/30 px-4 py-2 rounded-full transition-colors">GitHub</a>
            </div>
          </div>
        </article>

        <!-- 03 ReabList -->
        <article class="group flex flex-col bg-[#0d0d0d] border border-white/10 rounded-3xl overflow-hidden hover:border-[#6823ff]/70 hover:-translate-y-1 transition-all duration-300">
          <div class="relative h-56 overflow-hidden">
            <img src="../assets/images/reablist.png" alt="ReabList" class="w-full h-full object-cover object-top group-hover:scale-105 transition-transform duration-700" />
            <div class="absolute inset-0 bg-gradient-to-t from-[#0d0d0d] via-[#0d0d0d]/20 to-transparent"></div>
            <span class="absolute top-4 left-4 text-xs font-mono text-white/80 bg-black/50 backdrop-blur-md border border-white/10 px-3 py-1 rounded-full">03</span>
          </div>
          <div class="flex flex-col flex-1 p-6">
            <h3 class="text-xl font-semibold mb-2 group-hover:text-[#6823ff] transition-colors">ReabList</h3>
            <p class="text-gray-400 text-sm leading-relaxed mb-5">A productivity-focused to-do list application with dynamic task management and real-time state handling.</p>
            <div class="flex flex-wrap gap-2 mb-6">
              <span class="text-[10px] uppercase tracking-wider text-[#6823ff] bg-[#6823ff]/10 border border-[#6823ff]/20 px-2.5 py-1 rounded-full">Vue.js</span>
              <span class="text-[10px] uppercase tracking-wider text-[#6823ff] bg-[#6823ff]/10 border border-[#6823ff]/20 px-2.5 py-1 rounded-full">Node.js</span>
              <span class="text-[10px] uppercase tracking-wider text-[#6823ff] bg-[#6823ff]/10 border border-[#6823ff]/20 px-2.5 py-1 rounded-full">Bootstrap</span>
            </div>
            <div class="mt-auto flex items-center gap-3">
              <a href="https://reablist.vercel.app/" target="_blank" rel="noopener" class="inline-flex items-center gap-1.5 text-sm font-medium bg-[#6823ff] hover:bg-[#7d44ff] px-4 py-2 rounded-full transition-colors">Live Demo <span class="text-xs">↗</span></a>
              <a href="#" target="_blank" rel="noopener" class="text-sm text-gray-400 hover:text-white border border-white/10 hover:border-white/30 px-4 py-2 rounded-full transition-colors">GitHub</a>
            </div>
          </div>
        </article>

        <!-- 04 Wiboard -->
        <article class="group flex flex-col bg-[#0d0d0d] border border-white/10 rounded-3xl overflow-hidden hover:border-[#6823ff]/70 hover:-translate-y-1 transition-all duration-300">
          <div class="relative h-56 overflow-hidden">
            <img src="../assets/images/wiboard.png" alt="Wiboard" class="w-full h-full object-cover object-top group-hover:scale-105 transition-transform duration-700" />
            <div class="absolute inset-0 bg-gradient-to-t from-[#0d0d0d] via-[#0d0d0d]/20 to-transparent"></div>
            <span class="absolute top-4 left-4 text-xs font-mono text-white/80 bg-black/50 backdrop-blur-md border border-white/10 px-3 py-1 rounded-full">04</span>
          </div>
          <div class="flex flex-col flex-1 p-6">
            <h3 class="text-xl font-semibold mb-2 group-hover:text-[#6823ff] transition-colors">Wiboard</h3>
            <p class="text-gray-400 text-sm leading-relaxed mb-5">An interactive dashboard system for visualizing collaborative data and managing user workflows.</p>
            <div class="flex flex-wrap gap-2 mb-6">
              <span class="text-[10px] uppercase tracking-wider text-[#6823ff] bg-[#6823ff]/10 border border-[#6823ff]/20 px-2.5 py-1 rounded-full">React.js</span>
              <span class="text-[10px] uppercase tracking-wider text-[#6823ff] bg-[#6823ff]/10 border border-[#6823ff]/20 px-2.5 py-1 rounded-full">API</span>
              <span class="text-[10px] uppercase tracking-wider text-[#6823ff] bg-[#6823ff]/10 border border-[#6823ff]/20 px-2.5 py-1 rounded-full">Tailwind</span>
            </div>
            <div class="mt-auto flex items-center gap-3">
              <a href="https://wiboard.vercel.app/" target="_blank" rel="noopener" class="inline-flex items-center gap-1.5 text-sm font-medium bg-[#6823ff] hover:bg-[#7d44ff] px-4 py-2 rounded-full transition-colors">Live Demo <span class="text-xs">↗</span></a>
              <a href="#" target="_blank" rel="noopener" class="text-sm text-gray-400 hover:text-white border border-white/10 hover:border-white/30 px-4 py-2 rounded-full transition-colors">GitHub</a>
            </div>
          </div>
        </article>

        <!-- 05 Vichea-Learn -->
        <article class="group flex flex-col bg-[#0d0d0d] border border-white/10 rounded-3xl overflow-hidden hover:border-[#6823ff]/70 hover:-translate-y-1 transition-all duration-300">
          <div class="relative h-56 overflow-hidden">
            <img src="../assets/images/vichea-learn.png" alt="Vichea-Learn" class="w-full h-full object-cover object-top group-hover:scale-105 transition-transform duration-700" />
            <div class="absolute inset-0 bg-gradient-to-t from-[#0d0d0d] via-[#0d0d0d]/20 to-transparent"></div>
            <span class="absolute top-4 left-4 text-xs font-mono text-white/80 bg-black/50 backdrop-blur-md border border-white/10 px-3 py-1 rounded-full">05</span>
          </div>
          <div class="flex flex-col flex-1 p-6">
            <h3 class="text-xl font-semibold mb-2 group-hover:text-[#6823ff] transition-colors">Vichea-Learn</h3>
            <p class="text-gray-400 text-sm leading-relaxed mb-5">An online learning platform designed for structured course delivery and intuitive student navigation.</p>
            <div class="flex flex-wrap gap-2 mb-6">
              <span class="text-[10px] uppercase tracking-wider text-[#6823ff] bg-[#6823ff]/10 border border-[#6823ff]/20 px-2.5 py-1 rounded-full">HTML</span>
              <span class="text-[10px] uppercase tracking-wider text-[#6823ff] bg-[#6823ff]/10 border border-[#6823ff]/20 px-2.5 py-1 rounded-full">Bootstrap</span>
              <span class="text-[10px] uppercase tracking-wider text-[#6823ff] bg-[#6823ff]/10 border border-[#6823ff]/20 px-2.5 py-1 rounded-full">JavaScript</span>
            </div>
            <div class="mt-auto flex items-center gap-3">
              <a href="https://vichea-learn.vercel.app/" target="_blank" rel="noopener" class="inline-flex items-center gap-1.5 text-sm font-medium bg-[#6823ff] hover:bg-[#7d44ff] px-4 py-2 rounded-full transition-colors">Live Demo <span class="text-xs">↗</span></a>
              <a href="#" target="_blank" rel="noopener" class="text-sm text-gray-400 hover:text-white border border-white/10 hover:border-white/30 px-4 py-2 rounded-full transition-colors">GitHub</a>
            </div>
          </div>
        </article>

      </div>
    </div>
  </section>
</template>