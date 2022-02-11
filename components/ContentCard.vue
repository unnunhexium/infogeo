<template>
  <div :class="contentCardClasses">
    <div class="content-card__text-wrapper">
      <h3 class="content-card__title">{{ content.title }}</h3>
      <div class="content-card__span"></div>
      <p class="content-card__content">{{ content.content }}</p>
      <BaseButton class="content-card__button">czytaj więcej</BaseButton>
    </div>
    <div class="content-card__img-wrapper">
      <div class="content-card__img-wrapper--cut">
        <img :src="imageSrc" class="content-card__img1" />
      </div>
    </div>
  </div>
</template>

<script>
import BaseButton from "./base/BaseButton.vue";
export default {
  name: "ContentCard",
  components: { BaseButton },
  props: {
    content: {
      type: Object,
      required: true,
    },
  },
  computed: {
    imageSrc() {
      return this.content.image;
    },
    contentCardClasses() {
      return [
        "content-card",
        { "content-card__reverse": this.content.id % 2 === 0 },
      ];
    },
  },
};
</script>

<style lang="scss" scoped>
.content-card {
  display: flex;
  max-width: $layout-width;
  margin: 0 auto;
  padding-bottom: 50px;

  &__reverse {
    display: flex;
    flex-direction: row-reverse;
  }

  &__text-wrapper {
    width: 50%;
  }

  &__title {
    margin-top: 40px;
  }

  &__span {
    background: $accent;
    padding: 4px 0px;
    width: 8em;
    margin-top: 30px;
  }

  &__content {
    margin-top: 30px;
    line-height: 1.6rem;
  }

  &__button {
    margin-top: 30px;
  }

  &__img-wrapper {
    width: 50%;
  }

  &__img-wrapper--cut {
    width: 50%;
    margin: 0 auto;
    overflow: hidden;
    position: relative;
  }

  &__img1 {
    max-width: 200%;
    max-height: 500px;
    width: 200%;
    position: relative;
    right: 65%;
  }
}
</style>