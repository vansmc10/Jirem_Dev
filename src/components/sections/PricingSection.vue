<template>
  <section id="pricing" class="section-padding">
    <div class="container">
      <div class="text-center mb-5">
        <h2 class="section-title">Planes para tu Negocio</h2>
        <p class="section-subtitle lead text-muted">
          Invierte en tu transformación digital con precios pensados para el mercado peruano
        </p>
      </div>

      <div class="row g-4 mb-5 pricing-row">
        <!-- Plan Emprende -->
        <div class="col-lg-4 col-md-6">
          <div class="pricing-card material-card h-100">
            <div class="card-body d-flex flex-column text-center">
              <div class="badge badge-emprende mb-3 mx-auto">Para Emprendedores</div>
              <h3 class="plan-name">Plan Emprende</h3>
              <p class="plan-desc">Landing page profesional</p>
              
              <div class="price mb-4">
                <span class="currency">S/</span>
                <span class="amount">990</span>
              </div>

              <ul class="features-list mb-4 flex-grow-1">
                <li><span class="check-icon">✓</span> Landing page profesional</li>
                <li><span class="check-icon">✓</span> Dominio .com/.pe + SSL</li>
                <!-- <li><span class="check-icon">✓</span> Hosting 2GB</li>
                <li><span class="check-icon">✓</span> 3 correos corporativos</li> -->
                <li><span class="check-icon">✓</span> Diseño responsive</li>
                <!-- <li><span class="check-icon">✓</span> WhatsApp Business integrado</li> -->
              </ul>
              <div class="delivery"><span class="material-icons">schedule</span> 7-10 días hábiles</div>

              <button class="btn btn-outline-primary w-100" @click="consultarWhatsApp('Plan Emprende')">
                Consultar
              </button>
            </div>
          </div>
        </div>

        <!-- Plan Crece -->
        <div class="col-lg-4 col-md-6">
          <div class="pricing-card popular h-100">
            <div class="popular-badge">Más Popular</div>
            <div class="card-body d-flex flex-column text-center">
              <div class="badge badge-crece mb-3 mx-auto">Para Empresas</div>
              <h3 class="plan-name">Plan Crece</h3>
              <p class="plan-desc">Sitio web empresarial completo</p>
              
              <div class="price mb-4">
                <span class="currency">S/</span>
                <span class="amount">1,990</span>
              </div>

              <ul class="features-list mb-4 flex-grow-1">
                <li><span class="check-icon">✓</span> Sitio web multipágina</li>
                <li><span class="check-icon">✓</span> UI/UX corporativo estratégico</li>
                <li><span class="check-icon">✓</span> SEO On-Page completo</li>
                <!-- <li><span class="check-icon">✓</span> Google My Business</li> -->
                <li><span class="check-icon">✓</span> Hosting 5GB + panel admin</li>
                <li><span class="check-icon">✓</span> Analítica y métricas</li>
              </ul>
              <div class="delivery"><span class="material-icons">schedule</span> 15-20 días hábiles</div>

              <button class="btn btn-primary w-100" @click="consultarWhatsApp('Plan Crece')">
                Consultar Ahora
              </button>
            </div>
          </div>
        </div>

        <!-- Plan Elite -->
        <div class="col-lg-4 col-md-6">
          <div class="pricing-card material-card h-100">
            <div class="card-body d-flex flex-column text-center">
              <div class="badge badge-elite mb-3 mx-auto">Para Tiendas</div>
              <h3 class="plan-name">Plan Elite</h3>
              <p class="plan-desc">E-commerce y tiendas online</p>
              
              <div class="price mb-4">
                <span class="currency">S/</span>
                <span class="amount">3,990</span>
              </div>

              <ul class="features-list mb-4 flex-grow-1">
                <li><span class="check-icon">✓</span> E-commerce completo</li>
                <li><span class="check-icon">✓</span> Pasarelas Niubiz/Izipay/Culqi</li>
                <li><span class="check-icon">✓</span> Panel admin personalizado</li>
                <li><span class="check-icon">✓</span> Hosting empresarial</li>
                <li><span class="check-icon">✓</span> Soporte técnico 24/7</li>
                <li><span class="check-icon">✓</span> Escalabilidad garantizada</li>
              </ul>
              <div class="delivery"><span class="material-icons">schedule</span> 25-35 días hábiles</div>

              <button class="btn btn-outline-primary w-100" @click="consultarWhatsApp('Plan Elite')">
                Consultar
              </button>
            </div>
          </div>
        </div>
      </div>

      <!-- Brochure Download -->
      <div class="row">
        <div class="col-lg-8 mx-auto">
          <div class="material-card brochure-card text-center p-5">
            <span class="material-icons display-5 icon-document mb-3">description</span>
            <h4 class="mb-3 fw-bold">Brochure Completo</h4>
            <p class="text-muted mb-4">
              Descarga información detallada de todos nuestros servicios, planes y casos de éxito.
            </p>
            <a href="/brochure.html" target="_blank" class="btn btn-primary btn-lg">
              <span class="material-icons">download</span>
              Descargar Brochure
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const consultarWhatsApp = (paquete) => {
  const numero = '51943712678'
  const mensaje = encodeURIComponent(`Estimado equipo de JIREM DEV,

Me gustaría recibir información detallada sobre el "${paquete}". Agradeceré me puedan compartir los beneficios, alcances y condiciones.

Quedo atento a su pronta respuesta.

Saludos cordiales.`)
  window.open(`https://wa.me/${numero}?text=${mensaje}`, '_blank')
}
</script>

<style scoped>
.section-title {
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 1rem;
}

.section-subtitle {
  max-width: 600px;
  margin: 0 auto;
}

.pricing-row {
  justify-content: center;
}

/* ---- Cards ---- */
.pricing-card {
  border: 1px solid var(--border);
  border-radius: 20px;
  transition: transform 0.35s cubic-bezier(0.2, 0.8, 0.2, 1), box-shadow 0.35s ease;
}

.pricing-card:hover {
  transform: translateY(-6px);
  box-shadow: var(--shadow-hover);
}

/* ---- Popular card ---- */
.pricing-card.popular {
  position: relative;
  background: var(--bg-alt);
  border: 2px solid var(--accent);
  box-shadow: 0 0 0 1px rgba(37, 99, 235, 0.08), 0 8px 24px rgba(37, 99, 235, 0.12);
  transform: scale(1.05);
  z-index: 2;
}

.pricing-card.popular:hover {
  transform: scale(1.05) translateY(-6px);
}

.popular-badge {
  position: absolute;
  top: -14px;
  left: 50%;
  transform: translateX(-50%);
  background: var(--accent);
  color: #fff;
  font-size: 0.8rem;
  font-weight: 700;
  padding: 0.35rem 1.5rem;
  border-radius: 20px;
  letter-spacing: 0.3px;
  white-space: nowrap;
  z-index: 3;
}

/* ---- Badges ---- */
.badge {
  font-size: 0.72rem;
  font-weight: 600;
  padding: 0.4rem 1rem;
  border-radius: 20px;
  letter-spacing: 0.3px;
}

.badge-emprende {
  background: rgba(37, 99, 235, 0.08);
  color: var(--accent);
  border: 1px solid rgba(37, 99, 235, 0.2);
}

.badge-crece {
  background: rgba(37, 99, 235, 0.12);
  color: var(--accent);
  border: 1px solid rgba(37, 99, 235, 0.3);
}

.badge-elite {
  background: rgba(99, 102, 241, 0.08);
  color: #6366f1;
  border: 1px solid rgba(99, 102, 241, 0.2);
}

/* ---- Plan name & desc ---- */
.plan-name {
  font-size: 1.5rem;
  font-weight: 800;
  color: var(--text-h);
  margin-bottom: 0.25rem;
}

.plan-desc {
  font-size: 0.9rem;
  color: var(--text2);
  margin-bottom: 1.5rem;
}

/* ---- Price ---- */
.price {
  display: flex;
  align-items: baseline;
  justify-content: center;
  gap: 0.25rem;
}

.currency {
  font-size: 1.35rem;
  font-weight: 700;
  color: var(--accent);
}

.amount {
  font-size: 3rem;
  font-weight: 800;
  color: var(--text-h);
  line-height: 1;
  letter-spacing: -1px;
}

/* ---- Features ---- */
.features-list {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  flex-direction: column;
  gap: 0.7rem;
}

.features-list li {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.6rem;
  color: var(--text);
  font-size: 0.9rem;
}

.check-icon {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: 20px;
  height: 20px;
  border-radius: 50%;
  background: var(--accent);
  color: #fff;
  font-size: 0.7rem;
  font-weight: 700;
  flex-shrink: 0;
}

/* ---- Delivery ---- */
.delivery {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.3rem;
  font-size: 0.82rem;
  color: var(--text2);
  margin-bottom: 1.2rem;
}

.delivery .material-icons {
  font-size: 1rem;
  color: var(--accent);
}

/* ---- Buttons ---- */
.btn-outline-primary {
  background: transparent;
  border: 2px solid var(--accent);
  color: var(--accent);
  font-weight: 700;
  padding: 0.75rem 1.5rem;
  border-radius: 12px;
  transition: all 0.25s ease;
}

.btn-outline-primary:hover {
  background: var(--accent);
  color: #fff !important;
}

.btn-primary {
  background: var(--accent);
  border: none;
  font-weight: 700;
  padding: 0.75rem 1.5rem;
  border-radius: 12px;
  color: #fff !important;
  box-shadow: 0 4px 12px rgba(37, 99, 235, 0.25);
  transition: all 0.25s ease;
}

.btn-primary:hover {
  background: var(--accent-secondary);
  transform: translateY(-2px);
  box-shadow: 0 6px 16px rgba(37, 99, 235, 0.35);
}

/* ---- Brochure ---- */
.brochure-card {
  border-radius: 20px;
}

.icon-document {
  color: var(--accent);
  opacity: 0.8;
}

/* ---- Icons ---- */
.material-icons {
  display: inline-flex;
  vertical-align: middle;
}

.display-5 {
  font-size: 3rem;
}

/* ---- Responsive ---- */
@media (max-width: 992px) {
  .pricing-card.popular {
    transform: scale(1);
  }

  .pricing-card.popular:hover {
    transform: translateY(-6px);
  }
}
</style>
