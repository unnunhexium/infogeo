<template>
  <a :href="href" class="base-button"><slot /></a>
</template>

<script>
export default {
  name: "BaseButton",
  props: {
    href: {
      type: String,
      required: true,
    },
  },
};
</script>

<style lang="scss" scoped>
.base-button {
  font-family: "Open Sans";
  font-size: 18px;
  font-weight: 700;
  display: inline-block;
  padding: 0.75em 1.875em;
  color: $white;
  background: $accent;
  transition: background-color 0.2s, border-color 0.2s;
  text-decoration: none;
  border: none;
  cursor: pointer;

  &:active,
  &:focus,
  &:hover {
    background: $hover;
  }
}
</style>
