<template>
  <div class="home-page">
    <section class="hero">
      <div class="hero-content">
        <span class="badge">Welcome to Gatherly</span>

        <h1 class="hero-title">Connect, Discover, and Experience</h1>

        <p class="hero-subtitle">
          Join our vibrant community to explore the best events tailored for you. Lorem ipsum dolor
          sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et
          dolore magna aliqua.
        </p>

        <div class="hero-actions">
          <router-link to="/browse/events" class="btn btn-primary"> Discover Events </router-link>

          <router-link to="/about" class="btn btn-secondary"> Learn More </router-link>
        </div>
      </div>
    </section>

    <section class="features">
      <div class="feature-card" v-for="(feat, index) in featureList" :key="index">
        <div class="feature-icon">{{ feat.icon }}</div>
        <h3>{{ feat.title }}</h3>
        <p>{{ feat.desc }}</p>
      </div>
    </section>

    <section class="sitemap-visual">
      <h2>Website Structure / Site-Map</h2>

      <p class="sitemap-desc">
        A quick overview of how this application is structured via Vue Router.
      </p>

      <ul class="tree">
        <li>
          <router-link to="/">Home</router-link>
          <ul>
            <li><router-link to="/about">About</router-link></li>
            <li>
              <router-link to="/browse">Browse</router-link>
              <ul>
                <li>
                  <router-link to="/browse/events">Event List</router-link>
                  <ul>
                    <li><router-link to="/browse/events/1">Event Detail (Example)</router-link></li>
                  </ul>
                </li>
                <li><router-link to="/browse/category">Category</router-link></li>
              </ul>
            </li>
            <li><router-link to="/contact">Contact</router-link></li>
          </ul>
        </li>
      </ul>
    </section>
  </div>
</template>

<script setup>
const featureList = [
  {
    icon: '🎵',
    title: 'Curated Events',
    desc: 'Up event ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
  },
  {
    icon: '🌏',
    title: 'Global Reach',
    desc: 'Up event ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
  },
  {
    icon: '🤝',
    title: 'Community Driven',
    desc: 'Up event ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
  },
]
</script>

<style scoped>
.home-page {
  padding-bottom: 3rem;
}

/* Hero */
.hero {
  background: #fff;
  color: #1c1948;
  padding: 5rem 2rem;
  border-radius: 16px;
  margin-bottom: 3rem;
  text-align: center;
  border: 1px solid #e8e8ee;
}

.hero-content {
  max-width: 700px;
  margin: 0 auto;
}

.badge {
  display: inline-block;
  background: rgba(28, 25, 72, 0.08);
  color: #6644ff;
  padding: 0.4rem 1.2rem;
  border-radius: 100px;
  font-size: 0.85rem;
  font-weight: 600;
  margin-bottom: 1.5rem;
  border: 1px solid rgba(28, 25, 72, 0.12);
}

.hero-title {
  font-size: 2.8rem;
  font-weight: 800;
  line-height: 1.15;
  margin-bottom: 1.25rem;
  color: #1c1948;
}

.hero-subtitle {
  font-size: 1.05rem;
  color: #64748b;
  line-height: 1.7;
  margin-bottom: 2rem;
}

.hero-actions {
  display: flex;
  gap: 1rem;
  justify-content: center;
  flex-wrap: wrap;
}

.btn {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.8rem 1.8rem;
  font-weight: 600;
  font-size: 0.95rem;
  border-radius: 12px;
  text-decoration: none;
  transition: all 0.25s ease;
  cursor: pointer;
  border: none;
}

.btn-primary {
  background: #6644ff;
  color: #fff;
  box-shadow: 0 4px 16px rgba(102, 68, 255, 0.35);
}

.btn-primary:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 24px rgba(102, 68, 255, 0.5);
  background: #5533ee;
}

.btn-secondary {
  background: rgba(28, 25, 72, 0.06);
  color: #1c1948;
  border: 1px solid rgba(28, 25, 72, 0.2);
}

.btn-secondary:hover {
  background: rgba(28, 25, 72, 0.12);
  transform: translateY(-2px);
}

/* Features */
.features {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
  margin-bottom: 3rem;
}

.feature-card {
  background: #fff;
  border: 1px solid #e8e8ee;
  border-radius: 16px;
  padding: 2rem;
  transition: all 0.3s ease;
}

.feature-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 12px 32px rgba(0, 0, 0, 0.08);
  border-color: #6644ff;
}

.feature-icon {
  font-size: 2rem;
  margin-bottom: 1rem;
}

.feature-card h3 {
  font-size: 1.15rem;
  font-weight: 700;
  color: #1a1a2e;
  margin-bottom: 0.5rem;
}

.feature-card p {
  color: #64748b;
  font-size: 0.92rem;
  line-height: 1.6;
}

/* Sitemap */
.sitemap-visual {
  background: #fff;
  border: 1px solid #e8e8ee;
  border-radius: 16px;
  padding: 2rem;
}

.sitemap-visual h2 {
  font-size: 1.5rem;
  font-weight: 700;
  color: #1a1a2e;
  margin-bottom: 0.5rem;
}

.sitemap-desc {
  color: #64748b;
  margin-bottom: 1.5rem;
  font-size: 0.95rem;
}

.tree {
  list-style: disc;
  padding-left: 1.25rem;
}

.tree ul {
  list-style: circle;
  padding-left: 1.5rem;
  margin-top: 0.25rem;
}

.tree ul ul {
  list-style: square;
}

.tree li {
  margin-bottom: 0.35rem;
}

.tree a {
  color: #6644ff;
  font-weight: 500;
  text-decoration: none;
  transition: color 0.2s;
}

.tree a:hover {
  color: #4422cc;
  text-decoration: underline;
}

@media (max-width: 768px) {
  .hero-title {
    font-size: 2rem;
  }
  .features {
    grid-template-columns: 1fr;
  }
  .hero {
    padding: 3rem 1.5rem;
  }
}
</style>
