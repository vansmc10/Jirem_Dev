<script setup>
import { ref, onMounted, onUnmounted, computed } from 'vue'

const isScrolled = ref(false)
const isDarkMode = ref(false)
const activeIndex = ref(0)
const hoveredIndex = ref(null)
const isLoaded = ref(false)

const menuItems = [
  { name: 'Inicio', icon: 'home', href: '#home' },
  { name: 'Servicios', icon: 'layers', href: '#services' },
  { name: 'Nosotros', icon: 'info', href: '#about' },
  { name: 'Proyectos', icon: 'work', href: '#projects' },
  { name: 'Paquetes', icon: 'local_offer', href: '#pricing' },
  { name: 'Testimonios', icon: 'star', href: '#testimonials' },
  { name: 'Contacto', icon: 'mail', href: '#contact' }
]

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50
  
  // Dynamic active link detection
  menuItems.forEach((item, index) => {
    const section = document.querySelector(item.href)
    if (section) {
      const top = section.offsetTop - 150
      const bottom = top + section.offsetHeight
      if (window.scrollY >= top && window.scrollY < bottom) {
        activeIndex.value = index
      }
    }
  })
}

const toggleDarkMode = () => {
  isDarkMode.value = !isDarkMode.value
  updateTheme()
}

const updateTheme = () => {
  const mode = isDarkMode.value ? 'dark' : 'light'
  // Apply to BOTH class and data-attribute for maximum framework compatibility
  document.documentElement.classList.toggle('dark-theme', isDarkMode.value)
  document.documentElement.classList.toggle('light-theme', !isDarkMode.value)
  document.documentElement.setAttribute('data-bs-theme', mode)
  localStorage.setItem('theme', mode)
}

const indicatorStyle = computed(() => {
  const index = hoveredIndex.value !== null ? hoveredIndex.value : activeIndex.value
  return {
    transform: `translateX(${index * 110}px)`,
    opacity: index !== null ? 1 : 0
  }
})

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
  setTimeout(() => isLoaded.value = true, 100)
  
  const savedTheme = localStorage.getItem('theme')
  if (savedTheme) {
    isDarkMode.value = savedTheme === 'dark'
  } else {
    isDarkMode.value = window.matchMedia('(prefers-color-scheme: dark)').matches
  }
  updateTheme()
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<template>
  <!-- Desktop Navbar -->
  <nav :class="['navbar navbar-expand-lg fixed-top d-none d-lg-block nav-reveal', isScrolled ? 'nav-scrolled' : 'nav-default']">
    <div class="container relative">
      <!-- Removed brand-glow -->
      <a class="navbar-brand d-flex align-items-center" href="#">
        <div class="">
          <img src="../../assets/images/jiremdev_min.jpg" 
               alt="Our Team" 
               width="60px"
               height="60px"
               class="img-fluid rounded-4 shadow-md">
          
          <!--<span class="material-icons logo-icon">analytics</span>-->
        </div>
        <span class="ms-2 brand-text">Jirem<span class="text-accent">Dev</span></span>
      </a>

      <div class="d-flex align-items-center ms-auto">
        <ul class="navbar-nav me-4 align-items-center nav-pill-container" :class="{ 'loaded': isLoaded }">
          <div class="nav-indicator-pill" :style="indicatorStyle"></div>
          
          <li v-for="(item, index) in menuItems" 
              :key="item.name" 
              class="nav-item stagger-link"
              :style="{ transitionDelay: `${index * 0.1}s` }"
              @mouseenter="hoveredIndex = index"
              @mouseleave="hoveredIndex = null"
              @click="activeIndex = index">
            <a class="nav-link nav-link-pill" :href="item.href" :class="{ 'active': activeIndex === index }">
              {{ item.name }}
            </a>
          </li>
        </ul>

        <div class="nav-actions d-flex align-items-center">
          <button @click="toggleDarkMode" class="btn-theme-toggle me-3" aria-label="Toggle Theme">
            <span class="material-icons">{{ isDarkMode ? 'light_mode' : 'dark_mode' }}</span>
          </button>
          <a href="#contact" class="btn btn-primary">Empezar Ya</a>
        </div>
      </div>
    </div>
  </nav>

  <!-- Mobile Bottom Tab Bar -->
  <div class="mobile-nav-container d-lg-none">
    <div class="mobile-tab-bar">
      <div class="mobile-indicator" :style="{ transform: `translateX(${activeIndex * 100}%)` }">
        <div class="liquid-drop"></div>
      </div>
      
      <a v-for="(item, index) in menuItems" 
         :key="item.name"
         :href="item.href"
         class="mobile-tab-item"
         :class="{ 'active': activeIndex === index }"
         @click="activeIndex = index">
        <span class="material-icons">{{ item.icon }}</span>
        <span class="tab-label">{{ item.name }}</span>
      </a>
      
      <button @click="toggleDarkMode" class="mobile-tab-item btn-clear" aria-label="Toggle Theme">
        <span class="material-icons">{{ isDarkMode ? 'light_mode' : 'dark_mode' }}</span>
      </button>
    </div>
  </div>
</template>

<style scoped>
/* Entrance Animation */
.nav-reveal {
  animation: navEntrance 0.8s cubic-bezier(0.2, 0.8, 0.2, 1) forwards;
  transform: translateY(-100%);
  opacity: 0;
}

@keyframes navEntrance {
  to { transform: translateY(0); opacity: 1; }
}

/* Staggered Links */
.stagger-link {
  opacity: 0;
  transform: translateY(-10px);
  transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1);
}

.loaded .stagger-link {
  opacity: 1;
  transform: translateY(0);
}

/* Desktop Navbar Pill Indicators */
.nav-pill-container {
  position: relative;
  background: rgba(255, 255, 255, 0.05);
  padding: 5px;
  border-radius: 50px;
  border: 1px solid var(--border);
  display: flex;
  backdrop-filter: blur(10px);
}

.nav-indicator-pill {
  position: absolute;
  top: 5px;
  left: 5px;
  width: 100px;
  height: calc(100% - 10px);
  background: var(--accent);
  border-radius: 50px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  transition: transform 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  z-index: 0;
}

.nav-link-pill {
  position: relative;
  z-index: 1;
  padding: 0.6rem 0 !important;
  color: var(--text-h) !important;
  font-weight: 700;
  text-transform: uppercase;
  font-size: 0.8rem;
  letter-spacing: 0.8px;
  transition: all 0.3s ease;
  width: 110px;
  text-align: center;
}

.nav-link-pill.active {
  color: #fff !important;
}

/* Theme Toggle Button - Reverted Aesthetic */
.btn-theme-toggle {
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid var(--border);
  color: var(--text-h);
  border-radius: 50%;
  width: 44px;
  height: 44px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  padding: 0;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(5px);
}

.btn-theme-toggle:hover {
  background: var(--accent);
  border-color: var(--accent);
  color: #fff;
  transform: rotate(45deg) scale(1.1);
  box-shadow: 0 4px 12px rgba(37, 99, 235, 0.2);
}

/* Mobile Nav... */
.mobile-nav-container {
  position: fixed;
  bottom: 25px;
  left: 50%;
  transform: translateX(-50%);
  width: 92%;
  max-width: 450px;
  z-index: 2000;
  animation: mobileNavReveal 0.8s cubic-bezier(0.2, 0.8, 0.2, 1) forwards;
}

@keyframes mobileNavReveal {
  from { transform: translate(-50%, 100%); opacity: 0; }
  to { transform: translate(-50%, 0); opacity: 1; }
}

.mobile-tab-bar {
  background: rgba(20, 40, 80, 0.45);
  backdrop-filter: blur(24px) saturate(160%);
  border: 1px solid rgba(0, 242, 254, 0.15);
  border-radius: 28px;
  display: flex;
  justify-content: space-between;
  padding: 12px 16px;
  box-shadow: 0 8px 32px rgba(0, 242, 254, 0.08), inset 0 1px 0 rgba(255, 255, 255, 0.1);
  position: relative;
}

.mobile-tab-item {
  flex: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-decoration: none;
  color: rgba(255, 255, 255, 0.7);
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  z-index: 2;
  position: relative;
  height: 50px;
}

.mobile-tab-item .material-icons {
  color: rgba(255, 255, 255, 0.6);
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  font-size: 1.35rem;
}

.mobile-tab-item.active {
  color: #fff;
}

.mobile-tab-item.active .material-icons {
  color: #fff;
  transform: translateY(-20px);
  z-index: 3;
  filter: drop-shadow(0 0 8px rgba(0, 242, 254, 0.4));
}

.tab-label {
  font-size: 9px;
  font-weight: 800;
  text-transform: uppercase;
  position: absolute;
  bottom: 5px;
  opacity: 0;
  transform: translateY(10px);
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  color: rgba(235, 225, 225, 0.7);
  letter-spacing: 0.5px;
}

.mobile-tab-item.active .tab-label {
  opacity: 1;
  transform: translateY(0);
}

.mobile-indicator {
  position: absolute;
  top: -15px;
  left: 0;
  width: calc(100% / 6);
  display: flex;
  justify-content: center;
  transition: transform 0.5s cubic-bezier(0.68, -0.55, 0.265, 1.55);
}

/* .liquid-drop {
  width: 50px;
  height: 50px;
  background: linear-gradient(135deg, rgba(0, 242, 254, 0.8), rgba(79, 172, 254, 0.6));
  border-radius: 50%;
  box-shadow: 0 8px 24px rgba(0, 242, 254, 0.3), inset -2px -2px 6px rgba(0, 0, 0, 0.1), inset 2px 2px 6px rgba(255, 255, 255, 0.1);
  border: 3px solid rgba(255, 255, 255, 0.15);
  backdrop-filter: blur(8px);
} */

.btn-clear {
  background: transparent;
  border: none;
  padding: 0;
}

/* Light theme mobile nav adjustments */
:root.light-theme .mobile-tab-bar {
  background: rgba(220, 230, 245, 0.45);
  border: 1px solid rgba(79, 172, 254, 0.25);
  box-shadow: 0 8px 32px rgba(79, 172, 254, 0.08), inset 0 1px 0 rgba(255, 255, 255, 0.3);
}

:root.light-theme .mobile-tab-item {
  color: rgba(26, 32, 44, 0.75);
}

:root.light-theme .mobile-tab-item .material-icons {
  color: rgba(26, 32, 44, 0.6);
}

:root.light-theme .mobile-tab-item.active {
  color: #0a0a0c;
}

:root.light-theme .mobile-tab-item.active .material-icons {
  color: #0a0a0c;
  filter: drop-shadow(0 0 8px rgba(79, 172, 254, 0.25));
}

:root.light-theme .tab-label {
  color: rgba(18, 18, 18, 0.7);
}

/* :root.light-theme .liquid-drop {
  background: linear-gradient(135deg, rgba(5, 206, 228, 0.726), rgba(3, 232, 248, 0.6));
  border: 3px solid rgba(79, 172, 254, 0.25);
  box-shadow: 0 8px 24px rgba(79, 172, 254, 0.2), inset -2px -2px 6px rgba(255, 255, 255, 0.15), inset 2px 2px 6px rgba(0, 0, 0, 0.05);
} */

/* Navbar Base... */
.fixed-top {
  padding: 1.5rem 0;
  transition: all 0.4s ease;
  z-index: 1030;
}

.nav-scrolled {
  padding: 0.8rem 0;
  background: var(--nav-bg) !important;
  backdrop-filter: blur(12px) saturate(180%);
  border-bottom: 1px solid var(--border);
}

.brand-text {
  font-family: var(--heading);
  font-weight: 800;
  text-transform: uppercase;
  letter-spacing: 2px;
  color: var(--text-h);
}

.logo-icon-wrapper {
  background: var(--accent);
  padding: 6px;
  border-radius: 10px;
  display: flex;
  align-items: center;
  box-shadow: 0 2px 8px rgba(37, 99, 235, 0.2);
}

/* Removed btn-neon */
</style>
