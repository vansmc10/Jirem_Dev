<template>
  <section id="services" class="section-padding">
    <div class="container">
      <div class="text-center mb-5">
        <h2 class="section-title">Servicios</h2>
        <p class="section-subtitle lead text-muted">
          Desde la estrategia hasta la implementación, soluciones integrales para tu negocio
        </p>
      </div>
      <div class="row g-4">
        <div class="col-md-4">
          <div class="service-card">
            <div class="service-icon-wrapper">
              <span class="material-icons service-icon">code</span>
            </div>
            <h3 class="service-title">Desarrollo Personalizado</h3>
            <p class="service-desc">Aplicaciones web y móviles de alta calidad y escalables, adaptadas a las necesidades de tu negocio.</p>
            <div class="service-footer">
              <span class="service-tag">Web & Móvil</span>
            </div>
          </div>
        </div>
        <div class="col-md-4">
          <div class="service-card">
            <div class="service-icon-wrapper">
              <span class="material-icons service-icon">cloud_queue</span>
            </div>
            <h3 class="service-title">Migración a la Nube</h3>
            <p class="service-desc">Migra tu infraestructura a AWS, Google Cloud o Azure de forma segura, sin interrupciones y con costo optimizado.</p>
            <div class="service-footer">
              <span class="service-tag">Cloud</span>
            </div>
          </div>
        </div>
        <div class="col-md-4">
          <div class="service-card">
            <div class="service-icon-wrapper">
              <span class="material-icons service-icon">analytics</span>
            </div>
            <h3 class="service-title">Análisis de Datos</h3>
            <p class="service-desc">Transforma datos brutos en información útil mediante inteligencia empresarial y machine learning.</p>
            <div class="service-footer">
              <span class="service-tag">Data & BI</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.section-subtitle {
  max-width: 600px;
  margin: 0 auto;
}

.service-card {
  background: var(--bg-alt);
  border: 1px solid var(--border);
  border-radius: 20px;
  padding: 2.5rem 2rem;
  text-align: center;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  transition: transform 0.35s cubic-bezier(0.2, 0.8, 0.2, 1), box-shadow 0.35s ease, border-color 0.35s ease;
}

.service-card:hover {
  transform: translateY(-8px);
  box-shadow: var(--shadow-hover);
  border-color: var(--accent);
}

.service-icon-wrapper {
  width: 72px;
  height: 72px;
  border-radius: 20px;
  background: rgba(37, 99, 235, 0.08);
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 1.5rem;
  transition: background 0.35s ease, transform 0.35s ease;
}

.service-card:hover .service-icon-wrapper {
  background: var(--accent);
  transform: scale(1.05);
}

.service-icon {
  font-size: 2rem;
  color: var(--accent);
  transition: color 0.35s ease;
  line-height: 1;
  display: flex;
  align-items: center;
  justify-content: center;
}

.service-card:hover .service-icon {
  color: #fff;
}

.service-title {
  font-size: 1.2rem;
  font-weight: 700;
  color: var(--text-h);
  margin-bottom: 0.75rem;
}

.service-desc {
  font-size: 0.9rem;
  color: var(--text2);
  line-height: 1.6;
  margin: 0;
  flex-grow: 1;
}

.service-footer {
  margin-top: 1.5rem;
  padding-top: 1.25rem;
  border-top: 1px solid var(--border);
  width: 100%;
}

.service-tag {
  display: inline-block;
  font-size: 0.75rem;
  font-weight: 600;
  color: var(--accent);
  background: rgba(37, 99, 235, 0.08);
  padding: 0.3rem 1rem;
  border-radius: 20px;
  letter-spacing: 0.3px;
}
</style>
