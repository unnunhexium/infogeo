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
  font-weight: 700;
  background: $accent;
  color: $white;
  font-size: 18px;
  padding: 1.125em 1.875em;
  display: inline-block;
  text-decoration: none;
  border: none;
  cursor: pointer;
  transition: background-color 0.2s, border-color 0.2s;

  &:active,
  &:focus,
  &:hover {
    background: $hover;
  }
}
</style>
