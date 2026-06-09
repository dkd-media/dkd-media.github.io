<template>
  <div class="group relative flex flex-col justify-between space-y-4 p-6 border border-slate-900 bg-slate-950/20 rounded-2xl transition-all duration-300 hover:border-blue-500/30 hover:bg-slate-950/50">
    <div class="space-y-3">
      <!-- Tag/Pill -->
      <div class="inline-block text-[9px] font-bold uppercase tracking-widest text-blue-400 border border-blue-500/20 bg-blue-500/5 px-2.5 py-0.5 rounded-full">
        Phase {{ index + 1 }}
      </div>
      <!-- Title -->
      <h3 class="text-lg font-normal text-white tracking-tight flex items-center gap-2">
        {{ title }}
      </h3>
      <!-- Description -->
      <p class="text-xs text-slate-400 leading-relaxed font-light">
        {{ desc }}
      </p>
    </div>

    <!-- Core focus bullet points -->
    <ul class="space-y-2 pt-2 border-t border-slate-900/60">
      <li v-for="item in points" :key="item" class="text-[11px] text-slate-400 flex items-start gap-2 leading-tight">
        <span class="text-blue-500 text-xs select-none">✓</span>
        <span>{{ item }}</span>
      </li>
    </ul>
  </div>
</template>

<script setup>
defineProps({
  title: { type: String, required: true },
  desc: { type: String, required: true },
  points: { type: Array, required: true },
  index: { type: Number, required: true }
})
</script>