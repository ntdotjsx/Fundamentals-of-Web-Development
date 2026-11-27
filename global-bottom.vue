<script setup lang="ts">
import { computed } from 'vue'
import { useNav } from '@slidev/client'

const { currentPage, total, currentSlideRoute } = useNav()

const hideFooter = computed(() => {
  const fm = currentSlideRoute.value?.meta?.slide?.frontmatter as Record<string, unknown> | undefined
  return currentPage.value === 1 || Boolean(fm?.hideFooter)
})

const chapterLabel = computed(() => {
  const fm = currentSlideRoute.value?.meta?.slide?.frontmatter as Record<string, unknown> | undefined
  if (typeof fm?.chapter === 'string' && fm.chapter) return fm.chapter
  const filepath = currentSlideRoute.value?.meta?.slide?.filepath || ''
  const match = filepath.match(/(\d+)-day(\d+)/i)
  if (match) return `DAY ${match[2].padStart(2, '0')}`
  return '00 OVERVIEW'
})

const progress = computed(() => {
  if (!total.value) return 0
  return Math.round((currentPage.value / total.value) * 100)
})
</script>

<template>
  <footer
    v-if="!hideFooter"
    class="fixed bottom-4 left-14 right-14 z-20 flex items-center justify-between pointer-events-none select-none text-white/70"
  >
    <div class="flex items-center gap-2 text-[11px] font-medium tracking-wide">
      <carbon:cafe class="w-3.5 h-3.5 text-white/80" />
      <span>Mini Cafe Full-Stack</span>
      <span class="opacity-40">/</span>
      <span class="font-mono text-white/90">{{ chapterLabel }}</span>
    </div>

    <div class="flex items-center gap-3 text-[11px] font-mono">
      <div class="w-20 h-[2px] rounded-full bg-white/25 overflow-hidden">
        <div
          class="h-full bg-white transition-all duration-500"
          :style="{ width: `${progress}%` }"
        />
      </div>
      <span class="text-white/90">{{ String(currentPage).padStart(2, '0') }} / {{ String(total).padStart(2, '0') }}</span>
    </div>
  </footer>
</template>
