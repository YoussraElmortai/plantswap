<template>
  <section class="intro">
    <h1>Our plants</h1>
    <p>
      Do you have one or more plant cuttings to spare, and would you like to exchange them for a new
      plant? Check out our selection below.
    </p>
  </section>
  <section class="plants">
    <div class="filter">
      <span>Filter by:</span>
      <button class="filter_button">Tropical</button>
      <button class="filter_button">Fast-Growing</button>
      <button class="filter_button">Low Maintenance</button>
      <button class="filter_button">High Maintenance</button>
      <button class="filter_button">Moderate Water</button>
      <button class="filter_button">Drought-Tolerant</button>
    </div>

    <div class="wrapper">
      <article class="plant_card">
        <img src="https://i.pinimg.com/736x/fb/2c/5f/fb2c5f8873fab78087317653d5b72dcc.jpg" />
        <div class="plant_content">
          <h3>Monstera</h3>
          <p></p>
        </div>
        <a class="button" href="/plants">More info</a>
      </article>

      <article class="plant_card">
        <img src="https://i.pinimg.com/736x/fb/2c/5f/fb2c5f8873fab78087317653d5b72dcc.jpg" />
        <div class="plant_content">
          <h3>Monstera</h3>
          <p></p>
        </div>
        <a class="button" href="/plants">More info</a>
      </article>

      <article class="plant_card">
        <img src="https://i.pinimg.com/736x/fb/2c/5f/fb2c5f8873fab78087317653d5b72dcc.jpg" />
        <div class="plant_content">
          <h3>Monstera</h3>
          <p></p>
        </div>
        <a class="button" href="/plants">More info</a>
      </article>

      <article class="plant_card">
        <img src="https://i.pinimg.com/736x/fb/2c/5f/fb2c5f8873fab78087317653d5b72dcc.jpg" />
        <div class="plant_content">
          <h3>Monstera</h3>
          <p></p>
        </div>
        <a class="button" href="/plants">More info</a>
      </article>

      <article class="plant_card">
        <img src="https://i.pinimg.com/736x/fb/2c/5f/fb2c5f8873fab78087317653d5b72dcc.jpg" />
        <div class="plant_content">
          <h3>Monstera</h3>
          <p></p>
        </div>
        <a class="button" href="/plants">More info</a>
      </article>
    </div>
  </section>
</template>

<style scoped>
.filter {
  display: flex;
  flex-flow: row wrap;
  align-items: center;
  gap: 0.5rem;
  margin-bottom: 2rem;
}

.filter_button {
  padding: 0.5rem;
  border: none;
  border-radius: 0.5rem;
  background-color: var(--accent-color);
  cursor: pointer;

  &:nth-of-type(2n) {
    background-color: var(--sec-color);
  }

  &:nth-of-type(3n) {
    background-color: var(--orange);
  }

  &:hover {
    background-color: var(--text-color);
    color: var(--bg-color);
  }
}

.wrapper {
  display: flex;
  flex-flow: row wrap;
  gap: 1rem;
}

.plant_card {
  height: fit-content;
  width: 100%;
  background: var(--sec-color);
  border-radius: 0.5rem;
  overflow: hidden;
  padding: 1rem;

  @media (min-width: 770px) {
    width: 40%;
  }

  @media (min-width: 1024px) {
    width: 30%;
  }

  & img {
    height: 20rem;
    width: 100%;
    object-fit: cover;
    border-radius: 0.5rem;
  }
}
</style>
