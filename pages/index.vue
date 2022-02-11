<template>
  <div class="home">
    <TheHero class="home__the-hero"></TheHero>
    <ContentCard
      v-for="content in contents"
      :content="content"
      :key="content.id"
      class="home__section"
    ></ContentCard>
  </div>
</template>

<script>
import contents from "../data/content";

export default {
  name: "IndexPage",
  components: {},
  data() {
    return {
      contents,
    };
  },
};
</script>

<style lang="scss">
@import "../styles/reset.scss";
.home {
}
</style>
