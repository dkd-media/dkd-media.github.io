<template>
  <div class="min-h-screen bg-[#030712] text-slate-200 font-sans antialiased selection:bg-blue-500/30 selection:text-blue-200 overflow-x-hidden">
    
    <!-- Ambient Glow Top Background Layer -->
    <div class="absolute top-0 left-1/2 -translate-x-1/2 w-full max-w-7xl h-[400px] sm:h-[600px] pointer-events-none overflow-hidden z-0">
      <div class="absolute -top-[200px] sm:-top-[250px] left-1/2 -translate-x-1/2 w-[500px] sm:w-[800px] h-[350px] sm:h-[500px] bg-gradient-to-b from-blue-600/10 to-transparent blur-[80px] sm:blur-[120px] rounded-full"></div>
    </div>

    <HeaderNavigation />

    <!-- Hero Section: Presenting the core identity from the logo guidelines -->
    <section class="relative z-10 max-w-5xl mx-auto px-4 sm:px-6 pt-16 sm:pt-24 pb-16 sm:pb-20 text-center space-y-6 sm:space-y-8">
      <div class="inline-flex items-center gap-2 border border-blue-500/20 bg-blue-500/5 text-[10px] sm:text-[11px] font-semibold uppercase tracking-widest text-blue-400 px-3 py-1 rounded-full">
        <span class="w-1.5 h-1.5 bg-blue-500 rounded-full animate-pulse"></span> Booking ambitious brand launches and digital rescues now
      </div>
      
      <h1 class="text-4xl sm:text-6xl md:text-7xl font-normal tracking-tight text-white max-w-4xl mx-auto leading-[1.1] sm:leading-[1.05]">
        We build standout brand experiences. <br class="hidden sm:inline" />
        <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-400 via-blue-500 to-indigo-400 font-medium">
          We grow attention, momentum, and digital resilience.
        </span>
      </h1>
      
      <p class="text-xs sm:text-base md:text-lg text-slate-400 max-w-2xl mx-auto font-light leading-relaxed px-2">
        From launch-ready brand destinations to performance upgrades and emergency site rescues, we help brands reclaim momentum, convert attention, and sustain growth through high-impact digital experiences.
      </p>

      <div class="flex flex-col xs:flex-row justify-center items-center gap-3 sm:gap-4 pt-2 max-w-xs xs:max-w-none mx-auto w-full xs:w-auto">
        <a href="#connect" class="w-full xs:w-auto bg-white hover:bg-slate-200 text-black text-xs font-semibold px-6 py-3.5 rounded-full transition tracking-wide shadow-lg shadow-white/5 text-center">
          Book a Brand Audit
        </a>
        <a href="#solutions" class="text-slate-400 hover:text-white text-xs font-medium transition flex items-center justify-center gap-1.5 group py-2">
          Explore our service tracks <span class="transform group-hover:translate-x-1 transition duration-200">→</span>
        </a>
      </div>
    </section>

    <hr class="border-slate-900 max-w-6xl mx-auto px-4 sm:px-6" />

    <!-- Core Solutions Framework Section -->
    <section id="solutions" class="relative z-10 max-w-6xl mx-auto px-4 sm:px-6 py-16 sm:py-24 space-y-12 sm:space-y-16">
      <div class="max-w-xl space-y-2 sm:space-y-3">
        <h2 class="text-xs font-semibold uppercase tracking-widest text-blue-500">Our Capabilities</h2>
        <p class="text-xl sm:text-2xl text-white font-light tracking-tight">Three service tracks to launch, scale, and rescue your digital brand.</p>
      </div>

      <!-- Core Pillars Layout Matrix (Build, Grow, Rescue) -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6 lg:gap-8">
        <CapabilityCard 
          v-for="(sol, index) in solutions" 
          :key="sol.title" 
          :title="sol.title" 
          :desc="sol.desc" 
          :points="sol.points"
          :index="index"
        />
      </div>
    </section>

    <!-- Deep-Dive Focus Case Study: The Rescue Theme -->
    <section id="proof" class="relative z-10 bg-gradient-to-b from-transparent via-slate-950/40 to-transparent py-16 sm:py-20 border-y border-slate-900">
      <div class="max-w-6xl mx-auto px-4 sm:px-6 grid grid-cols-1 lg:grid-cols-12 gap-8 lg:gap-12 items-center">
        
        <div class="lg:col-span-7 space-y-4 sm:space-y-6">
          <div class="text-xs font-semibold uppercase tracking-widest text-slate-500">Case Study / Digital Rescue</div>
          <h3 class="text-xl sm:text-3xl text-white font-light tracking-tight leading-snug">
            Turning a broken brand presence into a growth engine.
          </h3>
          <p class="text-xs sm:text-sm text-slate-400 leading-relaxed font-light">
            A once-promising brand site was trapped in outdated architecture, sluggish pages, and broken customer journeys. We moved in quickly, rebuilt the experience, removed the friction, and relaunched the brand on a platform designed to convert.
          </p>
          <p class="text-xs sm:text-sm text-slate-500 leading-relaxed font-light">
            The result was a stable, polished online presence that performs like a modern growth machine.
          </p>
        </div>

        <div class="lg:col-span-5 grid grid-cols-1 xs:grid-cols-2 gap-4 pt-4 lg:pt-0">
          <div class="border border-slate-900 bg-[#070b14] p-5 sm:p-6 rounded-2xl text-center space-y-1">
            <div class="text-2xl sm:text-3xl font-light text-white tracking-tight">98%</div>
            <div class="text-[9px] sm:text-[10px] font-semibold uppercase tracking-widest text-slate-500">Lighthouse Score Achieved</div>
          </div>
          <div class="border border-slate-900 bg-[#070b14] p-5 sm:p-6 rounded-2xl text-center space-y-1">
            <div class="text-2xl sm:text-3xl font-light text-blue-400 tracking-tight">-5.1s</div>
            <div class="text-[9px] sm:text-[10px] font-semibold uppercase tracking-widest text-slate-500">Load Speed Reduction</div>
          </div>
        </div>

      </div>
    </section>

    <!-- Project Engagements / Pricing Tiers -->
    <section id="pricing" class="relative z-10 max-w-6xl mx-auto px-4 sm:px-6 py-16 sm:py-24 space-y-12 sm:space-y-16">
      <div class="text-center space-y-2 sm:space-y-3 max-w-xl mx-auto">
        <h2 class="text-xs font-semibold uppercase tracking-widest text-blue-500">How We Partner</h2>
        <p class="text-xl sm:text-2xl text-white font-light tracking-tight">Flexible engagement paths built for launches, growth, and urgent rescues.</p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-4xl mx-auto">
        <PricingCard 
          v-for="tier in pricingTiers" 
          :key="tier.name" 
          :tier="tier" 
        />
      </div>
    </section>

    <!-- Dynamic Context Contact Form Integration -->
    <section id="connect" class="relative z-10 max-w-xl mx-auto px-4 sm:px-6 pb-24 sm:pb-32 pt-8 space-y-6 sm:space-y-8">
      <div class="text-center space-y-2">
        <h2 class="text-xs font-semibold uppercase tracking-widest text-blue-500">Ready to revive your digital presence?</h2>
        <p class="text-xl text-white font-light tracking-tight">Share your current challenges so we can match the right team and timeline.</p>
      </div>

      <form @submit.prevent="handleSubmit" class="space-y-4 border border-slate-900 bg-slate-950/40 p-5 sm:p-6 rounded-2xl backdrop-blur-sm">
        <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
          <div class="space-y-1.5">
            <label class="text-[9px] sm:text-[10px] font-bold uppercase tracking-wider text-slate-400">Your Name</label>
            <input type="text" v-model="form.name" required class="w-full bg-[#090f1e] border border-slate-800 rounded-xl px-4 py-3 text-xs text-white focus:outline-none focus:border-blue-500 transition" placeholder="Alex" />
          </div>
          <div class="space-y-1.5">
            <label class="text-[9px] sm:text-[10px] font-bold uppercase tracking-wider text-slate-400">Email Address</label>
            <input type="email" v-model="form.email" required class="w-full bg-[#090f1e] border border-slate-800 rounded-xl px-4 py-3 text-xs text-white focus:outline-none focus:border-blue-500 transition" placeholder="alex@company.com" />
          </div>
        </div>
        
        <div class="space-y-1.5">
          <label class="text-[9px] sm:text-[10px] font-bold uppercase tracking-wider text-slate-400">What kind of project do you need?</label>
          <div class="relative">
            <select v-model="form.type" class="w-full bg-[#090f1e] border border-slate-800 rounded-xl px-4 py-3 text-xs text-slate-300 focus:outline-none focus:border-blue-500 transition appearance-none">
              <option value="build">We build: custom brand site or campaign platform</option>
              <option value="grow">We grow: optimize performance, conversion, and engagement</option>
              <option value="rescue">We rescue: repair broken systems and reclaim momentum</option>
            </select>
            <div class="pointer-events-none absolute inset-y-0 right-0 flex items-center px-4 text-slate-500 text-xs">▼</div>
          </div>
        </div>

        <div class="space-y-1.5">
          <label class="text-[9px] sm:text-[10px] font-bold uppercase tracking-wider text-slate-400">Project Specifics</label>
          <textarea v-model="form.details" rows="4" required class="w-full bg-[#090f1e] border border-slate-800 rounded-xl px-4 py-3 text-xs text-white focus:outline-none focus:border-blue-500 transition resize-none" placeholder="Share your brand story, current website challenges, and what success looks like for this project."></textarea>
        </div>

        <button type="submit" class="w-full bg-white hover:bg-slate-200 text-black text-xs font-semibold py-3.5 rounded-xl transition uppercase tracking-widest mt-2 shadow-sm">
          Send Project Brief
        </button>
      </form>
    </section>

    <!-- Footer Block matching tagline structure -->
    <footer class="relative z-10 border-t border-slate-950 bg-[#02050c] py-8 text-center text-[10px] sm:text-[11px] text-slate-600 tracking-wide px-4">
      <div>&copy; 2026 DKD Media. Brand growth, digital rescue, and media momentum.</div>
    </footer>

  </div>
</template>

<script setup>
import { ref } from 'vue'
import HeaderNavigation from '../components/HeaderNavigation.vue'
import CapabilityCard from '../components/CapabilityCard.vue'
import PricingCard from '../components/PricingCard.vue'

const form = ref({
  name: '',
  email: '',
  type: 'build',
  details: ''
})

const handleSubmit = () => {
  alert(`Thanks, ${form.value.name}. Your brief is received and our team will follow up with a priority plan.`)
  form.value = { name: '', email: '', type: 'build', details: '' }
}

// Aligned explicitly with the exact pillars of the slogan update
const solutions = [
  {
    title: 'We Build',
    desc: 'Designing bold brand experiences and custom digital platforms that move fast, look sharp, and convert reliably from day one.',
    points: [
      'Brand-led product and campaign experiences',
      'Conversion-first interface design',
      'Modular, scalable systems for future growth'
    ]
  },
  {
    title: 'We Grow',
    desc: 'Accelerating your live website with growth-focused performance, conversion, and engagement strategies that turn visitors into loyal customers.',
    points: [
      'Conversion roadmap and CRO optimization',
      'Performance lift and speed tuning',
      'Growth-ready feature rollouts'
    ]
  },
  {
    title: 'We Rescue',
    desc: 'Stepping into damaged or outdated online systems, stabilizing them fast, then rebuilding trust with clean code and a better brand experience.',
    points: [
      'Emergency performance and stability triage',
      'Legacy system rescue and modernization',
      'Stabilize, polish, and relaunch with confidence'
    ]
  }
]

const pricingTiers = [
  {
    name: 'Rapid Rescue Sprint',
    price: '$250',
    featured: false,
    desc: 'Fast emergency work for immediate site recovery, performance rescue, or quick growth improvements.',
    features: [
      'Rapid audit with action plan',
      'One urgent system fix or redesign recommendation',
      'Fast execution window',
      'Safety and launch verification'
    ],
    cta: 'Start Rescue Sprint'
  },
  {
    name: 'Brand Growth & Build',
    price: 'Custom',
    featured: true,
    desc: 'End-to-end launches, full rebuilds, and marketing-ready platforms designed for sustainable audience growth.',
    features: [
      'Discovery and brand positioning',
      'Custom digital product development',
      'Holistic growth strategy',
      'Ongoing launch support'
    ],
    cta: 'Start Growth Strategy'
  }
]
</script>