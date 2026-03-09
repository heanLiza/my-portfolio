<template>
  <section id="about" class="relative overflow-hidden px-6 pt-32 pb-24 md:pt-30 md:pb-32">
    <div
      class="pointer-events-none absolute -left-24 -top-10 h-[500px] w-[500px] rounded-full bg-purple-600/10 blur-[120px]"
    ></div>

    <div class="relative z-10 mx-auto max-w-7xl">
      <div class="grid items-center gap-12 lg:grid-cols-2 lg:gap-16">
        
        <div class="order-2 space-y-8 lg:order-1 text-center lg:text-left">
          <div
            class="inline-flex items-center gap-2 rounded-full border border-purple-500/20 bg-purple-500/10 px-4 py-1.5"
          >
            <span class="h-1.5 w-1.5 animate-pulse rounded-full bg-purple-500"></span>
            <span class="text-[10px] font-bold uppercase tracking-[0.2em] text-purple-400">
              Frontend Architect
            </span>
          </div>

          <h1 class="text-5xl font-bold leading-[1.1] tracking-tighter text-white md:text-7xl lg:text-8xl">
            I'm
            <span class="bg-gradient-to-r from-purple-400 to-indigo-400 bg-clip-text text-transparent">
              Liza
            </span><span class="text-purple-400">.</span><br />
            <span class="opacity-90">Frontend Developer</span>
          </h1>

          <p class="mx-auto lg:mx-0 max-w-xl text-lg leading-relaxed text-gray-400 md:text-xl">
            I specialize in the intersection of design and performance, building 
            modern interfaces that are visually stunning and technically optimized.
          </p>
        <div class="flex flex-wrap justify-center lg:justify-start gap-5 pt-4">
            <NuxtLink
              to="/#projects"
              class="group relative inline-flex items-center justify-center overflow-hidden 
                    rounded-2xl bg-[#6823ff] px-10 py-4 font-bold text-white 
                    transition-all duration-300 ease-out
                    hover:scale-105 active:scale-95
                    shadow-[0_0_20px_rgba(109,40,217,0.4)] 
                    hover:shadow-[0_0_35px_rgba(109,40,217,0.7)]"
            >
              <span class="relative z-10">Explore Work</span>
              
              <div 
                class="absolute inset-0 -z-10 bg-gradient-to-br from-[#7c3aed] via-[#6d28d9] to-[#5b21b6] 
                      opacity-0 group-hover:opacity-100 transition-opacity duration-300"
              ></div>
            </NuxtLink>

            <button
              class="rounded-2xl border border-white/10 bg-white/5 px-10 py-4 font-bold text-white 
                    transition-all duration-300 hover:bg-white/10 hover:border-white/20 
                    hover:scale-105 active:scale-95"
            >
              Download CV
            </button>
          </div>
          <div class="flex flex-wrap justify-center lg:justify-start gap-6 pt-12 opacity-30 grayscale hover:grayscale-0 transition-all duration-500">
            <span class="text-sm font-black tracking-widest text-white"># NUXT3</span>
            <span class="text-sm font-black tracking-widest text-white"># VUE3</span>
            <span class="text-sm font-black tracking-widest text-white"># TAILWIND</span>
            <span class="text-sm font-black tracking-widest text-white"># LARAVEL</span>
          </div>
        </div>

        <div class="relative order-1 flex justify-center lg:order-2">
          <div
            class="absolute -right-2 -top-2 z-20 flex h-28 w-28 items-center justify-center rounded-full border-[6px] border-[#0a0c10]  bg-[#6823ff]  shadow-2xl shadow-purple-500/40 md:-right-6 md:h-32 md:w-32"
          >
            <p class="text-center text-[10px] font-black leading-tight text-white uppercase tracking-tighter">
              Hire Me<br />Hire Me<br />Hire Me
            </p>
          </div>

          <div
            class="relative aspect-[4/5] w-full max-w-[340px] overflow-hidden rounded-[3rem] border border-white/10 bg-[#0d1117]/50 shadow-2xl backdrop-blur-sm md:max-w-[420px]"
          >
            <img
              src="@/assets/images/liza.png"
              alt="Hean Liza"
              class="h-full w-full object-cover transition-transform duration-700 hover:scale-110"
            />
            <div class="absolute inset-0 bg-gradient-to-t from-[#0a0c10]/80 via-transparent to-transparent"></div>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>