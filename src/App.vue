<script setup>
import AppNavbar from './components/layout/AppNavbar.vue'
import HeroSection from './components/sections/HeroSection.vue'
import ServicesSection from './components/sections/ServicesSection.vue'
import AboutSection from './components/sections/AboutSection.vue'
import ProjectsSection from './components/sections/ProjectsSection.vue'
import TechStackSection from './components/sections/TechStackSection.vue'
import PricingSection from './components/sections/PricingSection.vue'
import TestimonialsSection from './components/sections/TestimonialsSection.vue'
import ContactSection from './components/sections/ContactSection.vue'
import AppFooter from './components/layout/AppFooter.vue'
</script>

<template>
  <div class="app-container">
    <AppNavbar />
    <main>
      <HeroSection />
      <ServicesSection />
      <AboutSection />
      <ProjectsSection />
      <TechStackSection />
      <PricingSection />
      <TestimonialsSection />
      <ContactSection />
    </main>
    <AppFooter />
  </div>
</template>

<style>
/* Global smoothing */
html {
  scroll-behavior: smooth;
}

.app-container {
  overflow-x: hidden;
}
</style>
