<script setup></script>

<template>
  <section class="hero">
    <h1>Swap, Grow, Thrive, repeat</h1>
    <h2>Connecting community with <span class="accent"> plants</span></h2>
    <div class="">
      <img
        src="https://plantswap-webapplicatie.vercel.app/_app/immutable/assets/derde.bbba9ac1.avif"
      />
    </div>
  </section>

  <section class="reasons">
    <div class="reasons_list">
      <h2>4 Reasons Why You Should Start Keeping Plants</h2>
      <ol>
        <li>
          Instant mood boosters – because staring at a leafy friend is cheaper than therapy (and
          they don’t talk back).
        </li>
        <li>
          You’ll finally have a valid excuse to talk to yourself – “Just checking if my fern needs
          water… or emotional support.”
        </li>
        <li>
          Drama-free companionship – no ghosting, just the occasional dramatic wilt when you forget
          they exist.
        </li>
        <li>
          Survival of the fittest (for you AND them) – if they live, you’re a plant whisperer. If
          they die… well, it was a “learning experience.”
        </li>
      </ol>
    </div>
    <div class="">
      <img src="" />
    </div>
  </section>
</template>

<style scoped>
.hero {
  & h1 {
    margin-bottom: 0.5rem;
  }

  & div {
    height: 50vh;
    padding: 0;

    & img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      border-radius: 0.5rem;
    }
  }
}

.reasons {
  display: flex;
  flex-flow: row wrap;
  gap: 1.5rem;

  & .reasons_list {
    background: var(--text-color);
    color: var(--bg-color);
    max-width: 40rem;
    padding: 2rem 2rem;
    border-radius: 0.5rem;
  }

  & ol {
    font-size: 20px;
    display: flex;
    flex-flow: column;
    padding: 1rem;
    gap: 1.5rem;
  }
}

.pillars {
  display: flex;
  flex-flow: row wrap;
  justify-content: space-between;
  gap: 2rem;

  & article {
    width: 100%;
    height: auto;
    display: flex;
    flex-flow: column;
    padding: 1rem;
    background: var(--sec-color);
    border-radius: 0.5rem;

    &:nth-of-type(2n) {
      background-color: var(--accent-color);
    }

    &:nth-of-type(3n) {
      background-color: var(--orange);
    }

    @media (min-width: 770px) {
      width: 30%;
    }
  }
}
</style>
