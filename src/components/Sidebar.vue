<template>
	<div class="Sidebar">
		<img class="Sidebar__logo" src="../assets/icons/b.svg" alt="" />
		<button class="Sidebar__close" @click="$emit('hideSidebar')">
			<img class="Sidebar__ico" src="../assets/icons/close.svg" alt="" />
		</button>
		<div class="Sidebar__main">
			<a class="Sidebar__link" href="#about" @click="$emit('hideSidebar')">
				<span class="Sidebar__label">01.</span>
				About</a>
			<a class="Sidebar__link" href="#projects" @click="$emit('hideSidebar')">
				<span class="Sidebar__label">02.</span>
				Projects</a>
			<a class="Sidebar__link" href="#readings" @click="$emit('hideSidebar')">
				<span class="Sidebar__label">03.</span>
				Readings</a>
			<a class="Sidebar__link" href="#contact" @click="$emit('hideSidebar')">
				<span class="Sidebar__label">04.</span>
				Contact</a>
		</div>
	</div>
</template>

<script setup lang="ts">
const emits = defineEmits(["hideSidebar"])
</script>

<style>
.Sidebar {
	position: fixed;
	display: flex;
	justify-content: center;
	align-items: center;
	width: 100%;
	height: 100vh;
	background: rgba(0, 0, 0, 0.8);
	z-index: 10;
}

.Sidebar__logo {
	position: absolute;
	top: 1rem;
	left: 5%;
	display: block;
	width: 2.5rem;
}

.Sidebar__close {
	position: absolute;
	top: 1rem;
	right: 5%;
	display: block;
	background: none;
	border: none;
	outline: none;
	cursor: pointer;
}

.Sidebar__main {
	display: flex;
	flex-direction: column;
	align-items: center;
	gap: 1rem;
	max-width: 90%;
}

.Sidebar__link {
	display: block;
	color: #fff;
	font-size: 2rem;
	font-family: "Inconsolata", monospace;
	text-decoration: none;
}

.Sidebar__link:hover{
	color: var(--c-yellow);
}

.Sidebar__label{
	color: var(--c-green);
	font-size: 1.5rem;
}

.Sidebar__ico {
	display: block;
	width: 2rem;
}
</style>
