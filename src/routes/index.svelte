<script>
	import Proyectos from "../components/Proyectos/Proyectos.svelte";
</script>

<style>
	:global(html) {
		scroll-behavior: smooth;
	}
	.mi-nombre {
		font-size: clamp(60px, 8vw, 90px);
		font-weight: 800;
		color: var(--color-blanco);
		margin: 0.2rem 0;
	}
	.subtitulo {
		font-size: 3em;
		font-weight: 500;
		margin: 0;
	}
	.descripcion {
		padding: 1rem 0;
		text-align: justify;
	}
	/* SECTION SOBRE MI */
	.sobre-mi__content__texto {
		margin: 3rem 0;
	}
	.lista-code {
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		gap: 10px;
		margin: 0;
		padding: 0;
		list-style: circle;
	}
	.lista-code__li {
		font-weight: 400;
		font-size: 0.9em;
		display: flex;
		align-items: center;
	}
	.lista-code__li__svg {
		margin-right: 10px;
		width: 20px;
	}
	.sobre-mi__content__imagen-perfil {
		display: flex;
		justify-content: center;
		align-items: center;
	}
	.sobre-mi__content__imagen-perfil__img {
		cursor: pointer;
		width: 250px;
		mix-blend-mode: luminosity;
		opacity: 0.8;
		transition: all 0.25s cubic-bezier(0.645, 0.045, 0.355, 1);
	}
	.sobre-mi__content__imagen-perfil__img:hover {
		mix-blend-mode: normal;
		opacity: 1;
	}
	/* SECTION PROYECTOS */
</style>

<section>
	<p class="color-azul"><strong>Hola, mi nombre es</strong></p>
	<h1 class="mi-nombre">Kevin Puchaicela</h1>
	<h2 class="subtitulo">Desarrollador web.</h2>
	<p class="descripcion">
		Actualmente estoy estudiando
		<strong class="color-azul">1º de Desarrollo de aplicaciones web </strong>en
		el Instituto CIFP Francesc de borja moll.
		<br />
		<br />
		Me gusta mucho el desarrollo de páginas web, he ido aprendiendo poco a poco
		diferentes tecnologias.
		<br />
		<br />
		Mis conocimientos se orientas más al mundo
		<strong class="color-azul">Frontend</strong>
		aunque me gusta conocer ambos ámbitos, estoy aprendiendo como funciona el
		mundo Backend
	</p>
	<button class="btn"><a href="mailto:kemalan@hotmail.es">Contactar</a></button>
</section>

<section id="sobre-mi">
	<h2 class="titulo-section">Sobre mi</h2>
	<div class="sobre-mi__content">
		<div class="sobre-mi__content__texto">
			<p>
				Actualmente estoy estudiando
				<strong class="color-azul">1º de Desarrollo de aplicaciones web
				</strong>en el Instituto CIFP Francesc de borja moll.
			</p>
			<p>
				Me gusta mucho el desarrollo de páginas web, he ido aprendiendo poco a
				poco diferentes tecnologias.
			</p>
			<p>
				Mis conocimientos se orientas más al mundo
				<strong class="color-azul">Frontend</strong>
				aunque me gusta conocer ambos ámbitos, estoy aprendiendo como funciona
				el mundo Backend.
			</p>
			<p>Estas son las tecnologías con las que trabajo:</p>
			<ul class="lista-code">
				<li class="lista-code__li">
					<img src="html.svg" alt="" class="lista-code__li__svg" />
					HTML
				</li>
				<li class="lista-code__li">
					<img src="css.svg" alt="" class="lista-code__li__svg" />
					CSS
				</li>
				<li class="lista-code__li">
					<img src="javascript.svg" alt="" class="lista-code__li__svg" />
					Javascript
				</li>
				<li class="lista-code__li">
					<img src="jquery.svg" alt="" class="lista-code__li__svg" />
					Jquery
				</li>
				<li class="lista-code__li">
					<img src="git.svg" alt="" class="lista-code__li__svg" />
					Git
				</li>
				<li class="lista-code__li">
					<img src="bootstrap.svg" alt="" class="lista-code__li__svg" />
					Bootstrap
				</li>
				<li class="lista-code__li">
					<img src="wordpress.svg" alt="" class="lista-code__li__svg" />
					Wordpress
				</li>
				<li class="lista-code__li">
					<img src="svelte-icon.svg" alt="" class="lista-code__li__svg" />
					Svelte
				</li>
				<li class="lista-code__li">
					<img src="node-js.svg" alt="" class="lista-code__li__svg" />
					NodeJS
				</li>
				<li class="lista-code__li">
					<img src="adobe.svg" alt="" class="lista-code__li__svg" />
					Photoshop
				</li>
				<li class="lista-code__li">
					<img src="adobe-illustrator.svg" alt="" class="lista-code__li__svg" />
					Illustrator
				</li>
			</ul>
		</div>
		<div class="sobre-mi__content__imagen-perfil">
			<img
				src="foto-carnet.png"
				alt="ilustracion-code3"
				class="sobre-mi__content__imagen-perfil__img" />
		</div>
	</div>
</section>

<section id="proyectos">
	<h2 class="titulo-section">Proyectos</h2>
	<Proyectos />
	<div class="contenedor-proyectos my-5">
		<!-- <div class="proyecto py-4">
			<div style="display: none; " class="titulo-arriba-proyecto">
				<h4>Empresa de Construcciones y Reformas</h4>
				<p style="font-size: 11px; color: #447f91;">HTML | CSS | JAVASCRIPT</p>
			</div>
			<div class="imagen-proyecto">
				<a href="https://reformasmultiservicios.herokuapp.com/" target="_blank">
					<img class="img-fluid" src="#" alt="" />
				</a>
			</div>

			<div class="texto-proyecto">
				<div class="titulo-derecha-proyecto">
					<h4 style="font-size: 1.3rem;">
						Empresa de Construcciones y Reformas
					</h4>
					<p style="font-size: 11px; color: #447f91;">
						HTML | CSS | JAVASCRIPT
					</p>
				</div>

				<div class="contenedor-mirar my-2">
					<div class="bloque-mirar">
						<a href="#">
							<div style="display: flex;" class="arriba">
								<i
									style="font-size: 20px;margin: 0px 5px 0px 0px;"
									class="fab fa-github" />
								<p style="margin-bottom: 0;">Ver en Github</p>
							</div>
						</a>
					</div>
				</div>
				<div class="contenedor-mirar my-2">
					<div class="bloque-mirar">
						<a
							href="https://reformasmultiservicios.herokuapp.com/"
							target="_blank">
							<div style="display: flex;" class="arriba">
								<i
									style="font-size: 20px;margin: 0px 10px 0px 0px;"
									class="fas fa-folder-open" />
								<p style="margin-bottom: 0;">Ver Proyecto</p>
							</div>
							<p
								class="en-desarrollo"
								style="margin-bottom: 0; font-size: 10px;">
								(En desarrollo)
							</p>
						</a>
					</div>
				</div>
			</div>
		</div> -->
	</div>
</section>
<section id="por-diversion" class="contenedor">
	<div class="titulo-section">
		<h2 style="min-width: 213px; width: 300px;">Por diversión</h2>
		<hr />
	</div>
	<div class="working"><i class="fas fa-cogs" /></div>

	<div class="contenedor-por-diversion" />
</section>

<section id="contacto" class="contenedor">
	<div class="titulo-section">
		<h2>Contacto</h2>
		<hr />
	</div>
	<div class="c-formu">
		<div class="formu">
			<form action="" class="__colums__form">
				<input type="text" placeholder="Tu nombre" required />
				<input type="tel" placeholder="Teléfono (Opcional)" />
				<input type="email" placeholder="Email" required />
				<input type="text" placeholder="Asunto" required />
				<textarea type="text" placeholder="Mensaje / Consulta" required />
				<input type="submit" value="ENVIAR FORMULARIO" class="boton-contacto" />
			</form>
		</div>
	</div>
</section>
