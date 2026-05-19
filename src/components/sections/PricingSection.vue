<template>
  <section id="pricing" class="section-padding bg-light">
    <div class="container">
      <div class="text-center mb-5">
        <h2 class="section-title">Nuestros Paquetes</h2>
        <p class="section-subtitle lead text-muted">
          Soluciones para cada etapa de tu negocio digital
        </p>
      </div>

      <div class="row g-4 mb-5 pricing-row">
        <!-- Plan Emprende -->
        <div class="col-lg-4 col-md-6">
          <div class="pricing-card material-card h-100">
            <div class="card-body d-flex flex-column text-center">
              <div class="badge bg-secondary mb-3 mx-auto">Para Emprendedores</div>
              <h3 class="mb-3">Plan Emprende</h3>
              <p class="text-muted small mb-3">Landing page profesional</p>
              
              <div class="price mb-4">
                <span class="currency">S/</span>
                <span class="amount">1,200</span>
              </div>

              <ul class="features-list mb-4 flex-grow-1">
                <li><span class="material-icons">check_circle</span> Landing page profesional</li>
                <li><span class="material-icons">check_circle</span> Dominio .com/.pe + SSL</li>
                <li><span class="material-icons">check_circle</span> Hosting 2GB</li>
                <li><span class="material-icons">check_circle</span> 3 correos corporativos</li>
                <li><span class="material-icons">check_circle</span> Diseño responsive</li>
                <li><span class="material-icons">check_circle</span> WhatsApp Business integrado</li>
              </ul>
              <p class="small text-muted mb-3"><span class="material-icons" style="font-size: 1rem;">schedule</span> 7-10 días</p>

              <button class="btn btn-outline-primary w-100">
                Consultar
              </button>
            </div>
          </div>
        </div>

        <!-- Plan Crece -->
        <div class="col-lg-4 col-md-6">
          <div class="pricing-card material-card h-100 border-primary popular">
            <div class="card-body d-flex flex-column text-center">
              <div class="badge bg-primary mb-3 mx-auto">Más Popular</div>
              <h3 class="mb-3">Plan Crece</h3>
              <p class="text-muted small mb-3">Sitio web empresarial completo</p>
              
              <div class="price mb-4">
                <span class="currency">S/</span>
                <span class="amount">2,200<span style="font-size: 0.6em;">+</span></span>
              </div>

              <ul class="features-list mb-4 flex-grow-1">
                <li><span class="material-icons">check_circle</span> Sitio web multipágina</li>
                <li><span class="material-icons">check_circle</span> UI/UX corporativo estratégico</li>
                <li><span class="material-icons">check_circle</span> SEO On-Page completo</li>
                <li><span class="material-icons">check_circle</span> Google My Business</li>
                <li><span class="material-icons">check_circle</span> Hosting 5GB + panel admin</li>
                <li><span class="material-icons">check_circle</span> Analítica y métricas</li>
              </ul>
              <p class="small text-muted mb-3"><span class="material-icons" style="font-size: 1rem;">schedule</span> 15-20 días</p>

              <button class="btn btn-primary w-100">
                Consultar Ahora
              </button>
            </div>
          </div>
        </div>

        <!-- Plan Elite -->
        <div class="col-lg-4 col-md-6">
          <div class="pricing-card material-card h-100">
            <div class="card-body d-flex flex-column text-center">
              <div class="badge bg-info mb-3 mx-auto">Para Tiendas</div>
              <h3 class="mb-3">Plan Elite</h3>
              <p class="text-muted small mb-3">E-commerce y tiendas online</p>
              
              <div class="price mb-4">
                <span class="currency">S/</span>
                <span class="amount">4,500<span style="font-size: 0.6em;">+</span></span>
              </div>

              <ul class="features-list mb-4 flex-grow-1">
                <li><span class="material-icons">check_circle</span> E-commerce completo</li>
                <li><span class="material-icons">check_circle</span> Pasarelas Niubiz/Izipay/Culqi</li>
                <li><span class="material-icons">check_circle</span> Panel admin personalizado</li>
                <li><span class="material-icons">check_circle</span> Hosting empresarial</li>
                <li><span class="material-icons">check_circle</span> Soporte técnico 24/7</li>
                <li><span class="material-icons">check_circle</span> Escalabilidad garantizada</li>
              </ul>
              <p class="small text-muted mb-3"><span class="material-icons" style="font-size: 1rem;">schedule</span> 25-35 días</p>

              <button class="btn btn-outline-primary w-100">
                Consultar
              </button>
            </div>
          </div>
        </div>
      </div>

      <!-- Brochure Download -->
      <div class="row">
        <div class="col-lg-8 mx-auto">
          <div class="material-card text-center p-5">
            <span class="material-icons display-5 text-primary mb-3">description</span>
            <h4 class="mb-3 fw-bold">Obtén nuestro Brochure Completo</h4>
            <p class="text-muted mb-4">
              Descarga nuestro brochure detallado con información completa sobre todos nuestros servicios, 
              paquetes, precios, estudios de casos y testimonios de clientes.
            </p>
            <a href="/brochure.html" target="_blank" class="btn btn-primary btn-lg">
              <span class="material-icons">download</span>
              Ver Brochure
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// Sección de paquetes de precios
</script>

<style scoped>
.bg-light {
  background-color: #f8f9fa;
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

.pricing-card {
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  border: 2px solid transparent;
}

.pricing-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.1);
}

.pricing-card.popular {
  border-color: var(--primary-color);
  transform: scale(1.05);
}

.pricing-card.popular:hover {
  transform: scale(1.05) translateY(-8px);
}

.price {
  display: flex;
  align-items: baseline;
  justify-content: center;
  gap: 0.5rem;
}

.currency {
  font-size: 1.5rem;
  color: var(--primary-color);
}

.amount {
  font-size: 3rem;
  font-weight: 700;
  color: var(--dark-color);
}

.period {
  color: var(--text-muted);
  font-size: 1rem;
}

.features-list {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.75rem;
}

.features-list li {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  margin-bottom: 0;
  color: var(--text-muted);
  font-size: 0.95rem;
}

.features-list .material-icons {
  font-size: 1.25rem;
  color: var(--primary-color);
  flex-shrink: 0;
}

.badge {
  font-size: 0.75rem;
  font-weight: 600;
  padding: 0.5rem 1rem;
  width: fit-content;
}

.material-icons {
  display: inline-flex;
  vertical-align: middle;
}

.display-5 {
  font-size: 3rem;
}

.pricing-row {
  justify-content: center;
}

/* Responsive adjustments */
@media (max-width: 992px) {
  .pricing-card.popular {
    transform: scale(1);
  }

  .pricing-card.popular:hover {
    transform: translateY(-8px);
  }
}
</style>
