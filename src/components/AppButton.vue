<script>
export default {
  props: {
    content: String,
    color: String,
  },
};
</script>

<template>
  <a :class="color" href="">{{ content }}</a>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;
a {
  display: inline-block;
  padding: 8px 32px;
  text-decoration: none;
  color: $char-white;
  font-size: 0.6rem;

  &.blue {
    background-color: $primary-color;
  }

  &.dark {
    background-color: $char-color;
  }
}
</style>
