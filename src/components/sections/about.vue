<template>
	<section class="abilities" id="about">
		<h2 class="App__subtitle"><span class="App__label">01.</span> About me</h2>
		<p class="App__description">
			Hello! I'm Bild and i enjoy creating applications to help people. My
			interest in programing started back then in 2019 when i decide to write
			some small python scripts to make some macros in computer games.
			<br /><br />
			After that in my first years of software engineering career, i improve my
			knowledge in algorithms and data structures using Python, that led me to
			start studying web technologies and make the change to nodejs so i can
			specialize in Javascript and Vue.
			<br /><br />
			Since then, it has been a journey of lots of learning, through concepts of
			back-end and front-end, exploring other programing languages related to
			the web, and know how to apply architectural patterns to make the
			applications maintainable for the developers and enjoyable for the users.
			<br /><br />
			Here are some of the technologies i've been using.
		</p>
		<ul class="abilities__list">
			<li class="abilities__box">
				<span class="abilities__name"
					><strong>Javascript</strong> <br />
					(ES6, Typescript, Vue.js, Vite, Electron)
				</span>
				<a class="abilities__link" href="">
					<img
						class="abilities__logo"
						src="../../assets/logos/javascript.svg"
						alt=""
					/>
				</a>
			</li>
			<li class="abilities__box">
				<span class="abilities__name"
					><strong>Node.js</strong> <br />
					(Express, Fastify, REST, MongoDB, Jest)
				</span>
				<a class="abilities__link" href="">
					<img
						class="abilities__logo"
						src="../../assets/logos/nodejs.svg"
						alt=""
					/>
				</a>
			</li>
			<li class="abilities__box">
				<span class="abilities__name"
					><strong>Html & CSS</strong> <br />
					(Responsive Web Design, Tailwind CSS, Sass, BEM)
				</span>
				<a class="abilities__link" href="">
					<img
						class="abilities__logo"
						src="../../assets/logos/html.svg"
						alt=""
					/>
				</a>
			</li>
			<li class="abilities__box">
				<span class="abilities__name"
					><strong>PHP</strong> <br />
					(Laravel 8, Composer, PhpUnit)
				</span>
				<a class="abilities__link" href="">
					<img
						class="abilities__logo"
						src="../../assets/logos/php.svg"
						alt=""
					/>
				</a>
			</li>
			<li class="abilities__box">
				<span class="abilities__name"
					><strong>Go</strong> <br />
					(Algorithms and Data Structures, Echo)
				</span>
				<a class="abilities__link" href="">
					<img class="abilities__logo" src="../../assets/logos/go.svg" alt="" />
				</a>
			</li>
			<li class="abilities__box">
				<span class="abilities__name"
					><strong>Google Cloud Platform</strong> <br />
					(Firebase, App Engine, Cloud Functions)
				</span>
				<a class="abilities__link" href="">
					<img
						class="abilities__logo"
						src="../../assets/logos/gcp.svg"
						alt=""
					/>
				</a>
			</li>
		</ul>
		<img
			class="abilities__image"
			src="https://brittanychiang.com/static/30a645f7db6038f83287d0c6042d3b2b/754ad/me.jpg"
			alt=""
		/>
	</section>
</template>

<style>
.abilities {
}

.abilities__list {
	display: grid;
	grid-template-columns: repeat(2, 1fr);
	gap: 1rem;
	margin-bottom: 2rem;
}

.abilities__box {
	display: flex;
	justify-content: center;
	align-items: center;
	gap: 1rem;
}

.abilities__name {
	color: var(--c-text);
	text-align: center;
	line-height: 1.5;
}

.abilities__name > strong {
	font-weight: 600;
}

.abilities__logo {
	display: block;
	width: 2rem;
}

.abilities__image {
	position: relative;
	display: block;
	width: 70%;
	margin: 0 auto;
	margin-bottom: 4rem;
	filter: grayscale(100%);
}

@media (min-width: 768px) {
}

@media (min-width: 1024px) {
}
</style>
