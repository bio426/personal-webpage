<template>
	<section class="contact" id="contact">
		<h2 class="App__subtitle">
			<span class="App__label">04.</span> Get in touch
		</h2>
		<p class="App__description">
			Currently I'm looking for new opportunities to work, so if you want me to
			work in your team, or have a project where you think I could be useful,
			send me an email, and we could start creating new software products.
		</p>
		<a class="contact__email" href="mailto:bildloar@gmail.com">Say Hello!</a>
	</section>
</template>

<style>
.contact {
	text-align: center;
}

.contact__description {
	margin-bottom: 2rem;
	color: var(--c-text);
}

.contact__email {
	display: inline-block;
	margin-bottom: 6rem;
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

.contact__email:hover{
	background: var(--c-green);
	box-shadow: 0.5rem 0.5rem 0 var(--c-yellow);
	letter-spacing: 1px;
}
</style>
