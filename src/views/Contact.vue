<template>
  <div class="contact-page">
    <div class="contact-header">
      <h1>Contact Us</h1>

      <p>
        We'd love to hear from you. Please fill out the form below or reach out via our contact
        info.
      </p>
    </div>

    <div class="contact-content">
      <div class="contact-info">
        <div class="info-item">
          <div class="info-icon">📍</div>

          <div>
            <h3>Our Office</h3>
            <p>123 Event Street, Tech City, 10101</p>
          </div>
        </div>

        <div class="info-item">
          <div class="info-icon">📞</div>

          <div>
            <h3>Phone</h3>
            <p>+62 812 3456 7890</p>
          </div>
        </div>

        <div class="info-item">
          <div class="info-icon">✉️</div>

          <div>
            <h3>Email</h3>
            <p>hello@gatherly.com</p>
          </div>
        </div>
      </div>

      <div class="contact-form">
        <form @submit.prevent>
          <div class="form-group">
            <label>Name</label>
            <input type="text" placeholder="John Doe" class="form-control" />
          </div>

          <div class="form-group">
            <label>Email</label>
            <input type="email" placeholder="john@example.com" class="form-control" />
          </div>

          <div class="form-group">
            <label>Message</label>
            <textarea placeholder="How can we help you?" rows="5" class="form-control"></textarea>
          </div>

          <button class="btn-submit">Send Message</button>
        </form>
      </div>
    </div>
  </div>
</template>

<style scoped>
.contact-page {
  padding-bottom: 3rem;
}

.contact-header {
  margin-bottom: 2.5rem;
  text-align: center;
}

.contact-header h1 {
  font-size: 2.2rem;
  font-weight: 800;
  color: #1a1a2e;
  margin-bottom: 0.5rem;
}

.contact-header p {
  color: #64748b;
  font-size: 1.05rem;
  max-width: 500px;
  margin: 0 auto;
}

.contact-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2.5rem;
  align-items: start;
}

.contact-info {
  display: flex;
  flex-direction: column;
  gap: 1.25rem;
}

.info-item {
  display: flex;
  align-items: flex-start;
  gap: 1rem;
  background: #fff;
  border: 1px solid #e8e8ee;
  border-radius: 14px;
  padding: 1.25rem;
  transition: all 0.25s ease;
}

.info-item:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.06);
}

.info-icon {
  font-size: 1.5rem;
  flex-shrink: 0;
  width: 48px;
  height: 48px;
  background: #f1f0ff;
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.info-item h3 {
  font-size: 1rem;
  font-weight: 700;
  color: #1a1a2e;
  margin-bottom: 0.25rem;
}

.info-item p {
  color: #64748b;
  font-size: 0.92rem;
}

.contact-form {
  background: #fff;
  border: 1px solid #e8e8ee;
  border-radius: 16px;
  padding: 2rem;
}

.form-group {
  margin-bottom: 1.25rem;
}

.form-group label {
  display: block;
  font-size: 0.9rem;
  font-weight: 600;
  color: #1a1a2e;
  margin-bottom: 0.4rem;
}

.form-control {
  width: 100%;
  padding: 0.75rem 1rem;
  border: 1px solid #e2e8f0;
  border-radius: 10px;
  font-size: 0.95rem;
  font-family: inherit;
  color: #1a1a2e;
  transition: border-color 0.2s;
  background: #fafafa;
}

.form-control:focus {
  outline: none;
  border-color: #6644ff;
  box-shadow: 0 0 0 3px rgba(102, 68, 255, 0.1);
  background: #fff;
}

textarea.form-control {
  resize: vertical;
  min-height: 100px;
}

.btn-submit {
  width: 100%;
  padding: 0.85rem 1.5rem;
  background: #6644ff;
  color: #fff;
  font-weight: 600;
  font-size: 1rem;
  border-radius: 12px;
  border: none;
  cursor: pointer;
  transition: all 0.25s ease;
  box-shadow: 0 4px 16px rgba(102, 68, 255, 0.35);
}

.btn-submit:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 24px rgba(102, 68, 255, 0.5);
  background: #5533ee;
}

@media (max-width: 768px) {
  .contact-content { grid-template-columns: 1fr; }
}
</style>