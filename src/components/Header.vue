<template>
	<header class="header" :class="{ 'header--hide': hideHeader }" ref="headerEl">
		<div class="header__container">
			<a href="/" aria-label="home">
				<img class="header__logo" src="../assets/icons/b.svg" alt="" />
			</a>
			<button class="header__button" @click="$emit('showSidebar')">
				<img class="header__ico" src="../assets/icons/menu.svg" alt="" />
			</button>
			<nav class="header__links">
				<a class="header__link" href="#about"
					><span class="header__label">01.</span> About me</a
				>
				<a class="header__link" href="#projects">
					<span class="header__label">02.</span>
					Projects</a
				>
				<a class="header__link" href="#readings">
					<span class="header__label">03.</span>
					Readings</a
				>
				<a class="header__link" href="#contact">
					<span class="header__label">04.</span>
					Contact</a
				>
			</nav>
		</div>
	</header>
</template>

<script setup lang="ts">
import { ref, onMounted, watch } from "vue"

const props = defineProps({
	hide: Boolean,
})
const emits = defineEmits(["showSidebar"])

let hideHeader = ref(false)
let headerEl = ref<HTMLElement>()

let didScroll = false
let previousTopOffset = 0
let delta = 5
let headerHeight = 0

window.addEventListener("scroll", function () {
	didScroll = true
})

onMounted(() => {
	previousTopOffset = window.scrollY
	headerHeight = (headerEl.value as HTMLElement).clientHeight
	setInterval(function () {
		if (didScroll) {
			handleScroll()
			didScroll = false
		}
	}, 300)
})

function handleScroll() {
	let topOffset = window.scrollY
	if (Math.abs(previousTopOffset - topOffset) < delta) return
	if (topOffset > previousTopOffset && topOffset > headerHeight) {
		hideHeader.value = true
	} else {
		if (topOffset + window.screen.height < document.body.clientHeight) {
			hideHeader.value = false
		}
	}
	previousTopOffset = topOffset
}

watch(
	() => props.hide,
	() => {
		if (props.hide) {
			hideHeader.value = true
		} else {
			hideHeader.value = false
		}
	}
)
</script>

<style>
.header {
	position: fixed;
	top: 0;
	width: 100%;
	padding: 1rem 0;
	background: rgba(0, 0, 0, 0.8);
	backdrop-filter: blur(5px);
	color: var(--c-green);
	border-bottom: 1px solid var(--c-green);
	transition: top 0.2s ease;
	z-index: 10;
}

.header--hide {
	top: -5rem;
}

.header__container {
	display: flex;
	justify-content: space-between;
	width: 90%;
	margin: 0 auto;
}

.header__logo {
	display: block;
	width: 2.5rem;
}

.header__button {
	display: block;
	background: none;
	border: none;
	outline: none;
	cursor: pointer;
}

.header__links {
	display: none;
	align-items: center;
	gap: 2rem;
}

.header__link {
	color: var(--c-text);
	font-family: "Inconsolata";
	/* letter-spacing: 1px; */
	text-decoration: none;
}

.header__label {
	color: var(--c-green);
	font-size: 0.9rem;
}

.header__ico {
	display: block;
	width: 2.5rem;
}

@media (min-width: 768px) {
	.header__container {
		width: 80%;
	}

	.header__button {
		display: none;
	}

	.header__links {
		display: flex;
	}
}

@media (min-width: 1024px) {
	.header__container {
		width: 70%;
	}
}
</style>
