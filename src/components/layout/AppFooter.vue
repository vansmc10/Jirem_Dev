<template>
  <footer class="bg-dark text-white py-5">
    <div class="container py-4">
      <div class="row align-items-center">
        <div class="col-md-4 mb-4 mb-md-0">
          <a class="navbar-brand text-white fw-bold d-flex align-items-center gap-2 mb-3" href="#">
            <span class="material-icons text-primary">analytics</span>
            <span>JiremDev</span>
          </a>
          <p class="text-muted small">
            Impulsamos a las empresas a través de la excelencia digital y la innovación estratégica en software.
          </p>
        </div>
        <div class="col-md-4 mb-4 mb-md-0">
          <h5 class="fw-bold mb-3">Enlaces rápidos</h5>
          <ul class="list-unstyled small">
            <li><a href="#home" class="text-muted text-decoration-none">Home</a></li>
            <li><a href="#services" class="text-muted text-decoration-none">Servicios</a></li>
            <li><a href="#about" class="text-muted text-decoration-none">Nosotros</a></li>
            <li><a href="#projects" class="text-muted text-decoration-none">Projectos</a></li>
          </ul>
        </div>
        <div class="col-md-4">
          <h5 class="fw-bold mb-3">Subscribe</h5>
          <p class="text-muted small">Recibe las últimas novedades tecnológicas directamente en tu correo electrónico.
          </p>
          <div class="input-group mb-3">
            <input type="email" class="form-control form-control-sm bg-dark text-white border-secondary"
              placeholder="Email Address">
            <button class="btn btn-primary btn-sm px-3" type="button">Join</button>
          </div>
        </div>
      </div>
      <hr class="my-4 border-secondary opacity-25">
      <div class="row align-items-center">
        <div class="col-md-6 small text-muted text-center text-md-start">
          &copy; 2026 JiremDev. Todos los derechos reservados.
        </div>
        <div class="col-md-6 text-center text-md-end pt-3 pt-md-0">
          <a href="#" class="text-muted text-decoration-none ms-3"><small>Política de Privacidad</small></a>
          <a href="#" class="text-muted text-decoration-none ms-3"><small>Términos de Servicio</small></a>
        </div>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.bg-dark {
  background-color: #1a1a1a !important;
}

.text-muted {
  color: #999 !important;
}

li {
  margin-bottom: 0.5rem;
}

li a:hover {
  color: var(--primary-color) !important;
}
</style>
