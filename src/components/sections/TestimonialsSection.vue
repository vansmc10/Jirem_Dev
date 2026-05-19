<template>
  <section id="testimonials" class="section-padding">
    <div class="container">
      <div class="text-center mb-5">
        <h2 class="section-title">Testimonios de Clientes</h2>
        <p class="section-subtitle lead text-muted">
          Lo que nuestros clientes dicen sobre nuestros servicios
        </p>
      </div>

      <div class="row g-4">
        <!-- Testimonial 1 -->
        <div class="col-lg-4">
          <div class="testimonial-card material-card h-100">
            <div class="stars mb-3">
              <span v-for="i in 5" :key="i" class="material-icons">star</span>
            </div>
            <p class="testimonial-text mb-4">
              "JIREM Dev transformó completamente nuestra presencia online. El equipo fue muy profesional 
              y entregó nuestro sitio web en tiempo record. Altamente recomendado."
            </p>
            <div class="testimonial-author">
              <div class="author-avatar">JC</div>
              <div>
                <p class="author-name">Juan Carlos Méndez</p>
                <p class="author-role">Dueño de Empresa</p>
              </div>
            </div>
          </div>
        </div>

        <!-- Testimonial 2 -->
        <div class="col-lg-4">
          <div class="testimonial-card material-card h-100">
            <div class="stars mb-3">
              <span v-for="i in 5" :key="i" class="material-icons">star</span>
            </div>
            <p class="testimonial-text mb-4">
              "El equipo de JIREM Dev nos ayudó a crear una tienda online funcional y hermosa. 
              El soporte técnico fue excelente y siempre disponible. Mejoramos significativamente 
              nuestras ventas online."
            </p>
            <div class="testimonial-author">
              <div class="author-avatar">MC</div>
              <div>
                <p class="author-name">María Católicos</p>
                <p class="author-role">Gerente de Ventas</p>
              </div>
            </div>
          </div>
        </div>

        <!-- Testimonial 3 -->
        <div class="col-lg-4">
          <div class="testimonial-card material-card h-100">
            <div class="stars mb-3">
              <span v-for="i in 5" :key="i" class="material-icons">star</span>
            </div>
            <p class="testimonial-text mb-4">
              "Excelente servicio de inicio a fin. El diseño es moderno, responsive y exactamente 
              lo que necesitábamos. Muy atentos a los detalles y profesionales. Volveríamos a trabajar 
              con ellos sin dudar."
            </p>
            <div class="testimonial-author">
              <div class="author-avatar">RP</div>
              <div>
                <p class="author-name">Roberto Pérez</p>
                <p class="author-role">Consultor de Negocios</p>
              </div>
            </div>
          </div>
        </div>

        <!-- Testimonial 4 -->
        <div class="col-lg-4">
          <div class="testimonial-card material-card h-100">
            <div class="stars mb-3">
              <span v-for="i in 5" :key="i" class="material-icons">star</span>
            </div>
            <p class="testimonial-text mb-4">
              "Buscábamos un equipo confiable para nuestro proyecto web y los encontramos en JIREM Dev. 
              Su enfoque en SEO y optimización fue lo que marcó la diferencia en nuestro éxito digital."
            </p>
            <div class="testimonial-author">
              <div class="author-avatar">AL</div>
              <div>
                <p class="author-name">Ana López</p>
                <p class="author-role">Directora de Marketing</p>
              </div>
            </div>
          </div>
        </div>

        <!-- Testimonial 5 -->
        <div class="col-lg-4">
          <div class="testimonial-card material-card h-100">
            <div class="stars mb-3">
              <span v-for="i in 5" :key="i" class="material-icons">star</span>
            </div>
            <p class="testimonial-text mb-4">
              "Como startup, necesitábamos un MVP rápido y de calidad. JIREM Dev lo logró perfectamente 
              y dentro del presupuesto. El proceso fue transparente y la comunicación siempre clara."
            </p>
            <div class="testimonial-author">
              <div class="author-avatar">CF</div>
              <div>
                <p class="author-name">Carlos Flores</p>
                <p class="author-role">CEO Startup Tech</p>
              </div>
            </div>
          </div>
        </div>

        <!-- Testimonial 6 -->
        <div class="col-lg-4">
          <div class="testimonial-card material-card h-100">
            <div class="stars mb-3">
              <span v-for="i in 5" :key="i" class="material-icons">star</span>
            </div>
            <p class="testimonial-text mb-4">
              "Nos encantó trabajar con JIREM Dev. Son innovadores, escuchan las necesidades del cliente 
              y ofrecen soluciones reales. Nuestro site web ahora es una verdadera herramienta de negocio."
            </p>
            <div class="testimonial-author">
              <div class="author-avatar">SR</div>
              <div>
                <p class="author-name">Sandra Rodríguez</p>
                <p class="author-role">Propietaria de Boutique</p>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- CTA Section -->
      <div class="row mt-5">
        <div class="col-lg-8 mx-auto">
          <div class="material-card text-center p-5 bg-primary-light">
            <h3 class="mb-3 fw-bold">¿Listo para transformar tu negocio digital?</h3>
            <p class="text-muted mb-4">
              Únete a decenas de empresas que confían en JIREM Dev para sus soluciones web
            </p>
            <a href="#contact" class="btn btn-primary btn-lg">
              <span class="material-icons">mail</span>
              Contactar Ahora
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// Sección de testimonios de clientes
</script>

<style scoped>
.section-padding {
  padding: 5rem 0;
}

.section-title {
  font-size: 2.5rem;
  font-weight: 700;
  color: var(--dark-color);
  margin-bottom: 1rem;
}

.section-subtitle {
  max-width: 600px;
  margin: 0 auto;
}

.testimonial-card {
  background: white;
  border-radius: 0.75rem;
  border: 1px solid #ddd;
  padding: 2rem;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  display: flex;
  flex-direction: column;
}

.testimonial-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.1);
}

.stars {
  display: flex;
  gap: 0.25rem;
  margin-bottom: 1rem;
}

.stars .material-icons {
  font-size: 1.25rem;
  color: #ffc107;
}

.testimonial-text {
  color: var(--text-color);
  font-size: 0.95rem;
  line-height: 1.6;
  flex-grow: 1;
  margin: 0;
  font-style: italic;
}

.testimonial-author {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-top: 1.5rem;
  padding-top: 1.5rem;
  border-top: 1px solid #eee;
}

.author-avatar {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 700;
  font-size: 1.25rem;
  flex-shrink: 0;
}

.author-name {
  font-weight: 600;
  margin: 0;
  color: var(--dark-color);
  font-size: 0.95rem;
}

.author-role {
  font-size: 0.85rem;
  color: var(--text-muted);
  margin: 0.25rem 0 0 0;
}

.material-card {
  background: white;
  border-radius: 0.75rem;
  border: 1px solid #ddd;
}

.bg-primary-light {
  background: rgba(var(--primary-color-rgb), 0.05) !important;
}

.btn {
  transition: all 0.3s ease;
  text-decoration: none;
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
}

.btn-primary {
  background-color: var(--primary-color);
  color: white;
  border: none;
  padding: 0.75rem 1.5rem;
  border-radius: 0.5rem;
  font-weight: 600;
  cursor: pointer;
}

.btn-primary:hover {
  opacity: 0.9;
  transform: translateY(-2px);
}

.btn-lg {
  padding: 1rem 2rem;
  font-size: 1.1rem;
}

.material-icons {
  display: inline-flex;
  vertical-align: middle;
}
</style>
