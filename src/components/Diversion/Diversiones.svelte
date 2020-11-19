<script>
  import Diversion from "./Diversion.svelte";
  let diversiones = [];
</script>

<style>
  .icon-working {
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 5em;
  }
</style>

{#if diversiones.length > 0}
  <div class="diversiones">
    {#each diversiones as diversion}
      <Diversion {diversion} />
    {/each}
  </div>
{:else}
  <div class="icon-working"><i class="fas fa-cogs" /></div>
{/if}
