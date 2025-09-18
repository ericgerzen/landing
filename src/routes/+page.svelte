<script>
    function scrollToPropuesta() {
        const el = document.getElementById('la-propuesta');
        if (el) {
            el.scrollIntoView({ behavior: 'smooth' });
        }
    }
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
        <div class="downwards-container">
            <span class="downwards-text downwards-text-more-transparent">¡Conocé quiénes somos!</span>
            <a href="#la-propuesta" class="downwards-link" on:click|preventDefault={scrollToPropuesta}>
                <img src="/downwards.png" alt="Flecha hacia abajo" class="downwards-img downwards-img-original" />
            </a>
        </div>
    </section>

    <!-- Section 2: La Propuesta -->
    <section id="la-propuesta" class="section section-light">
        <h2 class="section-title section-title-large center section-title-top">La propuesta</h2>
        <div class="section-icons-row spaced-row more-space">
            <div class="icon-text">
                <img src="/Tacho.png" alt="Icono 1" class="icon-img" />
                <span class="icon-desc">El E-waste forma gran parte<br>de la contaminacion mundial.<br>Miles de componentes aún<br>operativos se desechan a diario.</span>
            </div>
            <div class="icon-text">
                <img src="/Bombilla.png" alt="Icono 2" class="icon-img" />
                <span class="icon-desc">Decidimos traer un<br>modelo de mercado<br>extranjero al pais para<br>abarcar este problema.</span>
            </div>
            <div class="icon-text">
                <img src="/Reciclar.png" alt="Icono 3" class="icon-img" />
                <span class="icon-desc">Un marketplace basado en<br>electronicos testeados y<br>reutilizados, eco friendly,<br>con mejores precios.</span>
            </div>
        </div>
    </section>

    <!-- Section 3: Nosotros -->
    <section id="nosotros" class="section section-alt">
        <h2 class="section-title section-title-large center section-title-top">¿Por qué nosotros?</h2>
        <div class="section-icons-row spaced-row more-space">
            <div class="icon-text">
                <img src="/Escudo.png" alt="Icono 1" class="icon-img" />
                <span class="icon-desc">Ofrecemos excelentes<br>garantías</span>
            </div>
            <div class="icon-text">
                <img src="/Checklist.png" alt="Icono 2" class="icon-img" />
                <span class="icon-desc">Todos nuestros productos<br>son extensamente testeados</span>
            </div>
            <div class="icon-text">
                <img src="/Pricetag.png" alt="Icono 3" class="icon-img" />
                <span class="icon-desc">Cobramos mínimas tarifas<br>a los vendedores</span>
            </div>
        </div>
    </section>

    <!-- Section 4: La Plataforma -->
    <section id="la-plataforma" class="section section-light platform-bg-section">
        <h2 class="section-title section-title-large center section-title-top">La plataforma</h2>
        <div class="platform-bg-row">
            <div class="platform-bg-col" style="--bg-img: url('/gpu.png');">
                <img src="/gpu.png" alt="Plataforma 1" class="icon-img platform-img-round platform-img-xlarge" />
            </div>
            <div class="platform-bg-col" style="--bg-img: url('/wcooling.png');">
                <img src="/wcooling.png" alt="Plataforma 2" class="icon-img platform-img-round platform-img-xlarge" />
            </div>
            <div class="platform-bg-col" style="--bg-img: url('/pc.png');">
                <img src="/pc.png" alt="Plataforma 3" class="icon-img platform-img-round platform-img-xlarge" />
            </div>
        </div>
    </section>

    <!-- Section 5: Ingresá Ahora -->
    <section id="ingresar-ahora" class="section section-alt section-cta">
        <h2 class="section-title section-title-large center">Ingresá ahora</h2>
        <div class="cta-icons-row">
            <div class="cta-side-icon-container">
                <img src="/user.png" alt="Usuario" class="cta-side-icon" />
                <span class="icon-desc">Formá parte de nuestra base de</span>
                <span class="colorful-text">3</span>
                <span class="icon-desc">usuarios</span>
            </div>
            <img src="/LAPITOPI.png" alt="Lapitopi" class="cta-lapitopi" />
            <div class="cta-side-icon-container">
                <img src="/Subtract.png" alt="Tiempo" class="cta-side-icon" />
                <span class="icon-desc">Creá una cuenta y empezá a comprar</span>
                <span class="colorful-text">YA MISMO</span>
            </div>
        </div>
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
        position: relative;
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
    .more-space {
        gap: 14vw;
    }
    .icon-text {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 1.2rem;
        min-width: 160px;
    }
    .icon-desc {
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
    .platform-img-round {
        width: 120px;
        height: 120px;
        border-radius: 50%;
        background: #fff;
        box-shadow: 0 2px 8px #0001;
        object-fit: cover;
    }
    .platform-img-xlarge {
        width: 220px;
        height: 220px;
    }
    .cta-lapitopi {
        display: block;
        margin: 2rem auto 2rem auto;
        width: 320px;
        max-width: 80vw;
        height: auto;
    }
    .platform-bg-section {
        position: relative;
        overflow: hidden;
    }
    .platform-bg-row {
        display: flex;
        width: 100vw;
        height: 60vh;
        justify-content: center;
        align-items: center;
    }
    .platform-bg-col {
        flex: 1 1 0;
        display: flex;
        justify-content: center;
        align-items: center;
        position: relative;
        height: 100%;
        background: none;
    }
    .platform-bg-col::before {
        content: '';
        position: absolute;
        top: 50%;
        left: 50%;
        width: 70%;
        height: 70%;
        transform: translate(-50%, -50%);
        background-image: var(--bg-img);
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center;
        opacity: 0.13;
        z-index: 1;
        border-radius: 50%;
    }
    .platform-bg-col img {
        position: relative;
        z-index: 2;
    }
    .downwards-container {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: flex-end;
        position: absolute;
        left: 0;
        right: 0;
        bottom: 14vh;
        z-index: 10;
    }
    .downwards-text {
        color: rgba(255,255,255,0.85);
        font-size: 1.3rem;
        font-family: 'Rubik', sans-serif;
        font-weight: 500;
        margin-bottom: 0.7rem;
        text-shadow: 0 2px 8px #0002;
    }
    .downwards-text-more-transparent {
        color: rgba(255,255,255,0.55);
    }
    .downwards-img {
        width: 48px;
        height: 48px;
        opacity: 0.85;
    }
    .downwards-img-original {
        width: 64px;
        height: 16px;
        opacity: 0.85;
    }
    .downwards-link {
        display: block;
        cursor: pointer;
        transition: transform 0.2s;
    }
    .downwards-link:hover {
        transform: translateY(6px) scale(1.08);
    }
    .cta-side-icon-container {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 0;
        max-width: 220px;
    }
    .cta-icons-row {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        gap: 15vw;
        margin-bottom: 2rem;
    }
    .cta-side-icon {
        width: 90px;
        height: 90px;
        margin-bottom: 1rem;
    }
    .colorful-text {
        background: linear-gradient(90deg, #6C63FF 0%, #48C9B0 100%);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
        font-weight: bold;
        font-size: 2.5rem;
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
        .platform-img-round {
            width: 70px;
            height: 70px;
        }
        .platform-img-xlarge {
            width: 120px;
            height: 120px;
        }
        .cta-lapitopi {
            width: 180px;
            margin: 1.2rem auto 1.2rem auto;
        }
        .downwards-container {
            bottom: 10vh;
        }
        .downwards-text {
            font-size: 1rem;
            margin-bottom: 0.4rem;
        }
        .downwards-img {
            width: 32px;
            height: 32px;
        }
        .cta-side-icon {
            width: 50px;
            height: 50px;
        }
    }
    @media (max-width: 900px) {
        .platform-bg-row {
            flex-direction: column;
            height: auto;
            min-height: 60vw;
        }
        .platform-bg-col {
            width: 100vw;
            min-height: 33vw;
            height: 33vw;
        }
    }
</style>
