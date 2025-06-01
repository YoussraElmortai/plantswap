<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div class="blob"></div>
  <header>
    <nav>
      <RouterLink to="/"><img src="./assets/logo.svg" /></RouterLink>
      <RouterLink to="/plants">plants </RouterLink>
      <RouterLink to="/workshops">workshops</RouterLink>
      <RouterLink to="/contact">contact</RouterLink>
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
  position: absolute;
  height: 120px;
  width: 120px;
  background: var(--accent-color);
  z-index: -1000;
  border-radius: 100%;
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
    flex-flow: row wrap;
    gap: 1rem;
  }
}

nav a.router-link-exact-active {
  border-bottom: solid var(--sec-color);
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  font-size: 18px;
  text-decoration: none;
  color: inherit;
  padding: 0.3rem 1rem;
  border-bottom: solid transparent;
  transition: all ease-out 0.2s;

  &:hover {
    border-bottom: solid var(--accent-color);
  }
}

footer {
  padding: 2rem;
  display: flex;
  justify-content: center;
}
</style>
