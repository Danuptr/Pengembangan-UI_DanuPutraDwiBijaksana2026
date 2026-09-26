<template>
  <div class="about-page">
    <div class="about-header">
      <h1>About Gatherly</h1>
      <p>Building the future of event experiences, one community at a time.</p>
    </div>

    <div class="about-content">
      <div class="text-block">
        <h2>Our Mission</h2>

        <p>
          Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat
          nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia
          deserunt mollit anim id est laborum. Sed ut perspiciatis unde omnis iste natus error sit
          voluptatem accusantium doloremque laudantium.
        </p>
      </div>

      <div class="text-block">
        <h2>Our Vision</h2>

        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer nec odio. Praesent
          libero. Sed cursus ante dapibus diam. Sed nisi. Nulla quis sem at nibh elementum
          imperdiet. Duis sagittis ipsum. Praesent mauris. Fusce nec tellus sed augue semper porta.
        </p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.about-page {
  padding-bottom: 3rem;
}

.about-header {
  background: #fff;
  color: #1c1948;
  padding: 4rem 2rem;
  border-radius: 16px;
  margin-bottom: 2.5rem;
  text-align: center;
  border: 1px solid #e8e8ee;
}

.about-header h1 {
  font-size: 2.4rem;
  font-weight: 800;
  color: #1c1948;
  margin-bottom: 0.75rem;
}

.about-header p {
  color: #64748b;
  font-size: 1.05rem;
}

.about-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2rem;
}

.text-block {
  background: #fff;
  border: 1px solid #e8e8ee;
  border-radius: 16px;
  padding: 2rem;
}

.text-block h2 {
  font-size: 1.35rem;
  font-weight: 700;
  color: #1a1a2e;
  margin-bottom: 1rem;
}

.text-block p {
  color: #64748b;
  line-height: 1.75;
  font-size: 0.95rem;
}

@media (max-width: 768px) {
  .about-content { grid-template-columns: 1fr; }
  .about-header { padding: 3rem 1.5rem; }
  .about-header h1 { font-size: 1.8rem; }
}
</style>
