<template>
  <div class="category-page">
    <h2 class="section-title">Explore by Category</h2>

    <div class="category-grid">
      <div class="category-card" v-for="(cat, index) in categories" :key="index">
        <div class="cat-icon">{{ cat.icon }}</div>

        <h3>{{ cat.name }}</h3>

        <p>{{ cat.count }} Events</p>
      </div>
    </div>
  </div>
</template>

<script setup>
const categories = [
  { name: 'Music & Concerts', icon: '\uD83C\uDFB5', count: 24 },
  { name: 'Technology', icon: '\uD83D\uDCBB', count: 18 },
  { name: 'Art & Design', icon: '\uD83C\uDFA8', count: 12 },
  { name: 'Business', icon: '\uD83D\uDCBC', count: 30 },
  { name: 'Health & Wellness', icon: '\uD83C\uDFCB', count: 15 },
  { name: 'Food & Drink', icon: '\uD83C\uDF7D', count: 22 },
]
</script>

<style scoped>
.category-page {
  padding-bottom: 2rem;
}

.section-title {
  font-size: 1.6rem;
  font-weight: 700;
  color: #1a1a2e;
  margin-bottom: 1.5rem;
}

.category-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
}

.category-card {
  background: #fff;
  border: 1px solid #e8e8ee;
  border-radius: 16px;
  padding: 2rem;
  text-align: center;
  transition: all 0.3s ease;
  cursor: pointer;
}

.category-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 12px 32px rgba(0, 0, 0, 0.08);
  border-color: #6644ff;
}

.cat-icon {
  font-size: 2.5rem;
  margin-bottom: 0.75rem;
}

.category-card h3 {
  font-size: 1.1rem;
  font-weight: 700;
  color: #1a1a2e;
  margin-bottom: 0.25rem;
}

.category-card p {
  color: #94a3b8;
  font-size: 0.88rem;
}

@media (max-width: 768px) {
  .category-grid { grid-template-columns: 1fr 1fr; }
}

@media (max-width: 480px) {
  .category-grid { grid-template-columns: 1fr; }
}
</style>
