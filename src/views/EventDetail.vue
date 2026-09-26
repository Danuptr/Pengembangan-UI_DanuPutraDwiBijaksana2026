<template>
  <div class="event-detail-page">
    <button @click="$router.push('/browse/events')" class="btn-back">← Back to Events</button>

    <div class="detail-header">
      <div class="header-content">
        <span class="event-tag"> Community Event </span>

        <h1>Community Gathering {{ $route.params.id }}</h1>

        <div class="meta-info">
          <div class="meta-item">
            <span class="icon">📅</span>
            <span>October 15, 2026</span>
          </div>

          <div class="meta-item">
            <span class="icon">📍</span>
            <span>Main Auditorium, City Center</span>
          </div>

          <div class="meta-item">
            <span class="icon">👥</span>
            <span>500+ Attendees</span>
          </div>
        </div>
      </div>
    </div>

    <div class="detail-content">
      <div class="main-desc">
        <h2>About This Event</h2>

        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam id mauris. Vivamus
          hendrerit arcu sed erat molestie vehicula. Sed auctor neque eu tellus rhoncus ut eleifend
          nibh porttitor. Ut in nulla enim. Phasellus molestie magna non est bibendum non venenatis
          nisl tempor.
        </p>

        <p>
          Suspendisse dictum feugiat nisl ut dapibus. Mauris iaculis porttitor posuere. Praesent id
          metus massa, ut blandit odio. Proin quis tortor orci. Etiam at risus et justo dignissim
          consectetur.
        </p>

        <h2>Agenda</h2>

        <ul class="agenda-list">
          <li><strong>09:00 AM</strong> - Registration & Welcome Coffee</li>
          <li><strong>10:00 AM</strong> - Opening Keynote</li>
          <li><strong>11:30 AM</strong> - Networking Session</li>
          <li><strong>01:00 PM</strong> - Closing Remarks</li>
        </ul>
      </div>

      <div class="sidebar">
        <div class="ticket-card">
          <h3>Registration</h3>
          <p class="price">Free</p>
          <p class="ticket-desc">Secure your spot today before it runs out.</p>
          <button class="btn-register">Register Now</button>
          <p class="spots">Only 45 spots left</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.event-detail-page {
  padding-bottom: 3rem;
}

.btn-back {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: none;
  border: 1px solid #e2e8f0;
  color: #64748b;
  padding: 0.5rem 1rem;
  border-radius: 10px;
  font-size: 0.9rem;
  font-weight: 500;
  cursor: pointer;
  margin-bottom: 2rem;
  transition: all 0.2s;
}

.btn-back:hover {
  background: #f8fafc;
  color: #1a1a2e;
  border-color: #cbd5e1;
}

.detail-header {
  background: #fff;
  border-radius: 16px;
  padding: 3rem 2.5rem;
  color: #1c1948;
  margin-bottom: 2rem;
  border: 1px solid #e8e8ee;
}

.event-tag {
  display: inline-block;
  background: rgba(28, 25, 72, 0.08);
  color: #6644ff;
  padding: 0.3rem 1rem;
  border-radius: 100px;
  font-size: 0.82rem;
  font-weight: 600;
  margin-bottom: 1rem;
}

.detail-header h1 {
  font-size: 2.2rem;
  font-weight: 800;
  color: #1c1948;
  margin-bottom: 1.25rem;
}

.meta-info {
  display: flex;
  gap: 2rem;
  flex-wrap: wrap;
}

.meta-item {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  color: #64748b;
  font-size: 0.92rem;
}

.meta-item .icon {
  font-size: 1.1rem;
}

.detail-content {
  display: grid;
  grid-template-columns: 1fr 340px;
  gap: 2rem;
  align-items: start;
}

.main-desc {
  background: #fff;
  border: 1px solid #e8e8ee;
  border-radius: 16px;
  padding: 2rem;
}

.main-desc h2 {
  font-size: 1.35rem;
  font-weight: 700;
  color: #1a1a2e;
  margin-bottom: 1rem;
  margin-top: 1.5rem;
}

.main-desc h2:first-child {
  margin-top: 0;
}

.main-desc p {
  color: #64748b;
  line-height: 1.75;
  font-size: 0.95rem;
  margin-bottom: 0.75rem;
}

.agenda-list {
  list-style: none;
  padding: 0;
}

.agenda-list li {
  padding: 0.75rem 0;
  border-bottom: 1px solid #f1f5f9;
  color: #475569;
  font-size: 0.95rem;
}

.agenda-list li:last-child {
  border-bottom: none;
}

.agenda-list li strong {
  color: #6644ff;
  font-weight: 700;
}

.ticket-card {
  background: #fff;
  border: 1px solid #e8e8ee;
  border-radius: 16px;
  padding: 2rem;
  text-align: center;
}

.ticket-card h3 {
  font-size: 1.15rem;
  font-weight: 700;
  color: #1a1a2e;
  margin-bottom: 0.5rem;
}

.price {
  font-size: 2rem;
  font-weight: 800;
  color: #10b981;
  margin-bottom: 0.5rem;
}

.ticket-desc {
  color: #94a3b8;
  font-size: 0.9rem;
  margin-bottom: 1.5rem;
}

.btn-register {
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
  margin-bottom: 0.75rem;
}

.btn-register:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 24px rgba(102, 68, 255, 0.5);
  background: #5533ee;
}

.spots {
  color: #ef4444;
  font-size: 0.85rem;
  font-weight: 600;
}

@media (max-width: 768px) {
  .detail-content { grid-template-columns: 1fr; }
  .detail-header { padding: 2rem 1.5rem; }
  .detail-header h1 { font-size: 1.7rem; }
  .meta-info { gap: 1rem; }
}
</style>