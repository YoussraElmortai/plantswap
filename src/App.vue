<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/plants">plants </RouterLink>
      <RouterLink to="/workshops">workshops</RouterLink>
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
nav {
  width: 100%;
  font-size: 12px;
  padding: 1.5rem;
  display: flex;
  flex-flow: row;
  justify-content: space-around;
}

nav a.router-link-exact-active {
  background: var(--sec-color);
  border-radius: 0.5rem;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  font-size: 18px;
  text-decoration: none;
  color: inherit;
  padding: 0.5rem 1rem;
  transition: all ease-out 0.2s;

  &:hover {
    background: var(--accent-color);
    border-radius: 0.5rem;
  }
}
</style>
