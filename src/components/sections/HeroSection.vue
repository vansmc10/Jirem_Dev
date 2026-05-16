<script setup>
import heroImage from '../../assets/images/fondo_jiremdev.png'
</script>

<template>
  <section id="home" class="hero-section" :style="{ backgroundImage: `url(${heroImage})` }">
    <!-- Sophisticated Overlay Gradient -->
    <div class="hero-overlay"></div>
    
    <div class="container hero-container d-flex align-items-center justify-content-center">
      <div class="hero-glass-card">
        <div class="text-center">
          <h1 class="display-2 fw-bold mb-4">
            <span class="text-accent">Transformación</span> Digital Para Tu Negocio
          </h1>
          <p class="lead mb-5 hero-lead mx-auto">
            Ofrecemos consultoría estratégica e ingeniería de software especializada para ayudar a su empresa a crecer y prosperar en la era digital.
          </p>
          <div class="d-flex flex-column flex-sm-row gap-4 justify-content-center">
            <a href="#contact" class="btn btn-primary btn-lg">
              Empezar <span class="material-icons align-middle ms-1">arrow_forward</span>
            </a>
            <a href="#services" class="btn btn-outline-futuristic btn-lg">
              Nuestros Servicios
            </a>
          </div>
        </div>
      </div>
    </div>
    
    <!-- Background cleanup: Removed floating glows -->
  </section>
</template>

<style scoped>
.hero-section {
  position: relative;
  min-height: 100svh;
  width: 100%;
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  display: flex;
  overflow: hidden;
}

.hero-overlay {
  position: absolute;
  inset: 0;
  /* Multi-layered gradient for depth and readability */
  background: linear-gradient(135deg, rgba(0,0,0,0.7) 0%, rgba(0,0,0,0.3) 50%, rgba(0,0,0,0.7) 100%);
  z-index: 1;
}

.hero-container {
  position: relative;
  z-index: 2;
  width: 100%;
}

.hero-glass-card {
  background: rgba(15, 23, 42, 0.7);
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 24px;
  padding: 5rem 4rem;
  max-width: 1000px;
  box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.5);
  animation: cardEntrance 1.5s cubic-bezier(0.2, 0.8, 0.2, 1);
}

@keyframes cardEntrance {
  from { opacity: 0; transform: translateY(60px) scale(0.92); }
  to { opacity: 1; transform: translateY(0) scale(1); }
}

.text-accent {
  color: var(--accent);
}

h1.display-2 {
  color: #ffffff !important;
  font-weight: 800;
  letter-spacing: -1px;
}

.hero-lead {
  max-width: 750px;
  font-size: 1.15rem; /* Better baseline for mobile */
  font-weight: 400;
  line-height: 1.6;
  color: rgba(255, 255, 255, 0.95) !important; /* Force legibility against the dark background */
}

@media (min-width: 768px) {
  .hero-lead {
    font-size: 1.35rem; /* Larger for desktop */
  }
}

/* Removed Glowing Background Accents */

/* Button Refinement */
.btn-lg {
  padding: 1rem 2.5rem;
}

/* Clean Button Adjustments */

.btn-outline-futuristic {
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.3);
  color: #fff;
  font-weight: 600;
  transition: all 0.3s ease;
}

.btn-outline-futuristic:hover {
  background: rgba(255, 255, 255, 0.1);
  border-color: var(--accent);
  color: var(--accent);
}

/* Theme Adjustments */
:root.dark-theme .hero-glass-card {
  background: rgba(0, 0, 0, 0.4);
  border: 1px solid rgba(255, 255, 255, 0.05);
}

/* Responsive adjustments */
@media (max-width: 767.98px) {
  .hero-glass-card {
    padding: 3rem 1.5rem;
    border-radius: 30px;
  }
}
</style>
