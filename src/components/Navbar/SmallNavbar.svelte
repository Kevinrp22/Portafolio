<script>
  import globalStore from "../../stores/globalStore";
  export let segment;
</script>

<style>
  .barra {
    cursor: pointer;
    position: absolute;
    right: 25px;
    top: 30px;
    color: var(--color-blanco);
    font-size: 1.5rem;
  }
</style>

<nav>
  <div class="logo">K</div>
  <div
    class="barra"
    on:click={() => {
      globalStore.toggleItem('sidebar', true);
    }}>
    <i class="fas fa-bars" />
  </div>
</nav>
