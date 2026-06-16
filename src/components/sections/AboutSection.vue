<template>
  <section id="about" class="section-padding">
    <div class="container">
      <div class="text-center mb-5">
        <h2 class="section-title">Sobre Nosotros</h2>
        <p class="section-subtitle lead text-muted">
          Conoce al equipo detrás de JIREM DEV
        </p>
      </div>
      <div class="row align-items-center g-5">
        <div class="col-lg-6">
          <div class="about-image-wrapper">
            <div class="about-image-decoration"></div>
            <img src="https://images.unsplash.com/photo-1522071820081-009f0129c71c?auto=format&fit=crop&w=800&q=80" 
                 alt="Our Team" 
                 class="about-image">
          </div>
        </div>
        <div class="col-lg-6">
          <span class="about-badge">Desde 2025</span>
          <h2 class="about-title">Impulsando la innovación digital</h2>
          <p class="about-text">
            Somos un equipo de consultores, arquitectos y diseñadores de software apasionados por resolver problemas complejos y crear soluciones que transforman negocios.
          </p>
          <p class="about-text-muted">
            Nuestra misión es ayudar a empresas y emprendedores a superar la brecha entre sus objetivos comerciales y la realidad técnica. Creemos en la transparencia, las metodologías ágiles y en ofrecer valor cuantificable con cada proyecto.
          </p>
          <div class="about-stats">
            <div class="stat-item">
              <span class="stat-number">+5</span>
              <span class="stat-label">Años de experiencia</span>
            </div>
            <div class="stat-divider"></div>
            <div class="stat-item">
              <span class="stat-number">+30</span>
              <span class="stat-label">Proyectos entregados</span>
            </div>
            <div class="stat-divider"></div>
            <div class="stat-item">
              <span class="stat-number">100%</span>
              <span class="stat-label">Clientes satisfechos</span>
            </div>
          </div>
          <div class="about-features">
            <div class="feature-item">
              <span class="feature-icon">
                <span class="material-icons">check_circle</span>
              </span>
              <span class="feature-text">Soluciones de Software Escalables</span>
            </div>
            <div class="feature-item">
              <span class="feature-icon">
                <span class="material-icons">check_circle</span>
              </span>
              <span class="feature-text">Expertos en Desarrollo y Consultoría</span>
            </div>
            <div class="feature-item">
              <span class="feature-icon">
                <span class="material-icons">check_circle</span>
              </span>
              <span class="feature-text">Experiencia en Múltiples Industrias</span>
            </div>
            <div class="feature-item">
              <span class="feature-icon">
                <span class="material-icons">check_circle</span>
              </span>
              <span class="feature-text">Compromiso con Resultados Reales</span>
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

/* Image */
.about-image-wrapper {
  position: relative;
}

.about-image-decoration {
  position: absolute;
  top: -12px;
  left: -12px;
  width: 100%;
  height: 100%;
  border: 2px solid var(--accent);
  border-radius: 24px;
  opacity: 0.3;
  z-index: 0;
}

.about-image {
  width: 100%;
  height: auto;
  border-radius: 20px;
  position: relative;
  z-index: 1;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
}

/* Badge */
.about-badge {
  display: inline-block;
  font-size: 0.75rem;
  font-weight: 600;
  color: var(--accent);
  background: rgba(37, 99, 235, 0.08);
  padding: 0.35rem 1rem;
  border-radius: 20px;
  letter-spacing: 0.5px;
  margin-bottom: 1rem;
}

/* Title */
.about-title {
  font-size: 2rem;
  font-weight: 700;
  color: var(--text-h);
  margin-bottom: 1.25rem;
  line-height: 1.3;
}

/* Text */
.about-text {
  font-size: 1rem;
  color: var(--text);
  line-height: 1.7;
  margin-bottom: 1rem;
}

.about-text-muted {
  font-size: 0.92rem;
  color: var(--text2);
  line-height: 1.7;
  margin-bottom: 2rem;
}

/* Stats */
.about-stats {
  display: flex;
  align-items: center;
  gap: 1.5rem;
  margin-bottom: 2rem;
  padding: 1.25rem 1.5rem;
  background: var(--bg-alt);
  border: 1px solid var(--border);
  border-radius: 16px;
}

.stat-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.2rem;
  flex: 1;
}

.stat-number {
  font-size: 1.5rem;
  font-weight: 800;
  color: var(--accent);
  line-height: 1;
}

.stat-label {
  font-size: 0.7rem;
  font-weight: 500;
  color: var(--text2);
  text-align: center;
  text-transform: uppercase;
  letter-spacing: 0.3px;
}

.stat-divider {
  width: 1px;
  height: 40px;
  background: var(--border);
}

/* Features */
.about-features {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0.75rem;
}

.feature-item {
  display: flex;
  align-items: center;
  gap: 0.6rem;
}

.feature-icon {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 24px;
  height: 24px;
  border-radius: 50%;
  background: var(--accent);
  flex-shrink: 0;
}

.feature-icon .material-icons {
  font-size: 0.8rem;
  color: #fff;
}

.feature-text {
  font-size: 0.82rem;
  font-weight: 600;
  color: var(--text);
  line-height: 1.3;
}

@media (max-width: 768px) {
  .about-features {
    grid-template-columns: 1fr;
  }

  .about-stats {
    flex-direction: column;
    gap: 1rem;
  }

  .stat-divider {
    width: 100%;
    height: 1px;
  }

  .about-title {
    font-size: 1.6rem;
  }
}
</style>
