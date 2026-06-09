<template>
  <div :class="tier.featured ? 'border-2 border-blue-600/50 bg-gradient-to-b from-[#091022] to-[#030712] shadow-xl shadow-blue-950/10' : 'border border-slate-900 bg-slate-950/20'"
       class="p-6 sm:p-8 rounded-2xl flex flex-col justify-between relative space-y-6 sm:space-y-8 transition duration-300 hover:border-slate-800">
    
    <div v-if="tier.featured" class="absolute -top-3 left-6 bg-blue-600 text-[9px] font-bold uppercase tracking-widest text-white px-2.5 py-0.5 rounded-full">
      Most Requested
    </div>

    <div class="space-y-4">
      <div class="flex flex-row justify-between items-baseline gap-2">
        <h3 class="text-xs sm:text-sm font-bold text-white uppercase tracking-wider">{{ tier.name }}</h3>
        <div class="text-lg sm:text-xl font-normal text-white tracking-tight shrink-0">{{ tier.price }}</div>
      </div>
      <p class="text-xs text-slate-400 font-light leading-relaxed">{{ tier.desc }}</p>
      
      <hr class="border-slate-900" />
      
      <ul class="space-y-3 pt-2">
        <li v-for="feature in tier.features" :key="feature" class="text-xs text-slate-400 flex items-start gap-2.5 font-light leading-tight">
          <span class="text-blue-500 text-xs select-none">✓</span>
          <span>{{ feature }}</span>
        </li>
      </ul>
    </div>

    <a href="#connect" 
       :class="tier.featured ? 'bg-white hover:bg-slate-200 text-black font-semibold' : 'bg-slate-900 hover:bg-slate-800 text-slate-300 border border-slate-800'"
       class="w-full text-center text-xs py-3 rounded-xl transition shadow-sm block tracking-wide">
      {{ tier.cta }}
    </a>
  </div>
</template>

<script setup>
defineProps({
  tier: { type: Object, required: true }
})
</script>