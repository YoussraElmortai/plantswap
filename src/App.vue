<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/plants">plants</RouterLink>
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
  text-align: center;
  padding: 1.5rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
}
</style>
