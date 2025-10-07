<template>
  <div class="min-h-screen bg-slate-950 text-slate-100">
    <div class="relative overflow-hidden">
      <div class="absolute inset-x-0 top-0 h-[640px] bg-gradient-to-b from-primary-500/20 via-primary-500/5 to-transparent"></div>
      <div class="absolute inset-x-0 top-0 h-[640px] bg-grid-pattern opacity-20"></div>
      <div class="relative">
        <HeroHeader />
        <HeroSection />
      </div>
    </div>
    <main class="relative z-10 space-y-24 pb-24">
      <StatsSection />
      <ServicesSection />
      <ProcessTimeline />
      <PricingSection />
      <TestimonialSection />
      <CTASection />
    </main>
    <FooterSection />
  </div>
</template>

<script setup>
import HeroHeader from './components/HeroHeader.vue';
import HeroSection from './components/HeroSection.vue';
import StatsSection from './components/StatsSection.vue';
import ServicesSection from './components/ServicesSection.vue';
import ProcessTimeline from './components/ProcessTimeline.vue';
import PricingSection from './components/PricingSection.vue';
import TestimonialSection from './components/TestimonialSection.vue';
import CTASection from './components/CTASection.vue';
import FooterSection from './components/FooterSection.vue';
</script>
