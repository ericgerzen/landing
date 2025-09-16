<script>
  // No script needed for static content
</script>

<main class="main-content">
  <!-- Section 1: Logo & Header -->
  <section id="inicio" class="section section-hero">
    <div class="hero-content">
      <img src="/logo.png" alt="TechMarketBA Logo" class="hero-logo" />
      <div>
        <h1 class="hero-title center">TechMarketBA</h1>
        <p class="hero-subtitle center">Tu marketplace ecológico de confianza</p>
      </div>
    </div>
  </section>

  <!-- Section 2: Quienes Somos -->
  <section id="quienes-somos" class="section section-light">
    <h2 class="section-title center">¿Quiénes somos?</h2>
    <ul class="section-list">
      <li>• Primer ítem de ejemplo</li>
      <li>• Segundo ítem de ejemplo</li>
      <li>• Tercer ítem de ejemplo</li>
    </ul>
  </section>

  <!-- Section 3: Nuestros Objetivos -->
  <section id="nuestros-objetivos" class="section section-alt">
    <h2 class="section-title center">Nuestros objetivos</h2>
    <ul class="section-list">
      <li>• Primer objetivo de ejemplo</li>
      <li>• Segundo objetivo de ejemplo</li>
      <li>• Tercer objetivo de ejemplo</li>
    </ul>
  </section>

  <!-- Section 4: La Plataforma -->
  <section id="la-plataforma" class="section section-light">
    <h2 class="section-title center">La plataforma</h2>
    <div class="platform-images center">
      <img src="/gpu.png" alt="Plataforma 1" />
      <img src="/gpu.png" alt="Plataforma 2" />
      <img src="/gpu.png" alt="Plataforma 3" />
    </div>
    <ul class="section-list">
      <li>• Característica de ejemplo</li>
      <li>• Otra característica</li>
      <li>• Más detalles</li>
    </ul>
  </section>

  <!-- Section 5: Ingresá Ahora -->
  <section id="ingresar-ahora" class="section section-alt section-cta">
    <h2 class="section-title center">Ingresá ahora</h2>
    <p class="cta-subtitle center">¡Registrate y sé parte del cambio!</p>
    <button class="cta-button">Llevame ahí</button>
  </section>
</main>

<style>
.main-content {
  margin-top: 64px;
}
.section {
  width: 100vw;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 0;
  background: #fff;
  box-sizing: border-box;
}
.section-hero {
  background: linear-gradient(90deg, #6C63FF 0%, #48C9B0 100%);
  color: #fff;
}
.hero-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2vw;
}
.hero-logo {
  width: 80px;
  height: 80px;
  border-radius: 20px;
  background: #fff;
  box-shadow: 0 2px 8px #0001;
  object-fit: contain;
  margin-bottom: 1.5rem;
}
.hero-title {
  font-size: 2.8rem;
  font-family: 'Rubik', sans-serif;
  font-weight: 700;
  margin-bottom: 0.5rem;
}
.hero-subtitle {
  font-size: 1.2rem;
  font-family: 'Rubik', sans-serif;
  font-weight: 400;
  margin: 0;
}
.section-title {
  font-size: 2rem;
  font-family: 'Rubik', sans-serif;
  font-weight: 600;
  margin-bottom: 1.2rem;
  color: #3A3A3A;
}
.section-list {
  font-size: 1.1rem;
  font-family: 'Rubik', sans-serif;
  color: #555;
  margin: 0;
  padding: 0;
  list-style: none;
  text-align: center;
}
.platform-images {
  display: flex;
  gap: 2vw;
  margin-bottom: 1.2rem;
  justify-content: center;
}
.platform-images img {
  width: 60px;
  height: 60px;
  border-radius: 12px;
  background: #F0F0F0;
  object-fit: contain;
  box-shadow: 0 2px 8px #0001;
}
.section-cta {
  align-items: center;
  text-align: center;
}
.cta-subtitle {
  font-size: 1.1rem;
  color: #555;
  margin-bottom: 2rem;
}
.cta-button {
  background: linear-gradient(90deg, #6C63FF 0%, #48C9B0 100%);
  color: #fff;
  font-size: 1.3rem;
  font-family: 'Rubik', sans-serif;
  font-weight: 600;
  border: none;
  border-radius: 50px;
  padding: 1rem 2.5rem;
  cursor: pointer;
  box-shadow: 0 2px 8px #0002;
  transition: background 0.2s, transform 0.2s;
}
.cta-button:hover {
  background: linear-gradient(90deg, #48C9B0 0%, #6C63FF 100%);
  transform: scale(1.05);
}
.center {
  text-align: center;
  width: 100%;
}
.section-light {
  background: #F0F4FF;
  box-shadow: 0 2px 12px rgba(76, 110, 245, 0.04);
}
.section-alt {
  background: #F7F8FA;
  box-shadow: 0 2px 12px rgba(76, 110, 245, 0.04);
}
@media (max-width: 700px) {
  .main-content {
    margin-top: 48px;
  }
  .section-title {
    font-size: 1.3rem;
  }
  .hero-title {
    font-size: 2rem;
  }
  .platform-images img {
    width: 40px;
    height: 40px;
  }
  .cta-button {
    font-size: 1rem;
    padding: 0.7rem 1.5rem;
  }
}
</style>
