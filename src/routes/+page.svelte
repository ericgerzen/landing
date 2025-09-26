<script>
    function scrollToPropuesta() {
        const el = document.getElementById('la-propuesta');
        if (el) {
            el.scrollIntoView({ behavior: 'smooth' });
        }
    }
</script>

<main class="main-content">
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

    <section id="nosotros" class="section section-alt">
        <h2 class="section-title section-title-large center section-title-top">¿Por qué nosotros?</h2>
        <div class="section-icons-row nosotros-icons-column">
            <div class="icon-text icon-text-row">
                <img src="/Escudo.png" alt="Icono 1" class="icon-img" />
                <span class="icon-desc">Excelentes garantías</span>
            </div>
            <div class="icon-text icon-text-row">
                <img src="/Checklist.png" alt="Icono 2" class="icon-img" />
                <span class="icon-desc">Productos testeados</span>
            </div>
            <div class="icon-text icon-text-row">
                <img src="/Pricetag.png" alt="Icono 3" class="icon-img" />
                <span class="icon-desc">Mínimas tarifas</span>
            </div>
        </div>
        <img src="gamer.png" alt="Gamer" class="gamer-img" />
    </section>

    <section id="la-plataforma" class="section section-light platform-bg-section">
        <h2 class="section-title section-title-large center section-title-top">La plataforma</h2>
        <div class="platform-bg-row">
            <div class="platform-bg-col">
                <img src="/gpu.png" alt="Plataforma 1" class="icon-img platform-img-round platform-img-xlarge" />
            </div>
            <div class="platform-bg-col">
                <img src="/wcooling.png" alt="Plataforma 2" class="icon-img platform-img-round platform-img-xlarge" />
            </div>
            <div class="platform-bg-col">
                <img src="/pc.png" alt="Plataforma 3" class="icon-img platform-img-round platform-img-xlarge" />
            </div>
        </div>
    </section>

    <section id="ingresar-ahora" class="section section-alt section-cta">
        <h2 class="section-title section-title-large center">Ingresá ahora</h2>
        <div class="cta-icons-row">
            <div class="cta-side-icon-container left">
                <img src="/user.png" alt="Usuario" class="cta-side-icon" />
                <span class="icon-desc">Formá parte de nuestra base de</span>
                <span class="colorful-text">3</span>
                <span class="icon-desc">usuarios</span>
            </div>
            <img src="/LAPITOPI.png" alt="Lapitopi" class="cta-lapitopi" />
            <div class="cta-side-icon-container right">
                <img src="/Subtract.png" alt="Tiempo" class="cta-side-icon" />
                <span class="icon-desc">Creá una cuenta y empezá a comprar</span>
                <span class="colorful-text">YA MISMO</span>
            </div>
        </div>
        <p class="cta-subtitle center">¡Registrate y sé parte del cambio!</p>
        <button class="cta-button">Llevame ahí</button>
    </section>

    <script>
        const animatedSections = document.querySelectorAll('#nosotros, #la-plataforma, #ingresar-ahora');

        const observer = new IntersectionObserver((entries, observerInstance) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('is-visible');
                    observerInstance.unobserve(entry.target);
                }
            });
        }, {
            threshold: 0.4
        });

        animatedSections.forEach(section => {
            observer.observe(section);
        });
    </script>
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
        opacity: 0;
        animation: fadeInHero 1.2s ease-out forwards;
    }
    @keyframes fadeInHero {
        from {
            opacity: 0;
            transform: translateY(-40px);
        }
        to {
            opacity: 1;
            transform: translateY(0);
        }
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
    .nosotros-icons-column {
        flex-direction: column;
        align-items: flex-start;
        justify-content: flex-start;
        gap: 3rem;
        width: 100%;
        max-width: 600px;
        margin-left: 6vw;
    }
    .nosotros-icons-column .icon-text-row {
        flex-direction: row;
        align-items: center;
        text-align: left;
        gap: 2.5rem;
        min-width: 0;
    }
    .nosotros-icons-column .icon-img {
        margin-bottom: 0;
        background: #fff;
        border-radius: 50%;
        box-shadow: 0 2px 8px #0001;
        padding: 0.5rem;
    }
    .nosotros-icons-column .icon-desc {
        margin-top: 0;
        font-size: 1.3rem;
        text-align: left;
        color: #fff;
        text-shadow: 0 2px 8px #0002;
    }
    .section-icons-row.spaced-row {
        gap: 10vw;
    }
    .section-icons-row.more-space {
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

        transform: translate(-50%, -50%) scale(0);
        background: linear-gradient(to bottom, #6C63FF 0%, #48C9B0 100%);
        opacity: 0.5;
        z-index: 1;
        border-radius: 50%;
    }

    #la-plataforma:global(.is-visible) .platform-bg-col::before {
        animation: scaleUpCircle 0.8s ease-out forwards;
    }

    #la-plataforma:global(.is-visible) .platform-bg-col:nth-child(2)::before {
        animation-delay: 0.2s;
    }
    #la-plataforma:global(.is-visible) .platform-bg-col:nth-child(3)::before {
        animation-delay: 0.4s;
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
        opacity: 0;
    }
    .cta-side-icon-container.left {
        transform: translateX(-60px);
    }
    .cta-side-icon-container.right {
        transform: translateX(60px);
    }

    /* Keyframes for Section 5 */
    @keyframes fadeInLeft {
        from {
            opacity: 0;
            transform: translateX(-60px);
        }
        to {
            opacity: 1;
            transform: translateX(0);
        }
    }
    @keyframes fadeInRight {
        from {
            opacity: 0;
            transform: translateX(60px);
        }
        to {
            opacity: 1;
            transform: translateX(0);
        }
    }

    /* Rules to apply Section 5 animation when visible */
    #ingresar-ahora:global(.is-visible) .cta-side-icon-container.left {
        animation: fadeInLeft 1.2s ease-out forwards;
        animation-delay: 0.3s;
    }
    #ingresar-ahora:global(.is-visible) .cta-side-icon-container.right {
        animation: fadeInRight 1.2s ease-out forwards;
        animation-delay: 0.3s;
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
        .gamer-img {
            width: 300px;
            height: 300px;
        }
    }

    #nosotros {
        align-items: flex-start;
        padding-left: 6vw;
        background: linear-gradient(90deg, #6C63FF 0%, #48C9B0 100%) !important;
        color: #fff;
        position: relative; /* Crucial for positioning the gamer image */
        overflow: hidden; /* Prevents horizontal scrollbar */
    }

    #nosotros .nosotros-icons-column {
        align-items: flex-start;
        width: 100%;
        max-width: 800px;
        margin-left: 0;
        position: relative; /* Ensures text is on top of the image */
        z-index: 1;
    }

    /* === NEW STYLES FOR GAMER IMAGE === */
    .gamer-img {
        position: absolute;
        width: 400px;
        height: 100%;
        object-fit: cover;
        top: 50%;
        right: 0;
        transform: translate(10%, -50%);
        opacity: 0;
        z-index: 0;

        mask-image: linear-gradient(to right, transparent 0%, black 20%, black 100%);
        mask-mode: alpha; /* Use the alpha channel of the gradient for masking */
        mask-size: 100% 100%; /* Ensure the mask covers the entire image */
    }


    /* === NEW STYLES FOR SECTION 3 ANIMATION === */
    /* Keyframe for "Nosotros" text */
    @keyframes fadeInLeftText {
        from {
            opacity: 0;
            transform: translateX(-30px);
        }
        to {
            opacity: 1;
            transform: translateX(0);
        }
    }

    /* Initial hidden state for the text */
    #nosotros .nosotros-icons-column .icon-desc {
        opacity: 0;
    }

    /* Apply animation when section is visible */
    #nosotros:global(.is-visible) .icon-text-row .icon-desc {
        animation: fadeInLeftText 0.8s ease-out forwards;
    }

    /* Staggered delay for each item */
    #nosotros:global(.is-visible) .icon-text-row:nth-of-type(1) .icon-desc {
        animation-delay: 0.2s;
    }
    #nosotros:global(.is-visible) .icon-text-row:nth-of-type(2) .icon-desc {
        animation-delay: 0.4s;
    }
    #nosotros:global(.is-visible) .icon-text-row:nth-of-type(3) .icon-desc {
        animation-delay: 0.6s;
    }


    /* Keep original styles for "Nosotros" */
    #nosotros .nosotros-icons-column .icon-img {
        background: #fff;
        border-radius: 50%;
        box-shadow: 0 2px 8px #0001;
        padding: 0.5rem;
    }
    #nosotros .section-title {
        color: #fff;
        margin-top: 1rem;
    }
    #nosotros .nosotros-icons-column .icon-desc {
        color: #fff;
        text-shadow: 0 2px 8px #0002;
    }

    @keyframes fadeInFromRight {
        from {
            opacity: 0;
            transform: translate(40%, -50%);
        }
        to {
            opacity: 0.40; /* End at its final opacity */
            transform: translate(10%, -50%); /* End in its final position */
        }
    }

    #nosotros:global(.is-visible) .gamer-img {
        animation: fadeInFromRight 1.2s ease-out forwards;
        animation-delay: 0.8s;
    }

    @keyframes scaleUpCircle {
        from {
            transform: translate(-50%, -50%) scale(0);
        }
        to {
            transform: translate(-50%, -50%) scale(1);
        }
    }

</style>