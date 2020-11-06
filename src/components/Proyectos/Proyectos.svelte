<script>
  import Proyecto from "./Proyecto.svelte";
  let proyectos = [
    {
      nombre: "Pizzeria",
      imagen: "proyecto-pizzeria.png",
      tecnologias: ["HTML", "CSS", "Javascript"],
      link_github: "https://github.com/Kevinrp22/ProyectoPizzeria",
      link_proyecto: "#",
      desarrollando: false,
    },
    {
      nombre: "Empresa de construcciones y reformas",
      imagen: "reformasmultiservicios.png",
      tecnologias: ["HTML", "CSS", "Javascript"],
      link_github: "https://github.com/Kevinrp22/Reformas-Multiservicios",
      link_proyecto: "http://reformasmultiservicios.herokuapp.com/",
      desarrollando: false,
    },
  ];
</script>

<div class="proyectos">
  {#each proyectos as proyecto}
    <Proyecto {proyecto} />
  {/each}
</div>
