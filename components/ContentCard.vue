<template>
  <div class="content-card">
    <h3 class="content-card__title"><slot name="title" /></h3>
    <div class="content-card__span"></div>
    <p class="content-card__content"><slot name="content" /></p>
    <BaseButton class="content-card__button">czytaj więcej</BaseButton>
  </div>
</template>

<script>
import BaseButton from "./base/BaseButton.vue";
export default { components: { BaseButton } };
</script>

<style lang="scss" scoped>
.content-card {
  &__span {
    background: $accent;
    padding: 4px 0px;
    width: 8em;
  }
}
</style>