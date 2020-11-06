<script>
  import { afterUpdate, beforeUpdate, onMount } from "svelte";
  import globalStore from "../../stores/globalStore";
  onMount(() => {
    window.document.body.classList.toggle("overflow-html");
    console.log($globalStore.sidebar);
    let links = document.querySelectorAll(".sidebar .sidebar__link");
    links.forEach((link) => {
      console.log(link);
      link.addEventListener("click", () => {
        globalStore.toggleItem("sidebar", false);
      });
    });

    console.log($globalStore.sidebar);
  });
</script>

<style>
  .sidebar {
    display: flex;
    flex-direction: column;
    background-color: var(--background-secundario);
    position: fixed;
    height: 100vh;
    bottom: 0;
    top: 0;
    transition: width 0.5s ease;
    width: 200px;
    padding: 6rem 2rem;
    z-index: 111;
  }
  .sidebar__link {
    display: block;
    font-weight: 500;
    padding: 20px;
  }
  .sidebar__link:hover {
    color: var(--color-azul);
    font-weight: 600;
  }

  .sidebar__link i {
    width: 20px;
    margin-right: 0.5rem;
  }
  .sidebar__close {
    cursor: pointer;
    position: absolute;
    font-size: 2em;
    color: var(--color-azul);
    top: 30px;
    left: 30px;
  }
  .sidebar__close:hover {
    color: var(--color-blanco);
  }
</style>

<ul class="sidebar">
  <li><a href="/" class="sidebar__link"><i class="fas fa-home" />Inicio</a></li>
  <li>
    <a href="#sobre-mi" class="sidebar__link"><i
        class="fas fa-graduation-cap" />Sobre mi</a>
  </li>
  <li>
    <a href="#proyectos" class="sidebar__link"><i
        class="fas fa-folder-open" />Proyectos</a>
  </li>
  <li>
    <a href="#contacto" class="sidebar__link"><i
        class="fas fa-at" />Contacto</a>
  </li>
  <span
    class="sidebar__close"
    on:click={() => {
      globalStore.toggleItem('sidebar', false);
    }}><i class="fas fa-times" /></span>
</ul>
