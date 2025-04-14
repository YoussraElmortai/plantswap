<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <nav>
      <RouterLink to="/">Plantswap</RouterLink>
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
nav {
  width: 100%;
  font-size: 12px;
  padding: 2rem 3rem;
  display: flex;
  flex-flow: row;
  justify-content: space-between;
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
</style>
