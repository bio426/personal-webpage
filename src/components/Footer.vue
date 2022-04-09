<template>
	<footer class="Footer">
		<ul class="Footer__links">
			<li>
				<a class="Footer__link" href="https://github.com/bio426">
					<img class="Footer__ico" src="../assets/icons/github.svg" alt="link icon" />
				</a>
			</li>
			<li>
				<a class="Footer__link" href="https://www.linkedin.com/in/loarbild/">
					<img class="Footer__ico" src="../assets/icons/linkedin.svg" alt="link icon" />
				</a>
			</li>
			<li>
				<a class="Footer__link" href="https://twitter.com/LopezBild">
					<img class="Footer__ico" src="../assets/icons/twitter.svg" alt="link icon" />
				</a>
			</li>
		</ul>
		<p class="Footer__credit">
			Designed and Developed by <span class="Footer__author">Bild Lopez A.</span>
		</p>
	</footer>
</template>

<style>
.Footer {
	position: relative;
  padding-bottom: 2rem;
}

.Footer__container {
}

.Footer__links {
	display: flex;
  justify-content: center;
	gap: 2rem;
  margin-bottom: 2rem;
}

.Footer__link {
	cursor: pointer;
}

.Footer__ico {
	display: block;
	width: 1.5rem;
}

.Footer__credit {
	color: var(--c-text);
	font-family: "Inconsolata";
  text-align: center;
}

.Footer__author{
  color: var(--c-yellow);
}
</style>
