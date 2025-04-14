<script setup></script>

<template>
  <section class="hero">
    <h1>Swap, Grow, Thrive, repeat</h1>
    <h2>Connecting community with plants</h2>
  </section>

  <section class="pillars">
    <article>
      <h3>Vitality</h3>
      <p>
        Plants do more than beautify your home. they teach you about nature, purify the air, and
        boost mental health. Small plants, big perks!
      </p>
    </article>

    <article>
      <h3>Sustainability</h3>
      <p>
        Don’t toss dead plants. learn to care for them! Propagate, swap and grow your collection
        sustainably for free.
      </p>
    </article>

    <article>
      <h3>Collaboration</h3>
      <p>
        PlantSwap brings neighbors together through plant swaps making our community more connected,
        lively, and green!
      </p>
    </article>
  </section>
</template>

<style scoped>
.hero {
  & h1 {
    margin-bottom: 0.5rem;
  }
}

.pillars {
  display: flex;
  flex-flow: row wrap;
  gap: 2rem;

  & article {
    width: 100%;
    height: auto;
    display: flex;
    flex-flow: column;
    gap: 1rem;
    padding: 1rem;
    background: var(--sec-color);
    border-radius: 0.5rem;

    &:nth-of-type(2n) {
      background: var(--accent-color);
    }

    @media (min-width: 770px) {
      width: 30%;
    }
  }
}
</style>
