<script setup lang="ts">
import { computed, ref, watch } from 'vue'

const props = defineProps<{
  step: number
}>()

const manualStep = ref<number | null>(null)

watch(
  () => props.step,
  () => {
    manualStep.value = null
  },
)

const activeStep = computed(() => (manualStep.value !== null ? manualStep.value : props.step))

const hasHtml = computed(() => activeStep.value >= 1)
const hasCss = computed(() => activeStep.value >= 2)
const hasJs = computed(() => activeStep.value >= 3)
const hasBackend = computed(() => activeStep.value >= 4)

const caption = computed(() => {
  if (activeStep.value === 0) return 'กด Space หรือคลิกแท็บด้านบนเพื่อประกอบบ้านทีละชั้น'
  if (activeStep.value === 1) return '01 / HTML5 — โครงสร้าง เสา และกำแพง'
  if (activeStep.value === 2) return '02 / CSS3 — ทาสี ตกแต่งหน้าร้านให้สวยงาม'
  if (activeStep.value === 3) return '03 / JavaScript — เดินไฟ ป้ายเปิดร้าน และระบบโต้ตอบ'
  return '04 / PHP + MariaDB — ห้องครัวและคลังเก็บออเดอร์ถาวร'
})

function selectLayer(n: number) {
  manualStep.value = manualStep.value === n ? null : n
}
</script>

<template>
  <div class="thin-glass p-5 flex flex-col justify-between h-full">
    <div class="flex items-center justify-between gap-2">
      <span class="font-mono text-[11px] font-semibold tracking-widest text-white/70 uppercase">
        Interactive Blueprint
      </span>
      <div class="flex gap-1.5">
        <button
          v-for="(label, idx) in ['HTML', 'CSS', 'JS', 'DB']"
          :key="label"
          @click="selectLayer(idx + 1)"
          class="font-mono text-[11px] font-bold px-2.5 py-0.5 rounded-full transition-all cursor-pointer border"
          :class="
            activeStep >= idx + 1
              ? 'bg-white text-indigo-950 border-white shadow-sm'
              : 'bg-white/10 text-white/75 border-white/20 hover:bg-white/20'
          "
        >
          {{ label }}
        </button>
      </div>
    </div>

    <div class="flex-1 flex items-center justify-center my-1">
      <svg viewBox="0 0 380 220" class="w-full max-w-[385px] h-auto select-none overflow-visible">
        <defs>
          <linearGradient id="roofGrad" x1="0%" y1="0%" x2="100%" y2="100%">
            <stop offset="0%" stop-color="#fb923c" />
            <stop offset="100%" stop-color="#f472b6" />
          </linearGradient>
          <linearGradient id="wallGrad" x1="0%" y1="0%" x2="0%" y2="100%">
            <stop offset="0%" stop-color="#fff7ed" />
            <stop offset="100%" stop-color="#ffedd5" />
          </linearGradient>
          <linearGradient id="winGlow" x1="0%" y1="0%" x2="0%" y2="100%">
            <stop offset="0%" stop-color="#fef08a" />
            <stop offset="100%" stop-color="#facc15" />
          </linearGradient>
          <linearGradient id="dbGrad" x1="0%" y1="0%" x2="100%" y2="0%">
            <stop offset="0%" stop-color="#818cf8" />
            <stop offset="100%" stop-color="#38bdf8" />
          </linearGradient>
        </defs>

        <!-- Minimal Ground Hairline -->
        <line x1="16" y1="204" x2="364" y2="204" stroke="rgba(255,255,255,0.45)" stroke-width="2" stroke-linecap="round" />

        <!-- LAYER 2: CSS Paint & Decor -->
        <g class="transition-all duration-700" :style="{ opacity: hasCss ? 1 : 0 }">
          <rect x="44" y="88" width="168" height="116" rx="6" fill="url(#wallGrad)" />
          <polygon points="28,92 128,24 228,92" fill="url(#roofGrad)" />
          <path d="M 56 130 L 116 130 L 110 144 L 62 144 Z" fill="#8b5cf6" />
          <path d="M 68 130 L 80 130 L 77 144 L 68 144 Z" fill="#ffffff" opacity="0.9" />
          <path d="M 92 130 L 104 130 L 101 144 L 92 144 Z" fill="#ffffff" opacity="0.9" />
          <rect x="142" y="134" width="44" height="70" rx="5" fill="#4f46e5" />
          <rect x="64" y="144" width="44" height="36" rx="4" fill="#bae6fd" />
          <rect x="24" y="184" width="14" height="20" rx="2" fill="#f97316" />
          <circle cx="31" cy="177" r="9" fill="#34d399" />
        </g>

        <!-- LAYER 1: HTML Wireframe Structure -->
        <g
          class="transition-all duration-700"
          :style="{
            opacity: hasHtml ? 1 : 0.35,
            transform: hasHtml ? 'translateY(0)' : 'translateY(6px)',
          }"
        >
          <rect
            x="44"
            y="88"
            width="168"
            height="116"
            rx="6"
            fill="none"
            :stroke="hasCss ? '#1e1b4b' : '#ffffff'"
            stroke-width="2.4"
            :stroke-dasharray="hasHtml ? 'none' : '6 6'"
          />
          <polygon
            points="28,92 128,24 228,92"
            fill="none"
            :stroke="hasCss ? '#1e1b4b' : '#ffffff'"
            stroke-width="2.4"
            stroke-linejoin="round"
            :stroke-dasharray="hasHtml ? 'none' : '6 6'"
          />
          <rect
            x="142"
            y="134"
            width="44"
            height="70"
            rx="4"
            fill="none"
            :stroke="hasCss ? '#1e1b4b' : '#ffffff'"
            stroke-width="2"
          />
          <rect
            x="64"
            y="144"
            width="44"
            height="36"
            rx="4"
            fill="none"
            :stroke="hasCss ? '#1e1b4b' : '#ffffff'"
            stroke-width="2"
          />
          <line x1="86" y1="144" x2="86" y2="180" :stroke="hasCss ? '#1e1b4b' : '#ffffff'" stroke-width="1.5" />
          <circle cx="128" cy="64" r="11" :fill="hasCss ? '#ffffff' : 'none'" :stroke="hasCss ? '#1e1b4b' : '#ffffff'" stroke-width="2" />
        </g>

        <!-- LAYER 3: JavaScript Lights & Interactivity -->
        <g class="transition-all duration-700" :style="{ opacity: hasJs ? 1 : 0 }">
          <rect x="66" y="146" width="40" height="32" rx="3" fill="url(#winGlow)" opacity="0.95" />
          <line x1="86" y1="146" x2="86" y2="178" stroke="#1e1b4b" stroke-width="1.5" />
          <circle cx="128" cy="64" r="8.5" fill="#fde047" />
          <circle cx="195" cy="166" r="4.5" fill="#fbbf24" />
          <circle cx="195" cy="166" r="10" fill="none" stroke="#fde047" stroke-width="1.8" opacity="0.8" />
          <rect x="64" y="102" width="52" height="20" rx="6" fill="#0f172a" />
          <text
            x="90"
            y="115.5"
            text-anchor="middle"
            fill="#fde047"
            style="font-size: 10px; font-weight: 700; letter-spacing: 0.08em;"
          >
            OPEN
          </text>
          <circle cx="151" cy="170" r="3" fill="#fde047" />
        </g>

        <!-- LAYER 4: PHP + MariaDB Backend -->
        <g
          class="transition-all duration-700"
          :style="{
            opacity: hasBackend ? 1 : 0,
            transform: hasBackend ? 'translateX(0)' : 'translateX(12px)',
          }"
        >
          <path d="M 212 158 L 254 158" stroke="#ffffff" stroke-width="2.5" fill="none" class="animate-dash" />
          <polygon points="252,153 262,158 252,163" fill="#ffffff" />

          <rect
            x="264"
            y="88"
            width="96"
            height="116"
            rx="14"
            fill="rgba(15, 23, 42, 0.72)"
            stroke="rgba(255,255,255,0.45)"
            stroke-width="1.8"
          />
          <text
            x="312"
            y="108"
            text-anchor="middle"
            fill="#e0e7ff"
            style="font-size: 10px; font-weight: 700; letter-spacing: 0.06em;"
          >
            BACKEND
          </text>

          <rect x="278" y="117" width="68" height="23" rx="6" fill="rgba(255,255,255,0.14)" stroke="rgba(255,255,255,0.35)" />
          <text
            x="312"
            y="132"
            text-anchor="middle"
            fill="#ffffff"
            style="font-size: 10.5px; font-weight: 700;"
          >
            PHP 8.3
          </text>

          <line x1="312" y1="141" x2="312" y2="154" stroke="#a5b4fc" stroke-width="2" class="animate-dash" />

          <ellipse cx="312" cy="162" rx="28" ry="7.5" fill="#93c5fd" />
          <path d="M 284 162 L 284 187 A 28 7.5 0 0 0 340 187 L 340 162" fill="url(#dbGrad)" />
          <ellipse cx="312" cy="162" rx="28" ry="7.5" fill="#bfdbfe" />
          <text
            x="312"
            y="182"
            text-anchor="middle"
            fill="#ffffff"
            style="font-size: 9.5px; font-weight: 700;"
          >
            MariaDB
          </text>
        </g>
      </svg>
    </div>

    <div class="text-center text-[13.5px] font-medium text-white/90 pt-2 border-t border-white/15">
      {{ caption }}
    </div>
  </div>
</template>
