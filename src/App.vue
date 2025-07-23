<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div class="app">
    <header class="header">
      <div class="container">
        <div class="brand">
          <h1 class="logo">QureLab</h1>
          <p class="tagline">Data-driven insights with precision and clarity</p>
        </div>
        <nav class="nav">
          <RouterLink to="/" class="nav-link">Home</RouterLink>
          <RouterLink to="/about" class="nav-link">About</RouterLink>
        </nav>
      </div>
    </header>
    
    <main class="main">
      <RouterView />
    </main>
    
    <footer class="footer">
      <div class="container">
        <p>&copy; 2024 QureLab. Quantification with purpose.</p>
      </div>
    </footer>
  </div>
</template>

<style scoped>
@font-face {
  font-family: 'Goudy Old Style';
  src: url('./assets/Goudy Old Style Regular.ttf') format('truetype');
  font-weight: normal;
  font-style: normal;
}

.app {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  background: #ffffff;
  color: #1a1a1a;
  font-family: 'Goudy Old Style', Georgia, 'Times New Roman', serif;
  line-height: 1.6;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.header {
  border-bottom: 1px solid #e5e5e5;
  background: rgba(255, 255, 255, 0.95);
  backdrop-filter: blur(10px);
  position: sticky;
  top: 0;
  z-index: 100;
}

.header .container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1.5rem 2rem;
}

.brand {
  display: flex;
  flex-direction: column;
  gap: 0.25rem;
}

.logo {
  font-size: 2.25rem;
  font-weight: 300;
  margin: 0;
  letter-spacing: -0.02em;
  color: #000000;
}

.tagline {
  font-size: 0.875rem;
  color: #666666;
  margin: 0;
  font-weight: 400;
}

.nav {
  display: flex;
  gap: 2rem;
}

.nav-link {
  text-decoration: none;
  color: #666666;
  font-weight: 400;
  font-size: 0.9rem;
  transition: color 0.2s ease;
  position: relative;
}

.nav-link:hover {
  color: #000000;
}

.nav-link.router-link-active {
  color: #000000;
}

.nav-link.router-link-active::after {
  content: '';
  position: absolute;
  bottom: -0.5rem;
  left: 0;
  right: 0;
  height: 1px;
  background: #000000;
}

.main {
  flex: 1;
}

.footer {
  border-top: 1px solid #e5e5e5;
  background: #fafafa;
  margin-top: auto;
}

.footer .container {
  padding: 2rem;
  text-align: center;
}

.footer p {
  margin: 0;
  color: #666666;
  font-size: 0.875rem;
}

@media (max-width: 768px) {
  .header .container {
    flex-direction: column;
    gap: 1rem;
    padding: 1rem 2rem;
  }
  
  .nav {
    gap: 1.5rem;
  }
  
  .container {
    padding: 0 1rem;
  }
}
</style>
