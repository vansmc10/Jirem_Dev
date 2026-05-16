<template>
  <section id="contact" class="section-padding bg-light">
    <div class="container">
      <div class="row">
        <div class="col-lg-5 mb-5 mb-lg-0">
          <h2 class="fw-bold mb-4">Let's Work Together</h2>
          <p class="lead text-muted mb-4">
            Ready to start your next project? Get in touch with us today for a free consultation.
          </p>
          <div class="contact-info">
            <div class="d-flex align-items-center mb-3">
              <span class="material-icons text-primary me-3">email</span>
              <span class="text-muted">contact@consultantpro.com</span>
            </div>
            <div class="d-flex align-items-center mb-3">
              <span class="material-icons text-primary me-3">phone</span>
              <span class="text-muted">+1 (555) 123-4567</span>
            </div>
            <div class="d-flex align-items-center mb-3">
              <span class="material-icons text-primary me-3">location_on</span>
              <span class="text-muted">123 Tech Avenue, Silicon Valley, CA</span>
            </div>
          </div>
          <div class="social-links mt-4 d-flex gap-3">
            <a href="#" class="btn btn-outline-primary btn-sm rounded-circle"><span class="material-icons p-1">facebook</span></a>
            <a href="#" class="btn btn-outline-primary btn-sm rounded-circle"><span class="material-icons p-1">language</span></a>
            <a href="#" class="btn btn-outline-primary btn-sm rounded-circle"><span class="material-icons p-1">share</span></a>
          </div>
        </div>
        <div class="col-lg-7">
          <div class="material-card p-4">
            <h4 class="mb-4">Send a Message</h4>
            <form>
              <div class="row g-3 mb-3">
                <div class="col-md-6">
                  <label for="name" class="form-label small fw-bold">Name</label>
                  <input type="text" class="form-control" id="name" placeholder="Full Name" required>
                </div>
                <div class="col-md-6">
                  <label for="email" class="form-label small fw-bold">Email</label>
                  <input type="email" class="form-control" id="email" placeholder="example@email.com" required>
                </div>
              </div>
              <div class="mb-3">
                <label for="subject" class="form-label small fw-bold">Subject</label>
                <input type="text" class="form-control" id="subject" placeholder="Project Inquiry" required>
              </div>
              <div class="mb-4">
                <label for="message" class="form-label small fw-bold">Message</label>
                <textarea class="form-control" id="message" rows="4" placeholder="Tell us about your project goals..." required></textarea>
              </div>
              <button type="submit" class="btn btn-primary w-100 py-3 d-flex align-items-center justify-content-center gap-2">
                Send Message <span class="material-icons">send</span>
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
  border: 1px solid transparent;
}

.form-control:focus {
  background-color: var(--white);
  border: 1px solid var(--primary-color);
}
</style>
