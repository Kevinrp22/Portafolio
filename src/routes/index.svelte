<script>
	import Diversiones from "../components/Diversion/Diversiones.svelte";
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
		text-align: justify;
	}
	.lista-code {
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		gap: 10px;
		padding: 0.6rem 0 0 0;
		margin: 0;
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
	#sobre-mi .titulo-section {
		padding: 8rem 0 0.5rem 0;
	}
	/* SECTION PROYECTOS */
	/* SECTION CONTACTO */
	.form {
		display: flex;
		flex-direction: column;
		background-color: var(--background-secundario);
		padding: 1rem;
	}
	.form__input {
		padding: 1rem;
		margin: 0.2rem 0;
		font-size: 1em;
	}
	.form textarea {
		margin: 0.2rem 0 0.6rem 0;
		padding: 1rem;
		height: 100px;
		resize: none;
	}
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
</section>
<section id="por-diversion" class="contenedor">
	<h2 class="titulo-section">Por diversión</h2>
	<Diversiones />
</section>

<section id="contacto" class="contenedor">
	<h2 class="titulo-section">Contacto</h2>
	<div class="formulario">
		<form method="POST" action="https://formsubmit.co/kevinpuchaicela@gmail.com" enctype="multipart/form-data" class="form">
			<input class="form__input" type="text" name="name" placeholder="Tu nombre" required />
			<input class="form__input" type="tel" name="tel" placeholder="Teléfono (Opcional)" />
			<input class="form__input" type="email" name="email" placeholder="Email" required />
			<input class="form__input" type="text" name="message" placeholder="Asunto" required />
			<textarea type="text" placeholder="Mensaje / Consulta" required />
			<input class="btn" type="submit" value="ENVIAR FORMULARIO" />
		</form>
	</div>
</section>
