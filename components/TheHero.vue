<template>
  <div class="the-hero">
    <!--<div class="the-hero__wrapper">-->
    <h1 class="the-hero__title">infogeo</h1>
    <img src="../assets/1.jpg" class="the-hero__img1" />
    <img src="../assets/2.jpeg" class="the-hero__img2" />
    <h2 class="the-hero__subtitle">
      pewny partner - geodezja, budownictwo, architektura
    </h2>
    <!--</div>-->
  </div>
</template>

<script>
export default {
  name: "TheHero",
};
</script>

<style lang="scss" scoped>
.the-hero {
  background: $accent;
  margin-top: 10em;
  padding: 0 100px;
  display: grid;
  grid-template-columns: 3fr 1fr 2fr;
  row-gap: 50px;

  // &__wrapper {
  // position: relative;
  //}

  &__title,
  &__subtitle {
    color: $white;
  }
  &__title {
    text-transform: uppercase;
    grid-column: span 2;
  }

  &__img1,
  &__img2 {
    width: 100%;
    grid-column: span 1;
    position: relative;
  }

  &__img1 {
    bottom: 30%;
  }

  &__img2 {
    top: 20%;
  }

  &__subtitle {
    text-align: right;
    grid-column: span 2;
  }
}
</style>