<template>
  <section class="intro">
    <h1>Join us for a workshops</h1>
    <p>
      Workshops are fantastic learning opportunities where participants can gain practical skills,
      acquire new knowledge, and often meet new people as well.
    </p>
  </section>
  <section class="workshops">
    <article class="workshop_card">
      <span></span>
      <div class="workshop_image">
        <img
          src="https://img.freepik.com/free-photo/person-transplanting-plants-new-pots_23-2149384672.jpg?semt=ais_hybrid&w=740"
        />
      </div>
      <div class="workshop_content">
        <h3>Painting with plants</h3>
        <p>
          Workshops are fantastic learning opportunities where participants can gain practical
          skills,
        </p>
        <ul class="workshop_data">
          <li>OBA Linnaeusstraat</li>
          <li>Gratis</li>
          <li>Zaterdag 3 juni 2024</li>
        </ul>
      </div>
    </article>
    <article class="workshop_card">
      <span></span>
      <div class="workshop_image">
        <img
          src="https://img.freepik.com/free-photo/person-transplanting-plants-new-pots_23-2149384672.jpg?semt=ais_hybrid&w=740"
        />
      </div>
      <div class="workshop_content">
        <h3>Painting with plants</h3>
        <p>
          Workshops are fantastic learning opportunities where participants can gain practical
          skills,
        </p>
        <ul class="workshop_data">
          <li>OBA Linnaeusstraat</li>
          <li>Gratis</li>
          <li>Zaterdag 3 juni 2024</li>
        </ul>
      </div>
    </article>
    <article class="workshop_card">
      <span></span>
      <div class="workshop_image">
        <img
          src="https://img.freepik.com/free-photo/person-transplanting-plants-new-pots_23-2149384672.jpg?semt=ais_hybrid&w=740"
        />
      </div>
      <div class="workshop_content">
        <h3>Painting with plants</h3>
        <p>
          Workshops are fantastic learning opportunities where participants can gain practical
          skills,
        </p>
        <ul class="workshop_data">
          <li>OBA Linnaeusstraat</li>
          <li>Gratis</li>
          <li>Zaterdag 3 juni 2024</li>
        </ul>
      </div>
    </article>
  </section>
</template>

<style scoped>
.workshops {
  display: flex;
  flex-flow: row wrap;
  gap: 1.5rem;
}

.workshop_card {
  position: relative;
  z-index: 1;
  border: solid;
  border-radius: 0.5rem;
  height: 30rem;
  width: 100%;
  display: flex;
  flex-flow: column;
  justify-content: end;
  overflow: hidden;

  & img {
    position: absolute;
    z-index: -1;
    height: 100%;
    width: 100%;
    object-fit: cover;
    transition: all 0.2s ease-out;
  }

  &:hover img {
    transform: scale(1.03);
  }

  @media (min-width: 770px) {
    width: 40%;
  }

  @media (min-width: 1024px) {
    width: 30%;
  }
}

.workshop_image {
  position: absolute;
  height: 100%;
  width: 100%;
  background: linear-gradient(
    10deg,
    rgba(10, 26, 13, 1) 0%,
    rgba(8, 33, 37, 0.85) 12%,
    rgba(72, 112, 88, 0.71) 65%,
    rgba(82, 117, 94, 0.62) 76%,
    rgba(242, 241, 240, 0.56) 100%
  );
}

.workshop_content {
  position: relative;
  color: var(--bg-color);
  display: flex;
  flex-flow: column;
  padding: 1rem;
  gap: 1rem;

  & ul {
    list-style: none;
  }
}
</style>
