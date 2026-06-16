<template>
  <section id="projects" class="section-padding">
    <div class="container">
      <div class="text-center mb-5">
        <h2 class="section-title">Historias de Éxito</h2>
        <p class="section-subtitle lead text-muted">
          Proyectos que han transformado negocios y generado resultados reales
        </p>
      </div>
      <div class="row g-4">
        <div class="col-md-6 col-lg-4">
          <div class="project-card">
            <div class="project-image">
              <img src="https://images.unsplash.com/photo-1460925895917-afdab827c52f?auto=format&fit=crop&w=800&q=80" alt="Sistema de Gestión Hospitalaria">
              <div class="project-overlay">
                <span class="project-category">HealthTech</span>
              </div>
            </div>
            <div class="project-body">
              <div class="project-tags">
                <span class="project-tag">Sistema de Gestión Hospitalaria</span>
              </div>
              <h3 class="project-title">Salud / HealthTech</h3>
              <p class="project-desc">Sistema de gestión hospitalaria diseñado para digitalizar procesos clínicos y administrativos, facilitando el control de pacientes, programación de citas, historiales médicos y generación de reportes en una plataforma segura y escalable.</p>
            </div>
          </div>
        </div>
        <div class="col-md-6 col-lg-4">
          <div class="project-card">
            <div class="project-image">
              <img src="../../assets/images/jcstudio.png" alt="Portal Web para Estudio Fotográfico">
              <div class="project-overlay">
                <span class="project-category">Fotografía</span>
              </div>
            </div>
            <div class="project-body">
              <div class="project-tags">
                <span class="project-tag">Portal Web</span>
              </div>
              <h3 class="project-title">Sitio Web Fotografía Studio</h3>
              <p class="project-desc">Portal web corporativo para estudio fotográfico orientado a la presentación de portafolios visuales, servicios profesionales y reservas de sesiones, con diseño responsive y experiencia de usuario optimizada.</p>
              <a href="https://jcstudiosperu.com/" class="project-link" target="_blank">
                Ver Caso de Estudio
                <span class="material-icons">arrow_forward</span>
              </a>
            </div>
          </div>
        </div>
        <div class="col-md-6 col-lg-4">
          <div class="project-card">
            <div class="project-image">
              <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?auto=format&fit=crop&w=800&q=80" alt="Plataforma E-commerce VansYul">
              <div class="project-overlay">
                <span class="project-category">E-commerce</span>
              </div>
            </div>
            <div class="project-body">
              <div class="project-tags">
                <span class="project-tag">Plataforma E-commerce VansYul</span>
              </div>
              <h3 class="project-title">Comercio Electrónico</h3>
              <p class="project-desc">Plataforma de comercio electrónico multivendedor diseñada para gestionar catálogos de productos, ventas y operaciones comerciales en línea, con arquitectura escalable y capacidades de integración con servicios externos.</p>
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

.project-card {
  background: var(--bg-alt);
  border: 1px solid var(--border);
  border-radius: 20px;
  overflow: hidden;
  height: 100%;
  display: flex;
  flex-direction: column;
  transition: transform 0.35s cubic-bezier(0.2, 0.8, 0.2, 1), box-shadow 0.35s ease;
}

.project-card:hover {
  transform: translateY(-6px);
  box-shadow: var(--shadow-hover);
}

.project-image {
  position: relative;
  width: 100%;
  height: 220px;
  overflow: hidden;
}

.project-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.5s ease;
}

.project-card:hover .project-image img {
  transform: scale(1.08);
}

.project-overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(180deg, transparent 50%, rgba(0, 0, 0, 0.6));
  display: flex;
  align-items: flex-end;
  padding: 1rem;
}

.project-category {
  font-size: 0.75rem;
  font-weight: 600;
  color: #fff;
  background: var(--accent);
  padding: 0.3rem 1rem;
  border-radius: 20px;
  letter-spacing: 0.3px;
}

.project-body {
  padding: 1.5rem;
  display: flex;
  flex-direction: column;
  flex-grow: 1;
}

.project-tags {
  margin-bottom: 0.75rem;
}

.project-tag {
  display: inline-block;
  font-size: 0.72rem;
  font-weight: 600;
  color: var(--accent);
  background: rgba(37, 99, 235, 0.08);
  padding: 0.25rem 0.8rem;
  border-radius: 12px;
}

.project-title {
  font-size: 1.15rem;
  font-weight: 700;
  color: var(--text-h);
  margin-bottom: 0.6rem;
}

.project-desc {
  font-size: 0.88rem;
  color: var(--text2);
  line-height: 1.6;
  margin: 0;
  flex-grow: 1;
}

.project-link {
  display: inline-flex;
  align-items: center;
  gap: 0.3rem;
  font-size: 0.85rem;
  font-weight: 600;
  color: var(--accent);
  text-decoration: none;
  margin-top: 1rem;
  transition: gap 0.25s ease;
}

.project-link:hover {
  gap: 0.6rem;
}

.project-link .material-icons {
  font-size: 1.15rem;
}
</style>
