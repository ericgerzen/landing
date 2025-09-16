<script lang="ts">
  // Section IDs for scrolling
  const sections = [
    'inicio',
    'quienes-somos',
    'nuestros-objetivos',
    'la-plataforma',
    'ingresar-ahora'
  ];

  function scrollToSection(id: string) {
    const el = document.getElementById(id);
    if (el) {
      el.scrollIntoView({ behavior: 'smooth' });
    }
  }
</script>

<nav class="navbar">
  {#each sections as section, i}
    <button class="nav-title" on:click={() => scrollToSection(section)}>
      {#if i === 0}Inicio{/if}
      {#if i === 1}Quienes Somos{/if}
      {#if i === 2}Nuestros Objetivos{/if}
      {#if i === 3}La Plataforma{/if}
      {#if i === 4}Ingresar Ahora{/if}
    </button>
  {/each}
</nav>

<style>
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 64px;
  background: #fff;
  box-shadow: 0 2px 8px rgba(0,0,0,0.06);
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 1000;
}
.nav-title {
  background: none;
  border: none;
  color: #3A3A3A;
  font-size: 1.1rem;
  font-family: 'Rubik', sans-serif;
  font-weight: 500;
  margin: 0 2vw;
  cursor: pointer;
  padding: 0.5rem 1rem;
  border-radius: 20px;
  transition: background 0.2s, color 0.2s;
}
.nav-title:hover {
  background: #F0F0F0;
  color: #6C63FF;
}
@media (max-width: 600px) {
  .navbar {
    height: 48px;
  }
  .nav-title {
    font-size: 0.95rem;
    margin: 0 1vw;
    padding: 0.3rem 0.7rem;
  }
}
</style>

