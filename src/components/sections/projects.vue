<template>
	<section class="projects" id="projects">
		<h2 class="App__subtitle"><span class="App__label">02.</span> Projects</h2>
		<p class="App__description">
			There are some projects i build to showcase my knowledge on the web
			technologies.
		</p>
		<ul class="projects__list">
			<li>
				<div class="Project Project__bg1">
					<h4 class="Project__title">Porcus Clone</h4>
					<p class="Project__description">
						A Clone of the Porcus Website, with the dinamic animations, brand
						colors and responsive design.
					</p>
					<ul class="Project__tecnologies">
						<li class="Project__tecnology">Nuxt</li>
						<li class="Project__tecnology">Typescript</li>
						<li class="Project__tecnology">Sass</li>
					</ul>
					<div class="Project__links">
						<a
							class="Project__link"
							href="https://github.com/bio426/porcus-clone/blob/main/README.md"
							><img class="Project__ico" src="../../assets/icons/link.svg"
						/></a>
						<a
							class="Project__link"
							href="https://github.com/bio426/porcus-clone"
							><img class="Project__ico" src="../../assets/icons/github.svg"
						/></a>
					</div>
				</div>
			</li>
			<li>
				<div class="Project Project__bg2">
					<h4 class="Project__title">GS Desktop App</h4>
					<p class="Project__description">
						A desktop application to help with the generation and storage of pdf
						documents for a mechanical workshop.
					</p>
					<ul class="Project__tecnologies">
						<li class="Project__tecnology">Electron.js</li>
						<li class="Project__tecnology">Bootstrap 5</li>
						<li class="Project__tecnology">PdjKit</li>
					</ul>
					<div class="Project__links">
						<a
							class="Project__link"
							href="https://github.com/bio426/gs-systems/blob/main/README.md"
							><img class="Project__ico" src="../../assets/icons/link.svg"
						/></a>
						<a class="Project__link" href="https://github.com/bio426/gs-systems"
							><img class="Project__ico" src="../../assets/icons/github.svg"
						/></a>
					</div>
				</div>
			</li>
			<li>
				<div class="Project Project__bg3">
					<h4 class="Project__title">Delivery Webapp UX</h4>
					<p class="Project__description">
						An implementation of an external UX Design Project, with some of the
						provided application functionality and user workflow.
					</p>
					<ul class="Project__tecnologies">
						<li class="Project__tecnology">Vue.js</li>
						<li class="Project__tecnology">Vite</li>
						<li class="Project__tecnology">Sass</li>
					</ul>
					<div class="Project__links">
						<a
							class="Project__link"
							href="https://github.com/bio426/delivery-webapp-ux/blob/main/README.md"
							><img class="Project__ico" src="../../assets/icons/link.svg"
						/></a>
						<a
							class="Project__link"
							href="https://github.com/bio426/delivery-webapp-ux"
							><img class="Project__ico" src="../../assets/icons/github.svg"
						/></a>
					</div>
				</div>
			</li>
			<li>
				<div class="Project Project__bg4">
					<h4 class="Project__title">Delivery Webapp UX</h4>
					<p class="Project__description">
						An implementation of an external UX Design Project, with some of the
						provided application functionality and user workflow.
					</p>
					<ul class="Project__tecnologies">
						<li class="Project__tecnology">Vue.js</li>
						<li class="Project__tecnology">Vite</li>
						<li class="Project__tecnology">Sass</li>
					</ul>
					<div class="Project__links">
						<a
							class="Project__link"
							href="https://github.com/bio426/delivery-webapp-ux/blob/main/README.md"
							><img class="Project__ico" src="../../assets/icons/link.svg"
						/></a>
						<a
							class="Project__link"
							href="https://github.com/bio426/delivery-webapp-ux"
							><img class="Project__ico" src="../../assets/icons/github.svg"
						/></a>
					</div>
				</div>
			</li>
		</ul>
	</section>
</template>

<style>
.projects {
}

.projects__list {
	display: grid;
	grid-template-columns: 1fr;
	gap: 1rem;
	margin-bottom: 4rem;
}

.Project {
	padding: 1rem;
	background: var(--c-gray);
	background-image: linear-gradient(
			rgba(17, 17, 17, 0.9),
			rgba(17, 17, 17, 0.9)
		),
		url("https://networks.imdea.org/wp-content/uploads/2021/09/media-file-code-900x500.png");
	background-size: cover;
}

.Project__bg1 {
	background-image: linear-gradient(
			rgba(17, 17, 17, 0.9),
			rgba(17, 17, 17, 0.9)
		),
		url("https://raw.githubusercontent.com/bio426/porcus-clone/main/docs/index-desktop.png");
}

.Project__bg2 {
	background-image: linear-gradient(
			rgba(17, 17, 17, 0.9),
			rgba(17, 17, 17, 0.9)
		),
		url("https://raw.githubusercontent.com/bio426/gs-systems/main/docs/index-view.png");
}

.Project__bg3 {
	background-image: linear-gradient(
			rgba(17, 17, 17, 0.9),
			rgba(17, 17, 17, 0.9)
		),
		url("https://raw.githubusercontent.com/bio426/delivery-webapp-ux/main/docs/index.png");
}

.Project__title {
	margin-bottom: 1rem;
	color: var(--c-text);
	font-size: 1.5rem;
	font-weight: 600;
}
.Project__description {
	margin-bottom: 1rem;
	color: var(--c-text);
}
.Project__tecnologies {
	display: flex;
	gap: 1rem;
	margin-bottom: 1rem;
	list-style: none;
}
.Project__tecnology {
	color: var(--c-green);
}

.Project__links {
	display: flex;
	flex-direction: row-reverse;
	gap: 1rem;
}
.Project__link {
}

.Project__ico {
	display: block;
	width: 1.5rem;
}

@media (min-width: 768px) {
	.projects__list {
		grid-template-columns: repeat(2, 1fr);
	}
}
</style>
