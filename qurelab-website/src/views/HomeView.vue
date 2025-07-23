<script setup lang="ts">
// No imports needed for this minimal design
</script>

<template>
  <div class="home">
    <!-- Hero Section -->
    <section class="hero">
      <div class="container">
        <div class="hero-content">
          <h1 class="hero-title">
            Quantifying complexity<br>
            with <span class="highlight">clarity</span>
          </h1>
          <p class="hero-description">
            QureLab transforms data into actionable insights through disciplined analysis,
            precise methodology, and unwavering commitment to truth.
          </p>
          <div class="hero-actions">
            <button class="btn-primary">Explore Our Work</button>
            <button class="btn-secondary">Learn More</button>
          </div>
        </div>
        <div class="hero-visual">
          <div class="data-grid">
            <div class="grid-item" v-for="i in 12" :key="i"></div>
          </div>
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section class="features">
      <div class="container">
        <div class="section-header">
          <h2 class="section-title">Our Approach</h2>
          <p class="section-subtitle">
            Every data question deserves methodical exploration and honest answers.
          </p>
        </div>
        
        <div class="features-grid">
          <div class="feature">
            <div class="feature-icon">
              <div class="icon-precision"></div>
            </div>
            <h3 class="feature-title">Precision</h3>
            <p class="feature-description">
              Rigorous methodology ensures every analysis meets the highest standards of accuracy.
            </p>
          </div>
          
          <div class="feature">
            <div class="feature-icon">
              <div class="icon-clarity"></div>
            </div>
            <h3 class="feature-title">Clarity</h3>
            <p class="feature-description">
              Complex insights delivered through clean, understandable visualizations and reports.
            </p>
          </div>
          
          <div class="feature">
            <div class="feature-icon">
              <div class="icon-trust"></div>
            </div>
            <h3 class="feature-title">Trust</h3>
            <p class="feature-description">
              Transparent processes and honest interpretation of results, even when inconvenient.
            </p>
          </div>
          
          <div class="feature">
            <div class="feature-icon">
              <div class="icon-innovation"></div>
            </div>
            <h3 class="feature-title">Innovation</h3>
            <p class="feature-description">
              Embracing cutting-edge methodologies and technologies to deliver superior analytical solutions.
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Stats Section -->
    <section class="stats">
      <div class="container">
        <div class="stats-grid">
          <div class="stat">
            <div class="stat-number">99.7%</div>
            <div class="stat-label">Accuracy Rate</div>
          </div>
          <div class="stat">
            <div class="stat-number">500+</div>
            <div class="stat-label">Projects Completed</div>
          </div>
          <div class="stat">
            <div class="stat-number">24/7</div>
            <div class="stat-label">Data Monitoring</div>
          </div>
          <div class="stat">
            <div class="stat-number">∞</div>
            <div class="stat-label">Possibilities</div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
.home {
  background: #ffffff;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

/* Hero Section */
.hero {
  padding: 6rem 0 8rem;
  background: linear-gradient(135deg, #fafafa 0%, #ffffff 100%);
}

.hero .container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;
}

.hero-title {
  font-size: 3.5rem;
  font-weight: 300;
  line-height: 1.1;
  margin: 0 0 1.5rem;
  color: #1a1a1a;
  letter-spacing: -0.02em;
}

.highlight {
  color: #000000;
  font-weight: 400;
  position: relative;
}

.highlight::after {
  content: '';
  position: absolute;
  bottom: 0.1em;
  left: 0;
  right: 0;
  height: 2px;
  background: #000000;
}

.hero-description {
  font-size: 1.125rem;
  line-height: 1.7;
  color: #666666;
  margin: 0 0 2.5rem;
  max-width: 90%;
}

.hero-actions {
  display: flex;
  gap: 1rem;
}

.btn-primary {
  background: #000000;
  color: #ffffff;
  border: none;
  padding: 0.875rem 2rem;
  font-size: 0.9rem;
  font-weight: 500;
  cursor: pointer;
  transition: all 0.2s ease;
  border-radius: 0;
}

.btn-primary:hover {
  background: #333333;
  transform: translateY(-1px);
}

.btn-secondary {
  background: transparent;
  color: #000000;
  border: 1px solid #000000;
  padding: 0.875rem 2rem;
  font-size: 0.9rem;
  font-weight: 500;
  cursor: pointer;
  transition: all 0.2s ease;
  border-radius: 0;
}

.btn-secondary:hover {
  background: #000000;
  color: #ffffff;
  transform: translateY(-1px);
}

/* Data Grid Visualization */
.hero-visual {
  display: flex;
  justify-content: center;
  align-items: center;
}

.data-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1rem;
  padding: 2rem;
}

.grid-item {
  width: 60px;
  height: 60px;
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  transition: all 0.3s ease;
  animation: pulse 3s infinite;
}

.grid-item:nth-child(odd) {
  animation-delay: 0.5s;
}

.grid-item:nth-child(3n) {
  animation-delay: 1s;
}

@keyframes pulse {
  0%, 100% { background: #f5f5f5; }
  50% { background: #e5e5e5; }
}

/* Features Section */
.features {
  padding: 6rem 0;
  background: #fafafa;
}

.section-header {
  text-align: center;
  margin-bottom: 4rem;
}

.section-title {
  font-size: 2.5rem;
  font-weight: 300;
  margin: 0 0 1rem;
  color: #1a1a1a;
  letter-spacing: -0.01em;
}

.section-subtitle {
  font-size: 1.125rem;
  color: #666666;
  margin: 0;
  max-width: 600px;
  margin: 0 auto;
}

.features-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 3rem;
  max-width: 800px;
  margin: 0 auto;
}

.feature {
  text-align: center;
  padding: 2rem;
}

.feature-icon {
  width: 80px;
  height: 80px;
  margin: 0 auto 1.5rem;
  display: flex;
  align-items: center;
  justify-content: center;
}

.icon-precision,
.icon-clarity,
.icon-trust,
.icon-innovation {
  width: 40px;
  height: 40px;
  border: 2px solid #000000;
}

.icon-precision {
  border-radius: 0;
  background: linear-gradient(45deg, transparent 30%, #000000 30%, #000000 70%, transparent 70%);
}

.icon-clarity {
  border-radius: 50%;
  background: radial-gradient(circle, transparent 40%, #000000 40%, #000000 60%, transparent 60%);
}

.icon-trust {
  clip-path: polygon(50% 0%, 0% 100%, 100% 100%);
  background: #000000;
  border: none;
}

.icon-innovation {
  border-radius: 0;
  background: conic-gradient(from 0deg, #000000 0deg, transparent 90deg, #000000 180deg, transparent 270deg);
  transform: rotate(45deg);
}

.feature-title {
  font-size: 1.25rem;
  font-weight: 500;
  margin: 0 0 1rem;
  color: #1a1a1a;
}

.feature-description {
  color: #666666;
  line-height: 1.6;
  margin: 0;
}

/* Stats Section */
.stats {
  padding: 4rem 0;
  background: #ffffff;
  border-top: 1px solid #e5e5e5;
  border-bottom: 1px solid #e5e5e5;
}

.stats-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 2rem;
}

.stat {
  text-align: center;
  padding: 1rem;
}

.stat-number {
  font-size: 3rem;
  font-weight: 300;
  color: #000000;
  margin-bottom: 0.5rem;
  letter-spacing: -0.02em;
}

.stat-label {
  font-size: 0.875rem;
  color: #666666;
  text-transform: uppercase;
  letter-spacing: 0.1em;
}

/* Responsive Design */
@media (max-width: 768px) {
  .hero .container {
    grid-template-columns: 1fr;
    gap: 3rem;
    text-align: center;
  }
  
  .hero {
    padding: 4rem 0 5rem;
  }
  
  .hero-title {
    font-size: 2.5rem;
  }
  
  .hero-actions {
    flex-direction: column;
    align-items: center;
  }
  
  .btn-primary,
  .btn-secondary {
    width: 100%;
    max-width: 300px;
  }
  
  .data-grid {
    grid-template-columns: repeat(3, 1fr);
    gap: 0.75rem;
    padding: 1rem;
  }
  
  .grid-item {
    width: 40px;
    height: 40px;
  }
  
  .features {
    padding: 4rem 0;
  }
  
  .features-grid {
    grid-template-columns: 1fr;
    gap: 2rem;
    max-width: none;
  }
  
  .section-title {
    font-size: 2rem;
  }
  
  .stats-grid {
    grid-template-columns: repeat(2, 1fr);
  }
  
  .stat-number {
    font-size: 2.5rem;
  }
}

@media (max-width: 480px) {
  .container {
    padding: 0 1rem;
  }
  
  .hero-title {
    font-size: 2rem;
  }
  
  .stats-grid {
    grid-template-columns: 1fr;
  }
}
</style>
