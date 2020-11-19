<script>
  import Nav from "../components/Navbar/Navbar.svelte";
  import Sidebar from "../components/Navbar/Sidebar.svelte";
  import globalStore from "../stores/globalStore";

  export let segment;
  let headerShadow = "pin";
  let y = 0;
  let lastY = 0;
  let lastDirection = "up";

  function changeClass(y) {
    let result = headerShadow;
    const scrolledPxs = lastY - y;
    const scrollDirection = scrolledPxs < 0 ? "down" : "up";
    const changedDirection = scrollDirection !== lastDirection;
    if (changedDirection) {
      result = scrollDirection === "down" ? "headerUp" : "headerDown";
      lastDirection = scrollDirection;
    }
    if (y == 0) {
      result = "";
    }
    lastY = y;
    return result;
  }

  $: headerShadow = changeClass(y);
  /* $: console.log(y) */
</script>

<style>
  main {
    position: relative;
    max-width: 56em;
    padding: 6.5em 2em;
    margin: 0 auto;
    box-sizing: border-box;
  }
  footer {
    text-align: center;
    margin: 0 auto;
    max-width: 56em;
    background-color: var(--color-azulFuerte);
    padding: 1.5rem;
  }
  footer p {
    margin: 0;
    padding: .5rem 0;
    color: var(--color-azul);
  }
</style>

<svelte:window bind:scrollY={y} />
{#if $globalStore.sidebar}
  <Sidebar />
{/if}
<header class={headerShadow}>
  <Nav {segment} />
</header>

<main>
  <slot />
</main>

<footer>
  <p>Diseñado y contruido por Kevin Puchaicela</p>
  <p>-2020-</p>
</footer>
