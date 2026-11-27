<script setup lang="ts">
defineProps<{
  logo: string
  name: string
  days: string
  role: string
  badgeClass?: string
  floatDelay?: string
}>()
</script>

<template>
  <div
    class="glass-card p-4 h-full flex flex-col justify-between gap-2.5 hover:-translate-y-0.5 hover:shadow-lg transition-all duration-300"
  >
    <div class="flex items-center justify-between gap-2">
      <div
        class="w-11 h-11 shrink-0 rounded-xl bg-white/95 border border-white shadow-sm flex items-center justify-center p-2 animate-float"
        :style="{ animationDelay: floatDelay || '0s' }"
      >
        <img :src="logo" :alt="name" class="w-full h-full object-contain" />
      </div>
      <span
        class="shrink-0 text-xs font-bold px-2.5 py-0.5 rounded-full"
        :class="badgeClass || 'bg-indigo-50 text-indigo-700'"
      >
        {{ days }}
      </span>
    </div>

    <div>
      <h3 class="!text-[16.5px] font-bold text-indigo-950 mb-1 m-0 leading-tight">{{ name }}</h3>
      <p class="text-[13.5px] text-slate-700 leading-snug m-0">{{ role }}</p>
    </div>
  </div>
</template>
