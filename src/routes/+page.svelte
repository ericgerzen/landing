<script>
    import { onMount } from 'svelte';

    onMount(() => {
        document.title = "PC Hardware Deals";
    });

    let totalSquares = 6;
    let currentIndex = 0;

    $: visibleSquares = Array(totalSquares)
        .fill(0)
        .map((_, i) => i)
        .slice(currentIndex, currentIndex + 2);

    let animationClass = '';
    let lastDir = 0;

    /**
     * Moves the carousel in the given direction.
     * @param {number} dir - Direction to move: -1 for left, 1 for right.
     */
    function move(dir) {
        if (dir === -1 && currentIndex > 0) {
            currentIndex--;
            lastDir = -1;
            animateSquares();
        } else if (dir === 1 && currentIndex < totalSquares - 2) {
            currentIndex++;
            lastDir = 1;
            animateSquares();
        }
    }

    function animateSquares() {
        animationClass = lastDir === 1 ? 'slide-right' : 'slide-left';
        setTimeout(() => {
            animationClass = '';
        }, 350);
    }
</script>

<section class="tall-section">
    <div class="left-content">
        <h1 class="text-3xl">Encontrá las mejores ofertas para componentes de computadora.</h1>
    </div>
    <div class="image-grid">
        <img src="/pc.png" alt="Pc">
        <img src="/keyboard.png" alt="Keyboard">
        <img src="/wcooling.png" alt="Water Cooling">
        <img src="/gpu.png" alt="GPU">
    </div>
</section>

<section class="darkness">
    <div class="scrolling-text">
        <span>
            TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT
            TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT
            TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT
            TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT
            TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT
        </span>
        <span>
            TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT
            TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT
            TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT
            TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT
            TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT
        </span>
    </div>
</section>

<section class="tall-section-2">
    <div class="arrow-container" on:click={() => move(-1)}>
        <img src="/arrow.png" alt="Left Arrow" class="arrow left-arrow" style="transform: scaleX(-1);" />
    </div>
    <div class="squares-indicator-wrapper">
        <div class="squares-container {animationClass}">
            {#each visibleSquares as square}
                <div class="round-square">{square + 1}</div>
            {/each}
        </div>
        <div class="indicators">
            {#each Array(totalSquares - 1) as _, i}
                <div class="indicator {i === currentIndex ? 'active' : ''}"></div>
            {/each}
        </div>
    </div>
    <div class="arrow-container" on:click={() => move(1)}>
        <img src="/arrow.png" alt="Right Arrow" class="arrow right-arrow" />
    </div>
</section>


<style>
    .tall-section {
        background: #5A3C78;
        min-height: 40.2rem;
        width: 100%;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        padding: 0 4vw;
        box-sizing: border-box;
    }
    .left-content {
        flex: 1 1 40%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: flex-start;
    }
    .tall-section h1 {
        font-family: 'Crete Round', serif;
        font-size: 4rem;
        color: white;
        margin: 0;
    }
    .image-grid {
        flex: 1 1 60%;
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-template-rows: 1fr 1fr;
        column-gap: 2vw;
        row-gap: 0;
        max-width: 40vw;
        max-height: 40vw;
        width: 100%;
        height: 100%;
        justify-items: center;
        align-items: center;
        align-self: center;
        margin: 0;
        box-sizing: border-box;
    }
    .image-grid img {
        width: 100%;
        max-width: 20vw;
        height: auto;
        max-height: 20vw;
        object-fit: contain;
        border-radius: 0.5rem;
        background: #fff2;
        box-shadow: 0 2px 8px #0002;
        transition: transform 0.2s;
        display: block;
    }
    .image-grid img:hover {
        transform: scale(1.05);
    }
    .darkness {
        background: #000;
        height: 6vh;
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        overflow: hidden;
        position: relative;
    }
    .scrolling-text {
        width: 100%;
        overflow: hidden;
        white-space: nowrap;
        position: relative;
        display: flex;
    }
    .scrolling-text span {
        display: inline-block;
        color: white;
        font-size: 1.5rem;
        font-family: 'Rubik', sans-serif;
        font-weight: bold;
        padding-right: 0.5rem;
        animation: scroll-right 30s linear infinite;
        white-space: nowrap;
    }
    @keyframes scroll-right {
        0% {
            transform: translateX(0);
        }
        100% {
            transform: translateX(-100%);
        }
    }

    .tall-section-2 {
        background: #A27ACA;
        min-height: 40.2rem;
        width: 100%;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        padding: 0 4vw;
        box-sizing: border-box;
    }
    .squares-indicator-wrapper {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        flex: 1 1 0%;
        height: 100%;
    }
    .squares-container {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        width: 100%;
        height: 70vh;
        gap: 3vw;
    }
    .round-square {
        width: 32vw;
        max-width: 420px;
        height: 32vw;
        max-height: 420px;
        background: #FF8686;
        border-radius: 32px;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 3rem;
        margin: 0;
        box-shadow: 0 4px 16px rgba(0,0,0,0.12);
        transition: transform 0.2s;
    }
    .indicators {
        display: flex;
        justify-content: center;
        margin-top: 24px;
        width: 100%;
    }
    .indicator {
        width: 40px;
        height: 6px;
        background: #fff;
        opacity: 0.4;
        border-radius: 3px;
        margin: 0 6px;
        transition: opacity 0.2s;
    }
    .indicator.active {
        opacity: 1;
        background: #FF8686;
    }
    .slide-right {
        animation: slideRight 0.35s cubic-bezier(0.4,0,0.2,1);
    }
    .slide-left {
        animation: slideLeft 0.35s cubic-bezier(0.4,0,0.2,1);
    }
    @keyframes slideRight {
        0% { transform: translateX(-60px); opacity: 0.7; }
        100% { transform: translateX(0); opacity: 1; }
    }
    @keyframes slideLeft {
        0% { transform: translateX(60px); opacity: 0.7; }
        100% { transform: translateX(0); opacity: 1; }
    }

    @media (max-width: 900px) {
        .tall-section {
            flex-direction: column;
            align-items: flex-start;
        }
        .image-grid {
            max-width: 90vw;
            max-height: none;
        }
        .image-grid img {
            max-width: 40vw;
        }
        .tall-section h1 {
            font-size: 2.5rem;
        }
    }
</style>