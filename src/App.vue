<template>
	<div class="App">
		<Background />
		<Header @show-sidebar="toogleSidebar" :hide="showSidebar" />
		<Sidebar v-if="showSidebar" @hide-sidebar="toogleSidebar" />
		<div class="App__container">
			<Swelcome />
			<SAbout />
			<SProjects />
			<SReadings />
			<SContact />
		</div>
		<Footer />
	</div>
</template>

<script setup lang="ts">
import { ref } from "vue"

import Background from "./components/Background.vue"
import Header from "./components/Header.vue"
import Sidebar from "./components/Sidebar.vue"
import Swelcome from "./components/sections/welcome.vue"
import SAbout from "./components/sections/about.vue"
import SProjects from "./components/sections/projects.vue"
import SReadings from "./components/sections/readings.vue"
import SContact from "./components/sections/contact.vue"
import Footer from "./components/Footer.vue"

let showSidebar = ref(false)

function toogleSidebar() {
	if (showSidebar.value) {
		showSidebar.value = false
		document.body.style.overflow = "auto"
	} else {
		showSidebar.value = true
		document.body.style.overflow = "hidden"
	}
}
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Inconsolata:wght@300;500;700;900&display=swap");

* {
	margin: 0;
	padding: 0;
	box-sizing: border-box;
	font-size: 16px;
	font-weight: normal;
	font-family: sans-serif;
}

html {
	scroll-behavior: smooth;
}

:root {
	--c-green: #75d03c;
	--c-yellow: #e1dc4b;
	--c-gray: #111111;
	--c-background: #000;
	--c-text: #fff;
}

.App {
	position: relative;
	background: #000;
	min-height: 100vh;
}

.App__container {
	position: relative;
	width: 90%;
	margin: 0 auto;
	z-index: 5;
}

.App__subtitle {
	margin-bottom: 1rem;
	padding-bottom: 0.5rem;
	color: var(--c-text);
	border-bottom: 1px solid #fff;
	font-family: "Inconsolata";
	font-size: 1.5rem;
	font-weight: 600;
	letter-spacing: 4px;
}

.App__label {
	color: var(--c-green);
}

.App__description {
	margin-bottom: 3rem;
	color: var(--c-text);
	line-height: 1.5;
}

@media (min-width: 768px) {
	.App__container {
		width: 70%;
	}

	.App__subtitle{
		font-size: 2rem;
	}

	.App__label {
	font-size: 1.2rem;
}

	.App__description{
		font-size: 1.2rem;
	}
}

@media (min-width: 1024px) {
	.App__container {
		width: 60%;
	}
}
</style>
