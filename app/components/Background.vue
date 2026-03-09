<template>
  <div
    class="relative min-h-screen overflow-hidden bg-[#020617]"
    style="
      background: 
        radial-gradient(circle at 20% 30%, rgba(29, 38, 113, 0.3) 0%, transparent 50%),
        radial-gradient(circle at 80% 70%, rgba(45, 27, 105, 0.2) 0%, transparent 50%),
        linear-gradient(180deg, #020617 0%, #080c14 100%);
    "
  >
    <div class="pointer-events-none absolute inset-0">
      <div
        v-for="star in stars"
        :key="star.id"
        class="star-slow absolute rounded-full bg-white/80"
        :style="{
          width: star.size + 'px',
          height: star.size + 'px',
          top: star.top + '%',
          left: star.left + '%',
          opacity: star.opacity,
          animationDuration: star.duration + 's',
          animationDelay: star.delay + 's',
        }"
      />
    </div>

    <div class="relative z-10">
      <slot />
    </div>
  </div>
</template>

<script setup lang="ts">
const stars = Array.from({ length: 100 }, (_, i) => ({
  id: i,
  size: Math.random() * 1.5 + 0.5,
  top: Math.random() * 100,
  left: Math.random() * 100,
  opacity: Math.random() * 0.5 + 0.1, 
  duration: Math.random() * 10 + 10,  
  delay: Math.random() * -100,       
}))
</script>

<style scoped>
.star-slow {
  animation: slowWalk linear infinite;
  will-change: transform;
}

@keyframes slowWalk {
  0% {
    transform: translateY(0);
  }
  100% {
    transform: translateY(-100px);
  }
}
</style>