<template>
	<section class="welcome">
		<h2 class="welcome__salute">Hi, my name is</h2>
		<span class="welcome__name">Bild Lopez</span>
		<span class="welcome__phrase">I build things for the web.</span>
		<p class="welcome__description">
			I'm a passionate junior web developer specialized in front-end, willing to
			help small business in my locality to integrate the technology to make
			their work easier and enjoyable.
		</p>
		<a href="" class="welcome__action">Check out my resume</a>
	</section>
</template>

<style>
.welcome {
	display: flex;
	flex-direction: column;
	justify-content: center;
	height: 100vh;
}

.welcome__salute {
	margin-bottom: 1rem;
	color: var(--c-green);
	font-family: "Inconsolata";
}

.welcome__name {
	margin-bottom: 1rem;
	color: var(--c-text);
	font-family: "Inconsolata";
	font-size: 2.5rem;
	font-weight: 900;
}

.welcome__phrase {
	margin-bottom: 1rem;
	color: var(--c-text);
	font-family: "Inconsolata";
	font-size: 2.5rem;
	font-weight: 700;
}

.welcome__description {
	margin-bottom: 4rem;
	line-height: 2;
	color: var(--c-text);
}

.welcome__action {
	position: relative;
	display: inline-block;
	margin: 0 auto;
	padding: 1rem 2rem;
	background: var(--c-yellow);
	color: var(--c-background);
	font-family: "Inconsolata";
	font-size: 1.2rem;
	font-weight: 600;
	text-decoration: none;
	cursor: pointer;
	transition: .5s;

	/* Decoration */
	box-shadow: 0.5rem 0.5rem 0 var(--c-green);
}

.welcome__action:hover {
	background: var(--c-green);
	box-shadow: 0.5rem 0.5rem 0 var(--c-yellow);
	letter-spacing: 1px;
}

@media (min-width: 768px) {
	.welcome__salute {
		font-size: 1.5rem;
	}

	.welcome__name {
		font-size: 3rem;
	}

	.welcome__phrase {
		font-size: 3rem;
	}

	.welcome__description {
		font-size: 1.2rem;
	}
}

@media (min-width: 1024px) {
	.welcome__salute {
		font-size: 1.5rem;
	}

	.welcome__name {
		font-size: 4rem;
	}

	.welcome__phrase {
		font-size: 4rem;
	}

	.welcome__description {
		font-size: 1.2rem;
	}
}
</style>
