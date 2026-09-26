<template>
  <div class="browse-page">
    <div class="browse-header">
      <h1>Browse & Discover</h1>

      <p>Find the events and categories that matter most to you.</p>
    </div>

    <div class="browse-content">
      <router-view></router-view>
    </div>
  </div>
</template>

<style scoped>
.browse-page {
  padding-bottom: 3rem;
}

.browse-header {
  margin-bottom: 2rem;
}

.browse-header h1 {
  font-size: 2rem;
  font-weight: 800;
  color: #1a1a2e;
  margin-bottom: 0.5rem;
}

.browse-header p {
  color: #64748b;
  font-size: 1.05rem;
}
</style>
