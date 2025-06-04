<script setup></script>

<template>
  <section class="hero">
    <h1>Swap, Grow, Thrive, repeat</h1>
    <h2>Connecting community with plants</h2>
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
  </section>

  <section>
    <h2>Our pillars</h2>
    <div class="pillars">
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
          PlantSwap brings neighbors together through plant swaps making our community more
          connected, lively, and green!
        </p>
      </article>
    </div>
  </section>

  <section class="carousel">
    <h2>The making of... de kast</h2>
    <article class="intro">
      <p>
        The first Neighborhood Campus "stekjeskast" (cutting box) was made by children from the
        Maakplaats 021 at the OBA Javaplein. Here, children from the neighborhood aged 8 and up
        learn, among other things, 3D printing, laser cutting, programming, or making musical
        instruments.
      </p>
    </article>
    <ul>
      <li>
        <img
          src="https://plantswap-webapplicatie.vercel.app/_app/immutable/assets/tweede.817ff5ea.avif"
        />
      </li>

      <li>
        <img
          src="https://plantswap-webapplicatie.vercel.app/_app/immutable/assets/bovenste.63dbcf15.avif"
        />
      </li>

      <li>
        <img
          src="https://plantswap-webapplicatie.vercel.app/_app/immutable/assets/derde.bbba9ac1.avif"
        />
      </li>
    </ul>
  </section>
</template>

<style scoped>
.hero {
  & h1 {
    margin-bottom: 0.5rem;
  }
}

.reasons {
  display: flex;
  flex-flow: row wrap;
  gap: 1.5rem;

  & div {
    padding: 2rem 2rem;
    border-radius: 0.5rem;
  }

  & .reasons_list {
    background: var(--text-color);
    color: var(--bg-color);
    max-width: 40rem;
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

.carousel {
  & ul {
    list-style: '';
    display: flex;
    flex-flow: row;
    gap: 1rem;

    & li {
      display: flex;
      flex-flow: column;
      justify-content: end;
      position: relative;
      height: 30rem;
      width: 30rem;
      border-radius: 0.5rem;
      overflow: hidden;

      & img {
        z-index: -1;
        object-fit: cover;
        height: 100%;
        width: 100%;
      }
    }
  }
}
</style>
