<script setup>
import { RouterLink, RouterView } from 'vue-router'
import { ref, onMounted, onUnmounted } from 'vue'
import { gsap } from 'gsap'

const blob = ref(null)
const mouseX = ref(0)
const mouseY = ref(0)
const posX = ref(0)
const posY = ref(0)
let animationFrame = null

const updateBlobPosition = () => {
  posX.value = gsap.utils.interpolate(posX.value, mouseX.value, 0.2)
  posY.value = gsap.utils.interpolate(posY.value, mouseY.value, 0.2)

  gsap.to(blob.value, {
    x: posX.value,
    y: posY.value,
    duration: 0.8,
    ease: 'power2.out',
  })

  animationFrame = requestAnimationFrame(updateBlobPosition)
}

const handleMouseMove = (e) => {
  mouseX.value = Math.min(
    Math.max(e.clientX, blob.value.offsetWidth / 2),
    window.innerWidth - blob.value.offsetWidth / 2,
  )
  mouseY.value = Math.min(
    Math.max(e.clientY, blob.value.offsetHeight / 2),
    window.innerHeight - blob.value.offsetHeight / 2,
  )
}

onMounted(() => {
  posX.value = window.innerWidth / 2 - blob.value.offsetWidth / 2
  posY.value = window.innerHeight / 2 - blob.value.offsetHeight / 2

  gsap.set(blob.value, {
    x: posX.value,
    y: posY.value,
  })

  window.addEventListener('mousemove', handleMouseMove)
  updateBlobPosition()
})

onUnmounted(() => {
  window.removeEventListener('mousemove', handleMouseMove)
  cancelAnimationFrame(animationFrame)
})
</script>

<template>
  <div ref="blob" class="blob"></div>
  <header>
    <nav>
      <RouterLink to="/"><img src="./assets/logo.svg" /></RouterLink>
      <div>
        <RouterLink to="/plants">plants </RouterLink>
        <RouterLink to="/workshops">workshops</RouterLink>
        <RouterLink to="/contact">contact</RouterLink>
      </div>
    </nav>
  </header>
  <main>
    <RouterView />
  </main>
  <footer>
    <p>
      Plantswap is a community initiative by
      <a href="https://www.buurtcampus.amsterdam/" target="_blank">Buurtcampus Oost</a>
    </p>
  </footer>
</template>

<style scoped>
.blob {
  position: fixed;
  left: 0;
  top: 0;
  height: 220px;
  aspect-ratio: 1;
  background: linear-gradient(to right, var(--link-color), var(--sec-color), #b4edaf);
  z-index: -1000;
  pointer-events: none;
  transform-origin: center;
  border-radius: 100%;
  filter: blur(60px);
  opacity: 0.5;
  animation: spin infinite 20s;
}

@keyframes spin {
  50% {
    scale: 1 1.5;
  }
}

header {
  margin-bottom: 3rem;
}

nav {
  width: 100%;
  font-size: 12px;
  display: flex;
  flex-flow: row;
  justify-content: space-between;
  align-items: end;

  & div {
    display: flex;
    flex-flow: row;
    gap: 1.5rem;
  }
}

nav a.router-link-exact-active {
  color: var(--orange);
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  font-size: 20px;
  text-decoration: none;
  color: inherit;
  padding: 0.3rem 1rem;
  border-bottom: solid transparent;
  transition: all ease-out 0.2s;

  &:hover {
    color: var(--orange);
  }
}

footer {
  padding: 2rem;
  display: flex;
  justify-content: center;

  & p {
    font-weight: bold;
  }
}
</style>
