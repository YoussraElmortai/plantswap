<template>
  <h1>Our plants</h1>
  <section class="plants">
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
    </div>
  </section>
</template>

<style scoped>
.wrapper {
  display: flex;
  flex-flow: row wrap;
  gap: 1rem;
}

.plant_card {
  height: fit-content;
  width: 20rem;
  background: var(--sec-color);
  border-radius: 0.5rem;
  overflow: hidden;
  padding: 1rem;

  & img {
    height: 20rem;
    width: 100%;
    object-fit: cover;
  }
}
</style>
