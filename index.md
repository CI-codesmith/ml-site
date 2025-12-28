---
layout: default
title: Machine Learning Course - MSBTE K-SCHEME 316316
permalink: /index.html
---

<!-- Hero Section -->
<div class="hero">
  <h1>Machine Learning Course</h1>
  <p class="subtitle">MSBTE K-SCHEME 316316 - Semester 6</p>
  <div>
    <span class="badge">Complete & Production Ready</span>
    <span class="badge">15 Practicals</span>
    <span class="badge">5 Units</span>
  </div>
  <p class="description">Comprehensive learning platform with 200+ theory components, hands-on laboratories, real-world applications, and production deployment guidance.</p>
  
  <div class="cta-group">
    <a href="#quick-start" class="btn btn-primary">
      <i class="fas fa-play"></i> Get Started Now
    </a>
    <a href="{{ '/what-is-ml.md' | relative_url }}" class="btn btn-secondary">
      <i class="fas fa-info-circle"></i> What is ML?
    </a>
  </div>
</div>

<!-- Quick Start Section -->
<div class="section" id="quick-start">
  <h2 class="section-title">🚀 Quick Start</h2>
  
  <div class="cards-grid">
    <div class="card">
      <div class="card-icon"><i class="fas fa-tools"></i></div>
      <h3>Setup Environment</h3>
      <p>Install Python, libraries, and development tools. Takes 15 minutes.</p>
      <a href="{{ '/resources/installation-guide.md' | relative_url }}" class="card-link">
        Setup Guide <i class="fas fa-arrow-right"></i>
      </a>
    </div>
    
    <div class="card">
      <div class="card-icon"><i class="fas fa-graduation-cap"></i></div>
      <h3>Learn Fundamentals</h3>
      <p>Start with Unit 1: Introduction to Machine Learning basics.</p>
      <a href="{{ '/units/unit-1/' | relative_url }}" class="card-link">
        Unit 1 <i class="fas fa-arrow-right"></i>
      </a>
    </div>
    
    <div class="card">
      <div class="card-icon"><i class="fas fa-code"></i></div>
      <h3>Build Your First Project</h3>
      <p>Complete Practical 1 and get hands-on with ML tools.</p>
      <a href="{{ '/practicals/practical-1/' | relative_url }}" class="card-link">
        Practical 1 <i class="fas fa-arrow-right"></i>
      </a>
    </div>
  </div>
</div>

<!-- Courses Section -->
<div class="section">
  <h2 class="section-title">📚 Course Units</h2>
  <p class="section-subtitle">5 comprehensive units covering ML fundamentals to advanced topics</p>
  
  <div class="grid-2">
    <a href="{{ '/units/unit-1/' | relative_url }}" style="text-decoration: none;">
      <div class="unit-card unit-1">
        <h3><i class="fas fa-cube"></i> Unit 1: Introduction</h3>
        <p>Fundamentals • Types • Python Basics • Environment Setup</p>
      </div>
    </a>
    
    <a href="{{ '/units/unit-2/' | relative_url }}" style="text-decoration: none;">
      <div class="unit-card unit-2">
        <h3><i class="fas fa-cube"></i> Unit 2: Supervised</h3>
        <p>Regression • Classification • Evaluation • Metrics</p>
      </div>
    </a>
    
    <a href="{{ '/units/unit-3/' | relative_url }}" style="text-decoration: none;">
      <div class="unit-card unit-3">
        <h3><i class="fas fa-cube"></i> Unit 3: Unsupervised</h3>
        <p>Clustering • Dimensionality • Anomaly Detection</p>
      </div>
    </a>
    
    <a href="{{ '/units/unit-4/' | relative_url }}" style="text-decoration: none;">
      <div class="unit-card unit-4">
        <h3><i class="fas fa-cube"></i> Unit 4: Advanced</h3>
        <p>Neural Networks • Deep Learning • Ensembles</p>
      </div>
    </a>
    
    <a href="{{ '/units/unit-5/' | relative_url }}" style="text-decoration: none;">
      <div class="unit-card unit-5">
        <h3><i class="fas fa-cube"></i> Unit 5: Ethics & Production</h3>
        <p>ML Ethics • Deployment • Real-world Cases</p>
      </div>
    </a>
    
    <a href="{{ '/units/' | relative_url }}" style="text-decoration: none;">
      <div class="unit-card" style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); display: flex; align-items: center; justify-content: center; min-height: 150px;">
        <h3 style="text-align: center; margin: 0;"><i class="fas fa-book"></i> View All Units</h3>
      </div>
    </a>
  </div>
</div>

<!-- Practicals Section -->
<div class="section">
  <h2 class="section-title">🧪 15 Practical Labs</h2>
  <p class="section-subtitle">Hands-on laboratory exercises with code examples and deliverables</p>
  
  <div class="grid-3">
    {% for i in (1..15) %}
      <a href="{{ '/practicals/practical-' | append: i | append: '/' | relative_url }}" style="text-decoration: none;">
        <div class="practical-card">
          <h3><i class="fas fa-flask"></i> Practical {{ i }}</h3>
          <p>
            {% if i <= 2 %}
              Environment & Data
            {% elsif i <= 5 %}
              Regression & Classification
            {% elsif i <= 8 %}
              Clustering & Analysis
            {% elsif i <= 11 %}
              Neural Networks
            {% else %}
              Real-world Applications
            {% endif %}
          </p>
        </div>
      </a>
    {% endfor %}
  </div>
  
  <div style="text-align: center; margin-top: var(--space-xl);">
    <a href="{{ '/practicals/' | relative_url }}" class="btn btn-primary">
      View All Practicals with Details
    </a>
  </div>
</div>

<!-- Key Resources Section -->
<div class="section">
  <h2 class="section-title">📖 Key Resources</h2>
  
  <div class="grid-3">
    <div class="card">
      <div class="card-icon"><i class="fas fa-book"></i></div>
      <h3>Complete Theory Notes</h3>
      <p>All 200+ concepts from 5 units in one comprehensive document.</p>
      <a href="{{ '/THEORY_NOTES.md' | relative_url }}" class="card-link">
        Read Notes <i class="fas fa-arrow-right"></i>
      </a>
    </div>
    
    <div class="card">
      <div class="card-icon"><i class="fas fa-list-check"></i></div>
      <h3>Course Syllabus</h3>
      <p>MSBTE K-SCHEME 316316 complete curriculum with learning outcomes.</p>
      <a href="{{ '/SYLLABUS.md' | relative_url }}" class="card-link">
        View Syllabus <i class="fas fa-arrow-right"></i>
      </a>
    </div>
    
    <div class="card">
      <div class="card-icon"><i class="fas fa-rocket"></i></div>
      <h3>Deployment Guide</h3>
      <p>Production deployment strategies and best practices.</p>
      <a href="{{ '/DEPLOYMENT.md' | relative_url }}" class="card-link">
        Deploy Now <i class="fas fa-arrow-right"></i>
      </a>
    </div>
    
    <div class="card">
      <div class="card-icon"><i class="fas fa-wrench"></i></div>
      <h3>Installation Guide</h3>
      <p>Complete setup instructions with troubleshooting.</p>
      <a href="{{ '/resources/installation-guide.md' | relative_url }}" class="card-link">
        Setup Guide <i class="fas fa-arrow-right"></i>
      </a>
    </div>
    
    <div class="card">
      <div class="card-icon"><i class="fas fa-timer"></i></div>
      <h3>Quick Start</h3>
      <p>Get your first ML project running in 30 minutes.</p>
      <a href="{{ '/resources/quick-start.md' | relative_url }}" class="card-link">
        Start Project <i class="fas fa-arrow-right"></i>
      </a>
    </div>
    
    <div class="card">
      <div class="card-icon"><i class="fas fa-tasks"></i></div>
      <h3>Assessments</h3>
      <p>Weekly tests, class tests, and preliminary exam papers.</p>
      <a href="{{ '/assessments/' | relative_url }}" class="card-link">
        View Tests <i class="fas fa-arrow-right"></i>
      </a>
    </div>
  </div>
</div>

<!-- Statistics Section -->
<div class="section">
  <h2 class="section-title">📊 Course Statistics</h2>
  
  <div class="grid-3">
    <div class="card" style="text-align: center;">
      <div style="font-size: 2.5rem; color: var(--primary); margin-bottom: var(--space-md);">
        <i class="fas fa-book"></i>
      </div>
      <h3 style="margin: 0;">200+</h3>
      <p style="margin: 0; color: #6b7280;">ML Concepts & Topics</p>
    </div>
    
    <div class="card" style="text-align: center;">
      <div style="font-size: 2.5rem; color: var(--secondary); margin-bottom: var(--space-md);">
        <i class="fas fa-flask"></i>
      </div>
      <h3 style="margin: 0;">15</h3>
      <p style="margin: 0; color: #6b7280;">Hands-on Practicals</p>
    </div>
    
    <div class="card" style="text-align: center;">
      <div style="font-size: 2.5rem; color: var(--success); margin-bottom: var(--space-md);">
        <i class="fas fa-code"></i>
      </div>
      <h3 style="margin: 0;">50+</h3>
      <p style="margin: 0; color: #6b7280;">Code Examples</p>
    </div>
    
    <div class="card" style="text-align: center;">
      <div style="font-size: 2.5rem; color: var(--warning); margin-bottom: var(--space-md);">
        <i class="fas fa-target"></i>
      </div>
      <h3 style="margin: 0;">25+</h3>
      <p style="margin: 0; color: #6b7280;">Learning Outcomes</p>
    </div>
    
    <div class="card" style="text-align: center;">
      <div style="font-size: 2.5rem; color: var(--danger); margin-bottom: var(--space-md);">
        <i class="fas fa-clipboard-check"></i>
      </div>
      <h3 style="margin: 0;">9</h3>
      <p style="margin: 0; color: #6b7280;">Assessment Papers</p>
    </div>
    
    <div class="card" style="text-align: center;">
      <div style="font-size: 2.5rem; color: var(--primary); margin-bottom: var(--space-md);">
        <i class="fas fa-project-diagram"></i>
      </div>
      <h3 style="margin: 0;">Complete</h3>
      <p style="margin: 0; color: #6b7280;">Production Ready</p>
    </div>
  </div>
</div>

<!-- Integration Section -->
<div class="section">
  <h2 class="section-title">🔗 Platform Integration</h2>
  <p class="section-subtitle">Everything you need in one place</p>
  
  <div class="cards-grid">
    <div class="card">
      <div class="card-icon"><i class="fas fa-chalkboard-user"></i></div>
      <h3>Interactive Overview</h3>
      <p>Explore ML concepts through our Gamma interactive site with visual explanations.</p>
      <a href="{{ '/what-is-ml.md' | relative_url }}" class="card-link">
        View Overview <i class="fas fa-arrow-right"></i>
      </a>
    </div>
    
    <div class="card">
      <div class="card-icon"><i class="fas fa-network-wired"></i></div>
      <h3>GitHub Integration</h3>
      <p>Complete source code, version control, and continuous deployment via GitHub.</p>
      <a href="https://github.com/CI-codesmith/ml-site" target="_blank" class="card-link">
        View Repository <i class="fas fa-arrow-right"></i>
      </a>
    </div>
    
    <div class="card">
      <div class="card-icon"><i class="fas fa-globe"></i></div>
      <h3>Custom Domain</h3>
      <p>Add your own domain for a professional presence. Complete setup guide included.</p>
      <a href="{{ '/CUSTOM_DOMAIN.md' | relative_url }}" class="card-link">
        Setup Domain <i class="fas fa-arrow-right"></i>
      </a>
    </div>
  </div>
</div>

<!-- Course Progress Tracker -->
<div class="section">
  <h2 class="section-title">🎯 Learning Path</h2>
  
  <div style="background-color: var(--light); padding: var(--space-xl); border-radius: var(--radius-lg); border-left: 4px solid var(--primary);">
    <h3 style="margin-top: 0;">Recommended Study Path</h3>
    <ol style="line-height: 2;">
      <li><strong>Week 1:</strong> Setup environment, learn Unit 1 fundamentals, complete Practicals 1-2</li>
      <li><strong>Week 2-3:</strong> Study Unit 2 (Supervised Learning), complete Practicals 3-5</li>
      <li><strong>Week 4:</strong> Study Unit 3 (Unsupervised), complete Practicals 6-8</li>
      <li><strong>Week 5-6:</strong> Study Unit 4 (Advanced), complete Practicals 9-10, 12-13</li>
      <li><strong>Week 7:</strong> Study Unit 5 (Ethics & Production), complete Practicals 11, 14-15</li>
      <li><strong>Week 8:</strong> Review, revise, and prepare for assessments</li>
    </ol>
  </div>
</div>

<!-- Call to Action -->
<div class="section" style="text-align: center; padding: var(--space-2xl); background: linear-gradient(135deg, rgba(0, 102, 204, 0.05) 0%, rgba(0, 102, 204, 0.1) 100%); border-radius: var(--radius-xl);">
  <h2>Ready to Master Machine Learning?</h2>
  <p style="font-size: 1.125rem; color: #6b7280; margin-bottom: var(--space-xl);">
    Start your journey with 15 hands-on practicals and comprehensive theory documentation.
  </p>
  <a href="{{ '/resources/installation-guide.md' | relative_url }}" class="btn btn-primary">
    <i class="fas fa-play-circle"></i> Get Started Now
  </a>
</div>
