<template>
  <section id="contact" class="section-padding">
    <div class="container">
      <div class="row">
        <div class="col-lg-5 mb-5 mb-lg-0 text-start">
          <h2 class="fw-bold mb-4">Trabajemos juntos</h2>
          <p class="lead text-muted mb-4">
            ¿Listo para comenzar tu próximo proyecto? Contáctanos hoy para una consulta gratuita.
          </p>
          <div class="contact-info">
            <div class="d-flex align-items-center mb-3">
              <span class="material-icons text-primary me-3">email</span>
              <span class="text-muted">vansmc10@gmail.com</span>
            </div>
            <div class="d-flex align-items-center mb-3">
              <span class="material-icons text-primary me-3">phone</span>
              <span class="text-muted">+51 958653474</span>
            </div>
            <div class="d-flex align-items-center mb-3">
              <span class="material-icons text-primary me-3">U</span>
              <span class="text-muted">Calle F lt. 10 - Chorrillos</span>
            </div>
          </div>
          <div class="social-links mt-4 d-flex gap-3">
            <a href="#"
              class="btn btn-outline-primary btn-sm rounded-circle d-flex align-items-center justify-content-center p-2"><span
                class="material-icons">contact_page</span></a>
            <a href="#"
              class="btn btn-outline-primary btn-sm rounded-circle d-flex align-items-center justify-content-center p-2"><span
                class="material-icons">public</span></a>
            <a href="#"
              class="btn btn-outline-primary btn-sm rounded-circle d-flex align-items-center justify-content-center p-2"><span
                class="material-icons">share</span></a>
          </div>
        </div>
        <div class="col-lg-7">
          <div class="material-card p-4 text-start">
            <h4 class="mb-4 fw-bold">Enviar mensaje</h4>
            <form @submit.prevent="sendEmail">
              <div class="row g-3 mb-3">
                <div class="col-md-6">
                  <label for="name" class="form-label small fw-bold">Nombre</label>
                  <input type="text" class="form-control" id="name" placeholder="Nombre completo" required>
                </div>
                <div class="col-md-6">
                  <label for="email" class="form-label small fw-bold">Email</label>
                  <input type="email" class="form-control" id="email" placeholder="example@email.com" required>
                </div>
              </div>
              <div class="mb-3">
                <label for="subject" class="form-label small fw-bold">Asunto</label>
                <input type="text" class="form-control" id="subject" placeholder="Consulta de proyecto" required>
              </div>
              <div class="mb-4">
                <label for="message" class="form-label small fw-bold">Mensaje</label>
                <textarea class="form-control" id="message" rows="4"
                  placeholder="Cuéntanos cuáles son los objetivos de tu proyecto..." required></textarea>
              </div>
              <!-- <div class="mb-4">
                <label for="brochure" class="form-label small fw-bold">Adjuntar Brochure o Documento (Opcional)</label>
                <div class="input-group">
                  <input type="file" class="form-control" id="brochure" accept=".pdf,.doc,.docx,.xls,.xlsx">
                  <span class="input-group-text bg-light">
                    <span class="material-icons text-primary">attach_file</span>
                  </span>
                </div>
                <small class="text-muted d-block mt-2">Formatos aceptados: PDF, DOC, DOCX, XLS, XLSX (Máx. 10MB)</small>
              </div> -->
              <button type="submit"
                class="btn btn-primary w-100 py-3 d-flex align-items-center justify-content-center gap-2">
                Envia Mensaje <span class="material-icons">enviar</span>
              </button>
            </form>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.form-control {
  background-color: var(--bg-light);
  border: 1px solid #ddd;
}

.form-control:focus {
  background-color: var(--white);
  border: 1px solid var(--primary-color);
  box-shadow: none;
}
</style>
