<template>
  <div class="the-hero">
    <div class="the-hero__background"></div>
    <div class="the-hero__wrapper">
      <h1 class="the-hero__title">infogeo</h1>
      <img src="/1.jpg" class="the-hero__img1" />
      <img src="/2.jpeg" class="the-hero__img2" />
      <h2 class="the-hero__subtitle">
        pewny partner - geodezja, budownictwo, architektura
      </h2>
    </div>
  </div>
</template>

<script>
export default {
  name: "TheHero",
};
</script>

<style lang="scss" scoped>
.the-hero {
  margin-top: 10em;
  padding-bottom: 50px;

  &__background {
    background: $accent;
    width: 100%;
    height: 70vh;
    position: absolute;
    top: 30vh;
  }

  &__wrapper {
    position: relative;
    display: grid;
    grid-template-columns: 3fr 1fr 2fr;
    row-gap: 50px;
    max-width: $layout-width;
    margin: 0 auto;
  }

  &__title,
  &__subtitle {
    color: $white;
  }
  &__title {
    text-transform: uppercase;
    grid-column: span 2;
    display: flex;
    align-items: flex-end;
    margin: 40px;
  }

  &__img1,
  &__img2 {
    width: 100%;
    grid-column: span 1;
    position: relative;
  }

  &__subtitle {
    grid-column: span 2;
    display: flex;
    align-items: flex-start;
    margin: 40px;
  }
}
</style>