<template>
  <div class="event-list-page">
    <div class="section-header">
      <h2 class="section-title">Upcoming Events</h2>
      <p class="section-desc">Discover the latest gatherings and activities happening near you.</p>
    </div>

    <div class="event-grid">
      <div class="event-card" v-for="i in 6" :key="i">
        <div class="event-body">
          <div class="event-meta">
            <span class="event-date"> Oct {{ 10 + i }}, 2026 </span>
            <span class="event-category"> Community </span>
          </div>

          <h3>Community Gathering {{ i }}</h3>

          <p class="event-loc">📍 Main Auditorium, City Center</p>

          <p class="event-desc">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam at velit vel magna
            interdum scelerisque.
          </p>

          <div class="card-footer">
            <router-link :to="'/browse/events/' + i" class="btn-link"> View Details → </router-link>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.event-list-page {
  padding-bottom: 2rem;
}

.section-header {
  margin-bottom: 2rem;
}

.section-title {
  font-size: 1.6rem;
  font-weight: 700;
  color: #1a1a2e;
  margin-bottom: 0.35rem;
}

.section-desc {
  color: #64748b;
  font-size: 0.95rem;
}

.event-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
  gap: 1.5rem;
}

.event-card {
  background: #fff;
  border: 1px solid #e8e8ee;
  border-radius: 16px;
  overflow: hidden;
  transition: all 0.3s ease;
}

.event-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 12px 32px rgba(0, 0, 0, 0.08);
  border-color: #6644ff;
}

.event-body {
  padding: 1.5rem;
}

.event-meta {
  display: flex;
  gap: 0.75rem;
  margin-bottom: 0.75rem;
}

.event-date {
  background: #f1f0ff;
  color: #6644ff;
  padding: 0.25rem 0.75rem;
  border-radius: 100px;
  font-size: 0.8rem;
  font-weight: 600;
}

.event-category {
  background: #ecfdf5;
  color: #10b981;
  padding: 0.25rem 0.75rem;
  border-radius: 100px;
  font-size: 0.8rem;
  font-weight: 600;
}

.event-body h3 {
  font-size: 1.15rem;
  font-weight: 700;
  color: #1a1a2e;
  margin-bottom: 0.5rem;
}

.event-loc {
  font-size: 0.85rem;
  color: #94a3b8;
  margin-bottom: 0.5rem;
}

.event-desc {
  color: #64748b;
  font-size: 0.9rem;
  line-height: 1.6;
  margin-bottom: 1rem;
}

.card-footer {
  padding-top: 0.75rem;
  border-top: 1px solid #f1f5f9;
}

.btn-link {
  color: #6644ff;
  font-weight: 600;
  font-size: 0.9rem;
  text-decoration: none;
  transition: color 0.2s;
}

.btn-link:hover {
  color: #4422cc;
}

@media (max-width: 768px) {
  .event-grid {
    grid-template-columns: 1fr;
  }
}
</style>
