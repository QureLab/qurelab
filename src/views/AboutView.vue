<template>
  <div class="about">
    <!-- Hero Section -->
    <section class="about-hero">
      <div class="container">
        <div class="hero-content">
          <h1 class="page-title">About QureLab</h1>
          <p class="page-subtitle">
            Founded on the principle that every data question deserves methodical exploration and honest answers.
          </p>
        </div>
      </div>
    </section>

    <!-- Mission Section -->
    <section class="mission">
      <div class="container">
        <div class="content-grid">
          <div class="content-text">
            <h2 class="section-title">Our Mission</h2>
            <p class="section-description">
              We believe in the power of disciplined analysis to reveal truth within complexity. 
              Our approach combines rigorous methodology with clear communication, ensuring that 
              insights are not only accurate but also actionable.
            </p>
            <p class="section-description">
              Every project begins with careful listening and ends with transparent reporting. 
              We handle data with the respect it deserves—as a reflection of real phenomena 
              that demands honest interpretation.
            </p>
          </div>
          <div class="content-visual">
            <div class="visual-element">
              <div class="data-flow">
                <div class="flow-item" v-for="i in 6" :key="i"></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Values Section -->
    <section class="values">
      <div class="container">
        <h2 class="section-title centered">Our Values</h2>
        <div class="values-grid">
          <div class="value">
            <h3 class="value-title">Methodical Rigor</h3>
            <p class="value-description">
              Every analysis follows established protocols and best practices, 
              ensuring reproducible and reliable results.
            </p>
          </div>
          <div class="value">
            <h3 class="value-title">Transparent Process</h3>
            <p class="value-description">
              We document our methods, assumptions, and limitations clearly, 
              allowing for informed decision-making.
            </p>
          </div>
          <div class="value">
            <h3 class="value-title">Honest Interpretation</h3>
            <p class="value-description">
              We report what the data shows, not what stakeholders hope to hear, 
              maintaining integrity above convenience.
            </p>
          </div>
          <div class="value">
            <h3 class="value-title">Continuous Learning</h3>
            <p class="value-description">
              We stay current with evolving methodologies and technologies, 
              constantly refining our approach to analysis.
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Team Section -->
    <section class="team">
      <div class="container">
        <h2 class="section-title centered">Our Approach</h2>
        <div class="approach-timeline">
          <div class="timeline-item">
            <div class="timeline-number">01</div>
            <div class="timeline-content">
              <h3 class="timeline-title">Listen & Understand</h3>
              <p class="timeline-description">
                We begin by carefully understanding your questions, constraints, and context.
              </p>
            </div>
          </div>
          <div class="timeline-item">
            <div class="timeline-number">02</div>
            <div class="timeline-content">
              <h3 class="timeline-title">Design & Plan</h3>
              <p class="timeline-description">
                We develop a methodical approach tailored to your specific analytical needs.
              </p>
            </div>
          </div>
          <div class="timeline-item">
            <div class="timeline-number">03</div>
            <div class="timeline-content">
              <h3 class="timeline-title">Analyze & Validate</h3>
              <p class="timeline-description">
                We execute our analysis with precision and validate results through multiple approaches.
              </p>
            </div>
          </div>
          <div class="timeline-item">
            <div class="timeline-number">04</div>
            <div class="timeline-content">
              <h3 class="timeline-title">Communicate & Guide</h3>
              <p class="timeline-description">
                We present findings clearly and guide you toward informed, data-driven decisions.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
.about {
  background: #ffffff;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

/* Hero Section */
.about-hero {
  padding: 6rem 0 4rem;
  background: linear-gradient(135deg, #fafafa 0%, #ffffff 100%);
  text-align: center;
}

.page-title {
  font-size: 3rem;
  font-weight: 300;
  margin: 0 0 1.5rem;
  color: #1a1a1a;
  letter-spacing: -0.02em;
}

.page-subtitle {
  font-size: 1.25rem;
  color: #666666;
  margin: 0;
  max-width: 700px;
  margin: 0 auto;
  line-height: 1.6;
}

/* Mission Section */
.mission {
  padding: 6rem 0;
  background: #ffffff;
}

.content-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;
}

.section-title {
  font-size: 2.25rem;
  font-weight: 300;
  margin: 0 0 2rem;
  color: #1a1a1a;
  letter-spacing: -0.01em;
}

.section-title.centered {
  text-align: center;
  margin-bottom: 3rem;
}

.section-description {
  font-size: 1.125rem;
  line-height: 1.7;
  color: #666666;
  margin: 0 0 1.5rem;
}

.section-description:last-child {
  margin-bottom: 0;
}

/* Visual Elements */
.visual-element {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 2rem;
}

.data-flow {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.flow-item {
  width: 200px;
  height: 8px;
  background: #f0f0f0;
  position: relative;
  overflow: hidden;
}

.flow-item::after {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, #000000, transparent);
  animation: flow 2s infinite;
  animation-delay: calc(var(--i, 0) * 0.3s);
}

.flow-item:nth-child(1)::after { --i: 0; }
.flow-item:nth-child(2)::after { --i: 1; }
.flow-item:nth-child(3)::after { --i: 2; }
.flow-item:nth-child(4)::after { --i: 3; }
.flow-item:nth-child(5)::after { --i: 4; }
.flow-item:nth-child(6)::after { --i: 5; }

@keyframes flow {
  0% { left: -100%; }
  100% { left: 100%; }
}

/* Values Section */
.values {
  padding: 6rem 0;
  background: #fafafa;
}

.values-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2.5rem;
}

.value {
  background: #ffffff;
  padding: 2.5rem 2rem;
  border: 1px solid #e5e5e5;
  transition: all 0.3s ease;
}

.value:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.1);
}

.value-title {
  font-size: 1.25rem;
  font-weight: 500;
  margin: 0 0 1rem;
  color: #1a1a1a;
}

.value-description {
  color: #666666;
  line-height: 1.6;
  margin: 0;
}

/* Timeline Section */
.team {
  padding: 6rem 0;
  background: #ffffff;
}

.approach-timeline {
  max-width: 800px;
  margin: 0 auto;
}

.timeline-item {
  display: grid;
  grid-template-columns: 80px 1fr;
  gap: 2rem;
  margin-bottom: 3rem;
  position: relative;
}

.timeline-item:not(:last-child)::after {
  content: '';
  position: absolute;
  left: 39px;
  top: 80px;
  width: 2px;
  height: calc(100% + 1rem);
  background: #e5e5e5;
}

.timeline-number {
  width: 60px;
  height: 60px;
  border: 2px solid #000000;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.125rem;
  font-weight: 500;
  color: #000000;
  background: #ffffff;
  position: relative;
  z-index: 1;
}

.timeline-title {
  font-size: 1.5rem;
  font-weight: 500;
  margin: 0 0 0.75rem;
  color: #1a1a1a;
}

.timeline-description {
  color: #666666;
  line-height: 1.6;
  margin: 0;
  font-size: 1.125rem;
}

/* Responsive Design */
@media (max-width: 768px) {
  .about-hero {
    padding: 4rem 0 3rem;
  }
  
  .page-title {
    font-size: 2.5rem;
  }
  
  .content-grid {
    grid-template-columns: 1fr;
    gap: 3rem;
  }
  
  .mission {
    padding: 4rem 0;
  }
  
  .values {
    padding: 4rem 0;
  }
  
  .team {
    padding: 4rem 0;
  }
  
  .values-grid {
    grid-template-columns: 1fr;
    gap: 2rem;
  }
  
  .value {
    padding: 2rem 1.5rem;
  }
  
  .timeline-item {
    grid-template-columns: 60px 1fr;
    gap: 1.5rem;
    margin-bottom: 2.5rem;
  }
  
  .timeline-item:not(:last-child)::after {
    left: 29px;
    top: 70px;
  }
  
  .timeline-number {
    width: 50px;
    height: 50px;
    font-size: 1rem;
  }
  
  .timeline-title {
    font-size: 1.25rem;
  }
  
  .timeline-description {
    font-size: 1rem;
  }
  
  .data-flow {
    gap: 0.75rem;
  }
  
  .flow-item {
    width: 150px;
    height: 6px;
  }
}

@media (max-width: 480px) {
  .container {
    padding: 0 1rem;
  }
  
  .page-title {
    font-size: 2rem;
  }
  
  .section-title {
    font-size: 1.875rem;
  }
  
  .timeline-item {
    grid-template-columns: 50px 1fr;
    gap: 1rem;
  }
  
  .timeline-number {
    width: 40px;
    height: 40px;
    font-size: 0.875rem;
  }
  
  .timeline-item:not(:last-child)::after {
    left: 24px;
  }
}
</style>
