<script>
  import Proyecto from "./Proyecto.svelte";
  let proyectos = [
    {
      nombre: "Empresa de construcciones y reformas",
      imagen: "reformasmultiservicios.png",
      tecnologias: ["HTML", "CSS", "Javascript"],
      link_github: "https://github.com/Kevinrp22/Reformas-Multiservicios",
      link_proyecto: "http://reformasmultiservicios.herokuapp.com/",
      desarrollando: true,
    },
    {
      nombre: "Pizzeria",
      imagen: "proyecto-pizzeria.png",
      tecnologias: ["HTML", "CSS", "Javascript"],
      link_github: "https://github.com/Kevinrp22/ProyectoPizzeria",
      link_proyecto: "#",
      desarrollando: true,
    },
    {
      nombre: "Oposipol Academia",
      imagen: "oposipolacademia.png",
      tecnologias: ["HTML", "CSS", "Javascript", "Svelte"],
      link_github: "https://github.com/Kevinrp22/www.oposipolacademia.com",
      link_proyecto: "https://web-oposipol.vercel.app/",
      desarrollando: false,
    },
  ];
</script>

<div class="proyectos">
  {#each proyectos as proyecto}
    <Proyecto {proyecto} />
  {/each}
</div>
