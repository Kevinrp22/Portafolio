<script>
  export let proyecto;
  let {
    nombre,
    imagen,
    tecnologias,
    link_github,
    link_proyecto,
    desarrollando,
  } = proyecto;
  tecnologias = tecnologias.join(" | "); // cambiamos las comas del array por "|"
  console.log(link_proyecto);
</script>

<style>
  .proyecto {
    margin-bottom: 2rem;
  }
  .proyecto:last-child{
    margin-bottom: 0px;
  }
  .proyecto__titulo {
    font-size: 1.5em;
    color: var(--color-blanco);
  }
  .proyecto__tecnologias {
    font-size: 11px;
    color: #447f91;
  }
  .en-desarrollo {
    color: var(--color-blanco); /* #ffd91ed1 */
    background-color: brown;
    padding: 0.3rem;
    border-radius: 4px;
    margin-left: 5px;
  }

  .proyecto__imagen {
    cursor: pointer;
    position: relative;
  }
  /* .proyecto__imagen a::before {
    content: "";
    position: absolute;
    background-color: #1f324dcf;
    top: 0;
    bottom: 0;
    width: 100%;
    height: 100%;
  }
  .proyecto__imagen a::after {
    content: "";
    position: absolute;
    box-sizing: border-box;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: url("/open.svg") no-repeat;
    background-size: 50% ;
    font-size: 1.2em;
    padding: 1rem;
    z-index: 11;
  } */
  .proyecto__links {
  }
  .proyecto__links__link {
    background-color: var(--background-secundario);
    color: var(--color-blanco);
    padding: 1rem 0;
    margin: 0.5rem 0;
    text-align: center;
    border-radius: 4px;
  }
  .proyecto__links__link:hover {
    background-color: var(--hover);
  }
  .hover-img {
    position: absolute;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    font-size: 1.9em;
    background-color: #1f324dcf;
    width: 100%;
    color: var(--color-blanco);
    height: 100%;
    top: 0;
    opacity: 0;
    transition: var(--transition);
  }
  .hover-img__icon {
    background-color: var(--background-secundario);
    padding: 1rem;
    border-radius: 100%;
  }

  .proyecto__imagen:hover .hover-img {
    opacity: 1;
    transition: var(--transition);
  }
</style>

<div class="proyecto">
  <h3 class="proyecto__titulo">{nombre}</h3>
  <p class="proyecto__tecnologias">
    {tecnologias}
    {#if desarrollando}
      <span class="en-desarrollo">Proyecto en desarrollo</span>
    {/if}
  </p>
  <div class="proyecto__imagen">
    <a href={link_proyecto} target="_blank">
      <img class="img-fluid" src={imagen} alt="" />
    </a>
    <a href={link_proyecto} class="hover-img"><i
        class="fas fa-external-link-alt hover-img__icon" /></a>
  </div>
  <!-- style="font-size: 20px;margin: 0px 5px 0px 0px;" -->
  <div class="proyecto__links">
    <a href={link_github}>
      <div class="proyecto__links__link">
        <i class="fab fa-github" />
        Ver en Github
      </div>
    </a>
    <a href={link_proyecto}>
      <div class="proyecto__links__link">
        <i class="fas fa-folder-open" />
        Ver proyecto
      </div>
    </a>
  </div>
</div>
