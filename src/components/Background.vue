<template>
	<div class="Background" ref="root">
		<slot></slot>
	</div>
</template>

<script setup lang="ts">
import { ref, onMounted } from "vue"

let didScroll = false
let root = ref<HTMLDivElement>()

window.addEventListener("scroll", function () {
	didScroll = true
})

onMounted(() => {
	setInterval(makeSquare, 500)
	setInterval(function () {
		if (didScroll) {
			handleScroll()
			didScroll = false
		}
	}, 300)
})

const IconClasses = [
	"Background__i1",
	"Background__i2",
	"Background__i3",
	"Background__i4",
	"Background__i5",
	"Background__i6",
	"Background__i7",
	"Background__i8",
]

function makeSquare() {
	const wrapper = document.querySelector(".Background")
	const square = document.createElement("span")
	if (wrapper && square) {
		let size = Math.floor(Math.random() * 50)
		square.style.width = 20 + size + "px"
		square.style.height = 20 + size + "px"
		square.style.top = Math.random() * innerHeight + "px"
		square.style.left = Math.random() * innerWidth + "px"
		square.classList.add(
			IconClasses[Math.floor(Math.random() * IconClasses.length)]
		)
		wrapper.appendChild(square)
		setTimeout(() => square.remove(), 5000)
	}
}

function handleScroll() {
	if (window.scrollY > window.screen.height) {
		root.value?.classList.add("Background--blur")
	} else {
		root.value?.classList.remove("Background--blur")
	}
}
</script>

<style>
.Background {
	position: fixed;
	width: 100%;
	min-height: 100vh;
	transition: filter 0.5s ease;
	z-index: 0;
}

.Background--blur {
	filter: blur(3px);
}

.Background > span {
	position: absolute;
	/* background: #fff; */
	/* background: url("../assets/images/kuza.png"); */
	background-size: cover;
	animation: animate 5s linear infinite;
}

.Background__i1 {
	background: url("../assets/images/kuza.png");
}
.Background__i2 {
	background: url("../assets/images/kuza-2.png");
}
.Background__i3 {
	background: url("../assets/images/dev.png");
}
.Background__i4 {
	background: url("../assets/images/dev-2.png");
}
.Background__i5 {
	background: url("../assets/images/thc.png");
}
.Background__i6 {
	background: url("../assets/images/thc-2.png");
}
.Background__i7 {
	background: url("../assets/images/music.png");
}
.Background__i8 {
	background: url("../assets/images/music-2.png");
}

@keyframes animate {
	0% {
		transform: scale(0) translateY(0) rotate(0deg);
		opacity: 0;
	}
	10%,
	90% {
		opacity: 1;
	}
	100% {
		transform: scale(1) translateY(-100%) rotate(360deg);
		opacity: 0;
	}
}
</style>
