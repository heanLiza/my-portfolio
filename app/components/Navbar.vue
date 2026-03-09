<template>
  <nav
    class="fixed top-6 left-1/2 -translate-x-1/2 z-50 
           w-[92%] max-w-5xl 
           rounded-full 
           border border-white/10 
           bg-[#0a0c10]/80 
           backdrop-blur-xl
           shadow-[0_8px_32px_rgba(0,0,0,0.5)]"
    >
    <div class="absolute inset-0 rounded-full border-t border-white/20 pointer-events-none"></div>

    <div class="flex items-center justify-between px-8 py-3.5">
      
      <NuxtLink to="/" class="flex items-center gap-3 group">
        <div class="w-2 h-6 bg-[#6823ff] rounded-full shadow-[0_0_15px_rgba(104,35,255,0.6)] group-hover:bg-[#8552ff] transition-colors"></div>
        <span class="text-white font-bold text-lg tracking-tight">Hean Liza</span>
      </NuxtLink>

      <ul class="hidden lg:flex items-center gap-10 text-[15px] font-medium text-gray-400">
        <li><NuxtLink to="/#about" class="hover:text-white transition-colors">About</NuxtLink></li>
        <li><NuxtLink to="/#skills" class="hover:text-white transition-colors">Skills</NuxtLink></li>
        <li><NuxtLink to="/#skills" class="hover:text-white transition-colors">Education</NuxtLink></li>
        <li><NuxtLink to="/#projects" class="hover:text-white transition-colors">Projects</NuxtLink></li>
        <li><NuxtLink to="/#contact" class="hover:text-white transition-colors">Contact</NuxtLink></li>
      </ul>

      <NuxtLink
        to="/#contact"
        class="hidden md:inline-flex px-7 py-2.5 rounded-full text-[15px] font-semibold text-white 
               bg-white/5 border border-white/20 
               hover:bg-white/10 hover:border-white/40 
               transition-all duration-300 ease-in-out">
        Hire Me
      </NuxtLink>

      <button class="lg:hidden text-white" @click="isOpen = !isOpen">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path v-if="!isOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 12h16m-7-6h7m-7 12h7" />
          <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>
    </div>

    <div v-if="isOpen" class="lg:hidden px-8 pb-8 flex flex-col gap-5 text-base font-medium text-gray-300 border-t border-white/5 mt-1 pt-5">
      <NuxtLink to="/#about" @click="closeMenu" class="hover:text-white">About</NuxtLink>
      <NuxtLink to="/#skills" @click="closeMenu" class="hover:text-white">Skills</NuxtLink>
      <NuxtLink to="/#projects" @click="closeMenu" class="hover:text-white">Projects</NuxtLink>
      <NuxtLink to="/#contact" @click="closeMenu" class="text-[#8552ff] font-bold">Contact</NuxtLink>
    </div>
  </nav>
</template>