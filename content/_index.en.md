---
toc: false
---

<style>
  .full-width {
    position: relative;
    left: 50%;
    right: 50%;
    margin-top: -1rem;
    margin-bottom: -2rem;
    margin-left: -50vw;
    margin-right: -50vw;
    width: 100vw;
  }

  .full-width > * {
    width: 100%;
  }
</style>

<style>
  .hero-container {
    position: relative;
    width: 100vw;
    min-height: 100vh;
    overflow: hidden;
    background: linear-gradient(180deg, #0a0e27 0%, #1a1f3a 50%, #050812 100%);
  }

  /* Background SVG Pattern */
  .hero-bg {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    opacity: 0.3;
  }

  /* Elementos flotantes animados */
  .floating-element {
    position: absolute;
    border-radius: 50%;
    filter: blur(60px);
    animation: float 6s ease-in-out infinite;
  }

  .floating-1 {
    width: 400px;
    height: 400px;
    background: radial-gradient(circle, rgba(0, 217, 255, 0.3) 0%, transparent 70%);
    top: 10%;
    left: 5%;
    animation-delay: 0s;
  }

  .floating-2 {
    width: 500px;
    height: 500px;
    background: radial-gradient(circle, rgba(255, 0, 110, 0.25) 0%, transparent 70%);
    bottom: 15%;
    right: 10%;
    animation-delay: 2s;
  }

  .floating-3 {
    width: 300px;
    height: 300px;
    background: radial-gradient(circle, rgba(107, 0, 255, 0.2) 0%, transparent 70%);
    top: 50%;
    right: 20%;
    animation-delay: 4s;
  }

  @keyframes float {
    0%, 100% { transform: translateY(0px) translateX(0px); }
    33% { transform: translateY(-30px) translateX(20px); }
    66% { transform: translateY(20px) translateX(-15px); }
  }

  /* Grid pattern sutil */
  .grid-overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-image: 
      linear-gradient(rgba(26, 77, 109, 0.1) 1px, transparent 1px),
      linear-gradient(90deg, rgba(26, 77, 109, 0.1) 1px, transparent 1px);
    background-size: 50px 50px;
    opacity: 0.4;
  }

  /* Contenido principal */
  .hero-content {
    position: relative;
    z-index: 10;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
    padding: 2rem;
    text-align: center;
  }

  .hero-title {
    font-size: clamp(3rem, 8vw, 7rem);
    font-weight: 900;
    background: linear-gradient(135deg, #00d9ff 0%, #00fff2 50%, #0066ff 100%);
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
    margin-bottom: 1rem;
    letter-spacing: -0.02em;
    animation: slideDown 1s ease-out;
    text-shadow: 0 0 80px rgba(0, 217, 255, 0.5);
  }

  .hero-subtitle {
    font-size: clamp(1.2rem, 3vw, 2rem);
    color: rgba(255, 255, 255, 0.8);
    margin-bottom: 3rem;
    font-weight: 300;
    letter-spacing: 0.05em;
    animation: slideDown 1s ease-out 0.2s backwards;
  }

  @keyframes slideDown {
    from {
      opacity: 0;
      transform: translateY(-50px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  /* Tarjetas de navegación */
  .nav-cards {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 2rem;
    max-width: 1200px;
    width: 100%;
    margin-top: 3rem;
    animation: fadeIn 1s ease-out 0.4s backwards;
  }

  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .nav-card {
    position: relative;
    background: rgba(255, 255, 255, 0.03);
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 255, 255, 0.1);
    border-radius: 20px;
    padding: 2.5rem 2rem;
    cursor: pointer;
    transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
    overflow: hidden;
    text-decoration: none;
    color: white;
    display: block;
  }

  .nav-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(135deg, rgba(0, 217, 255, 0.1) 0%, transparent 100%);
    opacity: 0;
    transition: opacity 0.4s;
  }

  .nav-card:hover {
    transform: translateY(-10px);
    border-color: rgba(0, 217, 255, 0.4);
    box-shadow: 0 20px 40px rgba(0, 217, 255, 0.2);
  }

  .nav-card:hover::before {
    opacity: 1;
  }

  .card-icon {
    font-size: 3rem;
    margin-bottom: 1rem;
    display: block;
    transition: transform 0.4s;
  }

  .nav-card:hover .card-icon {
    transform: scale(1.2) rotate(5deg);
  }

  .card-title {
    font-size: 1.5rem;
    font-weight: 700;
    margin-bottom: 0.5rem;
    color: #fff;
  }

  .card-description {
    font-size: 0.95rem;
    color: rgba(255, 255, 255, 0.6);
    line-height: 1.5;
  }

  /* Líneas de energía animadas */
  .energy-lines {
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    pointer-events: none;
  }

  .energy-line {
    position: absolute;
    height: 2px;
    background: linear-gradient(90deg, transparent, #00d9ff, transparent);
    animation: slideLine 3s ease-in-out infinite;
    opacity: 0.3;
  }

  .energy-line:nth-child(1) {
    top: 20%;
    width: 40%;
    left: -40%;
    animation-delay: 0s;
  }

  .energy-line:nth-child(2) {
    top: 45%;
    width: 50%;
    right: -50%;
    animation-delay: 1.5s;
    background: linear-gradient(90deg, transparent, #ff006e, transparent);
  }

  .energy-line:nth-child(3) {
    top: 70%;
    width: 35%;
    left: -35%;
    animation-delay: 3s;
    background: linear-gradient(90deg, transparent, #00fff2, transparent);
  }

  @keyframes slideLine {
    0% { transform: translateX(0); }
    100% { transform: translateX(calc(100vw + 100%)); }
  }

  /* Partículas flotantes */
  .particle {
    position: absolute;
    width: 4px;
    height: 4px;
    background: #00d9ff;
    border-radius: 50%;
    box-shadow: 0 0 10px #00d9ff;
    animation: particleFloat 4s ease-in-out infinite;
  }

  .particle:nth-child(1) { top: 25%; left: 15%; animation-delay: 0s; }
  .particle:nth-child(2) { top: 55%; left: 75%; animation-delay: 1s; background: #ff4d00; box-shadow: 0 0 10px #ff4d00; }
  .particle:nth-child(3) { top: 35%; left: 85%; animation-delay: 2s; background: #00fff2; box-shadow: 0 0 10px #00fff2; }
  .particle:nth-child(4) { top: 75%; left: 25%; animation-delay: 1.5s; background: #6b00ff; box-shadow: 0 0 10px #6b00ff; }

  @keyframes particleFloat {
    0%, 100% { transform: translateY(0) scale(1); opacity: 0.6; }
    50% { transform: translateY(-30px) scale(1.5); opacity: 1; }
  }

  /* CTA Button */
  .cta-button {
    display: inline-block;
    margin-top: 2rem;
    padding: 1.2rem 3rem;
    background: linear-gradient(135deg, #00d9ff, #0066ff);
    color: white;
    font-size: 1.1rem;
    font-weight: 700;
    text-decoration: none;
    border-radius: 50px;
    transition: all 0.3s;
    box-shadow: 0 10px 30px rgba(0, 217, 255, 0.3);
    animation: slideDown 1s ease-out 0.6s backwards;
    position: relative;
    overflow: hidden;
  }

  .cta-button::before {
    content: '';
    position: absolute;
    top: 50%;
    left: 50%;
    width: 0;
    height: 0;
    background: rgba(255, 255, 255, 0.2);
    border-radius: 50%;
    transform: translate(-50%, -50%);
    transition: width 0.6s, height 0.6s;
  }

  .cta-button:hover::before {
    width: 300px;
    height: 300px;
  }

  .cta-button:hover {
    transform: translateY(-3px);
    box-shadow: 0 15px 40px rgba(0, 217, 255, 0.5);
  }

  /* Responsive */
  @media (max-width: 768px) {
    .nav-cards {
      grid-template-columns: 1fr;
      gap: 1.5rem;
    }

    .hero-title {
      font-size: 3rem;
    }

    .nav-card {
      padding: 2rem 1.5rem;
    }
  }
</style>

<div class="full-width">
  <div class="hero-container">
    <!-- Elementos de fondo animados -->
    <div class="floating-element floating-1"></div>
    <div class="floating-element floating-2"></div>
    <div class="floating-element floating-3"></div>
    <div class="grid-overlay"></div>
    <!-- Líneas de energía -->
    <div class="energy-lines">
      <div class="energy-line"></div>
      <div class="energy-line"></div>
      <div class="energy-line"></div>
    </div>
    <!-- Partículas -->
    <div class="particle"></div>
    <div class="particle"></div>
    <div class="particle"></div>
    <div class="particle"></div>
    <!-- Contenido principal -->
    <div class="hero-content">
      <div style="display:flex;flex-direction:column;align-items:center">
        <svg xmlns="http://www.w3.org/2000/svg" xml:space="preserve" width="120" height="120" viewBox="0 0 135.467 135.467"><path d="M18.982-3.17v15.904l2.28 3.54-2.341 16.215-.022 10.046 3.384 9.041v6.505l2.762 6.059.18 16.124 2.85 8.017-.355 11.403 2.494 6.06 4.453 4.096-4.166-1.957-3.057-2.899-.348 11.092 8.003 20.626 61.348.03 3.568-10.902.49-19.553-4.721-3.386-2.585-4.454 4.542 3.92 3.21 1.426 3.651.269 4.097-5.703 1.68-4.515 3.4 1.134.724-8.285 2.35-1.743 1.913.936 3.647-8.263-.973-8.931-4.454-7.84-7.84-3.566-8.016-.89 3.74-.71 7.127.71 1.96-19.776 6.949-5.346V-3.14zm16.624 16.655 24.819 9.323 21.417 5.04 23.058 1.888-3.78 3.024 1.511 5.416-4.284 4.032-5.293 13.733-6.802 4.537-5.416 14.74-8.065 5.416-6.93-6.424-11.213-2.895-4.284-15.626-8.44-12.473 1.134-13.858z" style="fill:white"/></svg>
        <div style="font-family: ui-serif, Georgia, Cambria, 'Times New Roman', Times, serif;">
          <h1 style="font-size:5.5rem;color:white">ATLAS</h1>
          <hr style="border-color:white;margin:-0.3rem 0 0.4rem 0">
          <div style="display:flex;justify-content:space-between;color:white">
            <span>C</span>
            <span>O</span>
            <span>N</span>
            <span>S</span>
            <span>U</span>
            <span>L</span>
            <span>T</span>
            <span>I</span>
            <span>N</span>
            <span>G</span>
          </div>
        </div>
      </div>
      <a href="contact" class="cta-button">Start Now →</a>
      <!-- Tarjetas de navegación -->
      <div class="nav-cards">
        <a href="services" class="nav-card">
          <span class="card-icon">📊</span>
          <h3 class="card-title">Sports Analytics</h3>
          <p class="card-description">Advanced metrics, KPIs and data analysis to optimize performance</p>
        </a>
        <a href="services" class="nav-card">
          <span class="card-icon">💻</span>
          <h3 class="card-title">Digital Transformation</h3>
          <p class="card-description">Technology solutions and digitalization for sports organizations</p>
        </a>
        <a href="services" class="nav-card">
          <span class="card-icon">🎯</span>
          <h3 class="card-title">Strategic Consulting</h3>
          <p class="card-description">Planning, development and comprehensive management of sports projects</p>
        </a>
        <a href="blog" class="nav-card">
          <span class="card-icon">📰</span>
          <h3 class="card-title">Publications</h3>
          <p class="card-description">Latest news, insights and trends in sports</p>
        </a>
        <a href="about" class="nav-card">
          <span class="card-icon">🏆</span>
          <h3 class="card-title">About Us</h3>
          <p class="card-description">Meet our team, experience and track record in the sports sector</p>
        </a>
        <a href="contact" class="nav-card">
          <span class="card-icon">💬</span>
          <h3 class="card-title">Contact</h3>
          <p class="card-description">Schedule a consultation and discover how we can help you</p>
        </a>
      </div>
    </div>
  </div>
</div>

