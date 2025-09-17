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

  <!-- Section 2: La Propuesta -->
  <section id="la-propuesta" class="section section-light">
    <h2 class="section-title section-title-large center section-title-top">La propuesta</h2>
    <div class="section-icons-row spaced-row">
      <div class="icon-text">
        <img src="/Tacho.png" alt="Icono 1" class="icon-img" />
        <span>El E-waste forma gran parte<br>de la contaminacion mundial.<br>Miles de componentes aún<br>operativos se desechan a diario.</span>
      </div>
      <div class="icon-text">
        <img src="/Bombilla.png" alt="Icono 2" class="icon-img" />
        <span>Decidimos traer un<br>modelo de mercado<br>extranjero al pais para<br>abarcar este problema.</span>
      </div>
      <div class="icon-text">
        <img src="/Reciclar.png" alt="Icono 3" class="icon-img" />
        <span>Un marketplace basado en<br>electronicos testeados y<br>reutilizados, eco friendly,<br>con mejores precios.</span>
      </div>
    </div>
  </section>

  <!-- Section 3: Nosotros -->
  <section id="nosotros" class="section section-alt">
    <h2 class="section-title section-title-large center section-title-top">¿Por qué nosotros?</h2>
    <div class="section-icons-row spaced-row">
      <div class="icon-text">
        <img src="/Escudo.png" alt="Icono 1" class="icon-img" />
        <span>Ofrecemos excelentes<br>garantías</span>
      </div>
      <div class="icon-text">
        <img src="/Checklist.png" alt="Icono 2" class="icon-img" />
        <span>Todos nuestros productos<br>son extensamente testeados</span>
      </div>
      <div class="icon-text">
        <img src="/Pricetag.png" alt="Icono 3" class="icon-img" />
        <span>Cobramos mínimas tarifas<br>a los vendedores</span>
      </div>
    </div>
  </section>

  <!-- Section 4: La Plataforma -->
  <section id="la-plataforma" class="section section-light">
    <h2 class="section-title section-title-large center section-title-top">La plataforma</h2>
    <div class="section-icons-row spaced-row">
      <div class="icon-text">
        <img src="/gpu.png" alt="Plataforma 1" class="icon-img" />
        <span>Característica<br>de ejemplo</span>
      </div>
      <div class="icon-text">
        <img src="/gpu.png" alt="Plataforma 2" class="icon-img" />
        <span>OCaracterística<br>de ejemplo</span>
      </div>
      <div class="icon-text">
        <img src="/gpu.png" alt="Plataforma 3" class="icon-img" />
        <span>Característica<br>de ejemplo</span>
      </div>
    </div>
  </section>

  <!-- Section 5: Ingresá Ahora -->
  <section id="ingresar-ahora" class="section section-alt section-cta">
    <h2 class="section-title section-title-large center">Ingresá ahora</h2>
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
  width: 180px;
  height: 180px;
  border-radius: 50%;
  background: #fff;
  box-shadow: 0 2px 8px #0001;
  object-fit: contain;
  margin-bottom: 0;
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
.section-title-large {
  font-size: 3rem;
  font-weight: 800;
}
.section-title-top {
  margin-top: 12vh;
  margin-bottom: 3vh;
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
.section-icons-row {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: flex-start;
  gap: 5vw;
  margin-top: 2vh;
}
.spaced-row {
  gap: 10vw;
}
.icon-text {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1.2rem;
  min-width: 160px;
}
.icon-text span {
  font-size: 1.2rem;
  font-family: 'Rubik', sans-serif;
  color: #444;
  font-weight: 500;
  text-align: center;
  margin-top: 0.2rem;
}
.icon-img {
  width: 96px;
  height: 96px;
  object-fit: contain;
  margin-bottom: 0.5rem;
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
  .hero-logo {
    width: 80px;
    height: 80px;
  }
  .platform-images img {
    width: 40px;
    height: 40px;
  }
  .cta-button {
    font-size: 1rem;
    padding: 0.7rem 1.5rem;
  }
  .section-title-large {
    font-size: 2rem;
  }
  .section-icons-row {
    gap: 2vw;
  }
  .icon-text {
    min-width: 100px;
    gap: 0.7rem;
  }
  .icon-text span {
    font-size: 1rem;
  }
  .icon-img {
    width: 60px;
    height: 60px;
  }
}
</style>
